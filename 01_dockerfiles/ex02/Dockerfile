FROM ruby:2.5
RUN apt-get update && apt-get install -y --no-install-recommends apt-utils wget nodejs build-essential libpq-dev
RUN apt-get install -y bundler rake
ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app
ONBUILD RUN bundle update\
			&& rake db:migrate

#docker build -t ft-rails .
#docker build -t ex02 -f app/Dockerfile .
#docker run -p 3000:3000 -it --rm ex02
