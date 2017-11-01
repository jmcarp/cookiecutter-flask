FROM datagovsg/python-node
WORKDIR /opt/app
RUN apt-get update
RUN apt-get -y install \
  libpq-dev \
  postgresql-client \
  postgresql-client-common \
  && apt-get clean \
  && apt-get autoremove
COPY . .
RUN pip install -r requirements/dev.txt
RUN npm install
RUN npm run build
EXPOSE 5000
