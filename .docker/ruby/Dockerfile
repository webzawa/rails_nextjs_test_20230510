FROM ruby:3.2.2

ENV TZ=Asia/Tokyo

RUN apt-get update -qq && \
    apt-get install -y build-essential \
                       graphviz \
                       imagemagick \
                       libpq-dev &&\
    mkdir /test_rails_20230510-rails

ENV APP_ROOT /test_rails_20230510-rails
WORKDIR $APP_ROOT

ADD ./Gemfile $APP_ROOT/Gemfile
ADD ./Gemfile.lock $APP_ROOT/Gemfile.lock

RUN gem install bundler && \
    bundle install -j4
ADD . $APP_ROOT

CMD ["rails", "server", "-b", "0.0.0.0"]