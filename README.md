# installing_ruby_on_rails
### Tutorial - How To Install Ruby On Rails On Mac

In this tutorial you are going to learn how to install Ruby On Rails on Mac OS X 10.11 El Capitan. 

To do so, just follow the three easy steps below.

### 1. Installing Homebrew

[Homebrew](http://brew.sh/) is a package manager for OS X that allows you to install useful packages. 

To install it you need to have installed on you mac the program Xcode and to have said 'Yes' when you were asked if you wanted to install Command Line Developer Tools. 

After you have installed Xcode, you just need to run your Terminal the following command.

	ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

**Note:** In case you have installed Xcode without Command Line Developer Tools, you can run the following command on Terminal, and an alert box will pop-up asking you if you want to install it.

	xcode-select --install

### 2. Installing Ruby 

The installation of Ruby is going to be done with **rbenv**. 

Let's start by running the following command on Terminal to install rbenv.

	brew install rbenv ruby-build

After rbenv is installed we need to add it to bash, so that every time you open Terminal it is loaded and ready to use. To do this, run the following commands.

	echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile

Now that the command is added to the file we just need to execute the file so that it takes effect in the current Terminal window.

	source ~/.bash_profile

With rbenv installed and configured, it's time to install Ruby. In this tutorial we are installing the version 2.3.0 of Ruby, but feel free to install the version that you desire.
	
To install Ruby run the following command.

	rbenv install 2.3.0

**Other Commands**

If you want to set a specific version of Ruby for all projects, run the following command.

	rbenv global 2.3.0

If you want to set a specific version of Ruby to only one project, run the following command. It will set the specified version on the current directory only.

	rbenv local 2.3.0

If you want to check you current Ruby version, run the following command.

	ruby -v

**Note:** If you want to know which is the current stable version of Ruby, just go [here](https://www.ruby-lang.org/en/downloads/).

### 3. Installing Rails

Finally, the last step is to install Rails. This can be achieved by running two simple commands on your Terminal. The first command installs Rails.

	gem install rails -v 4.2.6

The second command is to let rbenv know that rails is installed and to create de executable.

	rbenv rehash

You have now successfully installed Ruby on Rails on your Mac OS X.

**Other Commands**

If you want to check you current Rails version, run the following command.
	
	rails -v

**Note:** If you want to know which is the current stable version of Rails, just go [here](https://rubygems.org/gems/rails).




