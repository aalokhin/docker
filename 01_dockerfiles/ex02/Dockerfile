FROM ruby

MAINTAINER aalokhin <aalokhin@student.unit.ua>



RUN apt-get update -y && apt-get upgrade -y && gem install rails && apt-get install nodejs -y

ONBUILD EXPOSE 3000
ONBUILD COPY . /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN bundle install && rails db:migrate && rails db:seed

# docker build --tag=ruby .
# docker run -it --rm ruby
# docker rmi $(docker images -q)