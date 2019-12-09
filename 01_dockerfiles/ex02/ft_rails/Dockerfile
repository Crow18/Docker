FROM ruby

RUN apt-get update && apt install -y nodejs && gem install rails bundler

ONBUILD WORKDIR /opt

ONBUILD RUN rails new app

ONBUILD WORKDIR /opt/app

ONBUILD RUN bundle install && rails generate migration CreateProducts name:string && rake db:migrate
