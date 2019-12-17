FROM ruby:2.6.0 
RUN mkdir -p /usr/app
WORKDIR /usr/app
COPY rails-example-project . 
RUN apt-get update && apt-get install -y nodejs
RUN gem install bundler
RUN bundle install
ENV RAILS_MASTER_KEY=AePhoof8soXaele1leipohmahjae3eir
#RUN rails db:migrate RAILS_ENV=production
RUN rails db:migrate
RUN rake assets:precompile
#WORKDIR /usr/app/spring-example-project
ENV RAILS_LOG_TO_STDOUT=true
#ENV SECRET_KEY_BASE=asdalol1234
#RUN echo "asdalol1234" > /usr/app/config/master.key
CMD rails s
