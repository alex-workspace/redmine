# Bản build 19/09/2023 dùng resource của chính redmine
version: '3.1'
services:
  redmine:
    image: redmine
    environment:
      REDMINE_DB_MYSQL: 192.168.45.52
      REDMINE_DB_PORT: 19202
      REDMINE_DB_DATABASE: nex-redmine-v2
      REDMINE_DB_USERNAME: redmine
      REDMINE_DB_PASSWORD: UnGfAeU75QE2Jx
      REDMINE_DB_ENCODING: utf8
      REDMINE_SECRET_KEY_BASE: supersecretkey
    ports:
      - "3000:3000"
      - "80:80"
    volumes:
      - ./red505/files:/usr/src/redmine/files
      - ./red505/plugins:/usr/src/redmine/plugins
      - ./red505/themes:/usr/src/redmine/themes
