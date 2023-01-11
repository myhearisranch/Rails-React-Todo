FROM ruby:3.0

RUN apt-get update --qq && apt-get install -y build-essential libpq-dev node.js

ENV APP_PATH /myapp

RUN mkdir $APP_PATH
WORKDIR $APP_PATH

COPY entrypoint.sh /usr/bin/
RUN chmod +x /usr/bin/entrypoint.sh
ENTRYPOINT [ "entrypoint.sh" ]
EXPOSE 3000

CMD [ "rails", "server", "-b", "0.0.0.0" ]