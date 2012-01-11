# Rails Development on Windows...Seriously

## Introduction

I love Windows. I love how stupidly easy it is for browsing the web, checking
email, or writing Word documents (if you still do that). I love that
Windows is everywhere and even my grandmother can use it.

At the same time, I also HATE Windows. If you're trying to program anything besides
.NET, it's an uphill battle.

The title of this talk is 'Rails Development on Windows...Seriously.' I'm going
to show you the past, the present, and the future of being a Rails developer in a
Windows world; and show you some of the tools you need to be successful. 

## The Past

Shhh. Don't tell anyone, but I started programming Ruby on Rails in a Windows
environment. At the time, fall 2008, I was using Windows Vista. 

Yes, you can all shudder in fear.

As bad as that release was, I made the most of it. Having my only programming
experience in a classroom-setting, I installed Aptana RadRails and hit the
ground stumbling.

Back then, there were basically two ways to install Rails on Windows:

1. Install JRuby and run on top of the Java Virtual Machine

2. Download the RubyInstaller executable and the DevKit and install everything
manually

I had no idea what JRuby really was or why I needed it and I really wasn't 
sure what I was doing in the first place so I opted for option two. I think
there may have been a way to install through RadRails but it was a craps-shoot
if it worked properly.

Everything installed fine and as long as you accepted all defaults then you
were golden. Heaven help the programmer who wanted to install Ruby to a
different path.

The biggest problem with having to install Ruby this way is that if you didn't
grab the DevKit, you couldn't build any C extensions. By the way, Ruby is
written in C and there are a shit-load of libraries that require C extensions
to build correctly. For beginners to run into these errors when all they want
to do is write a web app, this sucked.

## The Present

Let's fast-forward to 2011 and the biggest savior to Rails developers who want
to use Windows is RailsInstaller, created and maintained by Wayne E. Seguin. 

If you don't know Wayne, he works his ass off on Ruby Version Manager, SM Framework,
and RailsInstaller. He does it all for the good of the community so by him a
beer next time you see him.

RailsInstaller is an amazing piece of software because it packages up everything 
you need to start programming Ruby on Rails. Out of the box, you get Ruby, Rails,
Bundler, Git, Sqlite, TinyTDS, the DevKit for those pesky C extensions, and you
actually get support for SQLServer. Trying to hunt
down all of these components and installing them separately is a nightmare.

## The Future

Honestly, I don't know what's in store for the future right now,
but it has to be better than the past. We've come a long way and there's still 
a lot of work to be done.

So you've installed RailsInstaller and now you have a Ruby on Rails environment
but where do you go from here?

## What do I need?

Here are some of the essential things you need to be a successful Rails developer
in Windows

### Git

If you aren't tracking your code changes with Source Code Management, you're an idiot.
I don't care what anyone says, the best one is Git. The best thing about Git is 
that it's *distributed*. This means *everyone* has the full code repository so no
waiting on the Subversion server! There's also Github and if you aren't familiar
with it, it's amazing. Github brings a social aspect to coding and provides for
easy collaboration.

Honestly, I don't care what SCM you use as long as you use something. Quit creating
index.html.old. That isn't reliable and if you use a code-hosting service, then you
don't need to worry about your computer crashing. And we're running Windows so this
is something we probably worry about a few times a day.

### Pik

Ruby Version Manager, or RVM, is another exceptional tool written by Wayne. It makes it easy
to manage different versions of Ruby, provides sandboxed environments for different
projects, and allows people to test software compatibility. Unfortunately it doesn't run
on Windows.

The next best thing is a tool called Pik. Using Pik, you can install different
versions of Ruby including JRuby and IronRuby. It doesn't have the bells-and-whistles
that RVM does but trying to run mutliple Rubies without it would be a nightmare.
You can grab Pik from the Github page at github.com/vertiginous/pik.

### IDE or Text Editor

Now you need a way to actually write your applications. No, we're not going to 
fire up Visual Studio; it doesn't tend to play well with Rails
When choosing an editor, you can either go with a Text Editor or an Integrated
Development Environment. All of the options I'll talk about run across platforms so you
can use them on Windows, Mac, or Linux.

#### IDEs

If you're used to an all-in-one package, there are great offerings in JetBrains
RubyMine and Aptana Studio. You have to pay for RubyMine but it is by far the
most polished and has a ridiculous amount of features for editing, testing, and
deploying your application.

Aptana Studio is a free option and if you don't want to shell out the money for
RubyMine, is a great alternative. It's built on top of Eclipse so the Java developers
will feel right at home.

#### Text Editors

My favorite and the option chosen by most Rails developers is just a Text Editor.
There are a few different options that I recommend but the one thing I don't is
Notepad. Don't even touch that turd-of-a-program.

Vim is tried and true and has been around forever. It's incredibly extensible, 
and very fast. People tend to say that learning Vim is hard
but really there are a handful of commands to really need to know off the bat and
the rest you can pick up as you go. The best thing about Vim is that you can launch
it from the command line and start editing.

SublimeText is something that has a pretty big following. It costs money but not
that much and has support for Ruby and Rails baked in. I definitely encourage you
to check this one out.

Redcar is a great editor that is actually written in Ruby. Because of this, extending
it is easy since you can write the extensions and don't need to learn a separate
syntax. Another nice thing is that Redcar has support for TextMate bundles so you
can probably find extensions for anything you need.

## Learn something

Rails has an incredible community. Learning how to write great Ruby on Rails applications
has never been easier and there are resources for any type of learning style.

### Screencasts

I have to mention Railscasts becuase the amount of knowledge is just amazing. Ryan Bates has
been doing weekly screencasts on Rails topics since 2007(?). These are usually around 10-15
minutes and cover one thing each episode. If you want to learn how to add authentication
to your app quickly and easily, check out Railscasts.

### Tutorials

By far, the best tutorial is RailsTutorial by Michael Hartl. He goes into detail on
topics such as Ruby, Rails, and test-driven development. The HTML version of the book
is free and you can also purchase the PDF. If you want even more instruction, he has
some great screencasts there as well.

You can find many more tutorials, screencasts and documentation at http://rubyonrails.org
and by searching Google.

## Show the world

So you've written your first Ruby on Rails application and you're wondering where to go
from here. Let's share this really cool application with the rest of the world.
Save yourself a headache and a lot of work and don't think about deploying to a Windows
server. Thankfully, there are multiple Cloud Platform providers these days so you
don't even need to set up your own server. I'm obviously biased towards Engine Yard
but check out these other guys as well and see which one fits you better.

## Caveat

There's one major thing to know when writing Rails apps on Windows and it mainly comes
into play when working across platforms. Because many Windows requires binaries many
times for the gems to work correctly, gem developers will release different versions
for Unix and Windows. If you're deploying to a Unix environment, you'll need to make
sure to install the Unix versions wherever you're deploying.

## Troubleshooting

Inevitably, you're going to run into trouble. Even with all of the documentation available,
you still sould know where to go for help.

### Ruby on Rails Guides

The Ruby on Rails Guides are exactly what they say. They're basically the official
documentation for Rails. Often times they are a great starting point if you need
reference for standard Rails topics.

### Forums

If you need help on something out of the scope of the guides, a good forum is your next
best place. StackOverflow is probably the widest used forum site for programming help.
You can ask and answer questions and there is a point system for your activity. The
questions are also indexed by Google so a well-formed Google search returns great
results.

### IRC

The place I go when everything else fails is IRC, which stands for Internet Relay Chat.
IRC has been around for years and though I've never been a huge fan, you can talk with
people in real time about your issues.

If you're going to be in IRC rooms a lot, you need to find a good desktop client. I've
used mIRC with decent success but I'm sure there are many more out there. Whichever
you choose, there are a couple rooms that you need to hang out in: #Rails
and #RailsInstaller.

## What's next

I know this seems like a lot of information up front and I could probably go into much
more detail but I'm trying to save your sanity. If you want to check out these
slides again, you can go to emachnic.github.com/rails\_dev\_windows and you can also
get the notes at github.com/emachnic/rails\_dev\_windows.

The best thing you can do is get the software and start building something.
You can read all of the books and watch all the screencasts you want but until
you build a real application, the information won't stick. If you need help,
use the resources and you can find me online everywhere as emachnic. Good luck
and most important, HAVE FUN!

## Questions

