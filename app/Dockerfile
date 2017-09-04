FROM ruby:2.3.4

ENV APP_HOME /app

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
RUN gem install bundler

WORKDIR /tmp
ADD ./test_app/Gemfile Gemfile
ADD ./test_app/Gemfile.lock Gemfile.lock
RUN bundle install

ADD . $APP_HOME
WORKDIR $APP_HOME
