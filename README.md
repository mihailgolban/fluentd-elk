# Fluentd Elk

Centralized log aggregation with Fluentd and ELK

## Installation

1. Copy `.env.example` to `.env`

2. Run the following command

```bash
docker-compose up -d
```

## Usage

```yml
services:
  web:
    image: httpd
    ports:
      - "8080:80"
    links:
      - fluentd
    logging:
      driver: "fluentd"
      options:
        fluentd-address: <fluent-address>:24224
        tag: httpd.access
```
