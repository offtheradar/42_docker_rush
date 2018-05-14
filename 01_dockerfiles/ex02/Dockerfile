FROM ruby
RUN ["apt-get", "update", "-y", "&&", "apt-get", "upgrade", "-y"]
RUN ["apt-get", "-y", , "install", "build-essential"]
RUN ["apt-get", "-y", "install", "sqlite3"]
RUN ["apt-get", "-y", "install", "nodejs"]
RUN ["gem", "install", "bundler"]
RUN ["mkdir", "/opt/app"]
WORKDIR /opt/app
RUN ["gem", "install", "rails"]
ONBUILD COPY . /opt/app
ONBUILD RUN ["bundle", "install"]
ONBUILD RUN rake db:migrate
ONBUILD RUN rake db:seed
ONBUILD EXPOSE 3000