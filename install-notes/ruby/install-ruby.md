# Ruby Installation

## macOS

1. Install gpg (via homebrew)
```
brew install gnupg
```

2. Install gpg keys for [rvm](https://rvm.io/rvm/security)
```
gpg --keyserver hkp://pgp.mit.edu --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
```

3. Install rvm with stable version of ruby
```
\curl -sSL https://get.rvm.io | bash -s stable --ruby
```

OPTIONAL: If you want to install rspec (for ruby BDD tests)...
- Install rspec (via gem)
```
gem install rspec
```

OPTIONAL: Install everything in the Gemfile (via the bundler)
```
bundle install
```
NOTE: `bundle install` is sort of the equivalent of `npm install` or `yarn install`, per se.


## Points of Interest
- Rake = Ruby Make
- Rakefile = Similar to makefile but for ruby, a task runner. 
- Gem = Ruby Package
- Gemfile = A file of ruby packages/dependencies
- Bundler = Ruby equivalent of npm - node package manager (dependency manager/package manager)
- rvm = Ruby version manager (equivalent to nvm - node version manager)

