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