+++
title = "Rails Projekt mit spezieller Ruby und Rails Version"
date = 2019-12-11
draft = true
+++

```bash
export RAILS_GEM_VERSION='5.2.3'
export RUBY_VERSION='2.6.5'
rvm use $RUBY_VERSION
gem install rails --version $RAILS_GEM_VERSION
rails new doctolib-test
```
