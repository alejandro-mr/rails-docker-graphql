FROM ruby:2.5

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
RUN mkdir -p /usr/src/app
WORKDIR /usr/src/app

RUN gem install rails
COPY Gemfile Gemfile.lock ./
RUN bundle install
COPY . .
