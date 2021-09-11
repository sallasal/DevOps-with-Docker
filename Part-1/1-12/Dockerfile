FROM ubuntu:18.04

EXPOSE 5000

# Add env variables
ENV REACT_APP_BACKEND_URL=http://localhost:8080/

COPY . ./myapp
WORKDIR ./myapp

# Install curl
RUN apt-get update && apt-get install -y curl python

# Install node and serve
RUN curl -sL https://deb.nodesource.com/setup_14.x | bash
RUN apt install -y nodejs
RUN node -v && npm -v
RUN npm install

# Start in prod mode
RUN npm run build
RUN npm install -g serve

CMD ["serve", "-s", "-l", "5000", "build"]

