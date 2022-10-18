
![Logo](https://user-images.githubusercontent.com/64506580/159311466-f720a877-6c76-403a-904d-134addbd6a86.png)

* This is a modification of the following repo - https://github.com/huntabyte/tig-stack.git

# Telegraf, InfluxDB, Grafana (TIG) Stack

Gain the ability to analyze and monitor telemetry data by deploying the TIG stack within minutes using [Docker](https://docs.docker.com/engine/install/) and [Docker Compose](https://docs.docker.com/compose/install/).


## ⚡️ Getting Started

Clone the project

```bash
  git clone https://github.com/devunderslash/tig-stack.git
```

Navigate to the project directory

```bash
  cd tig-stack
```

Change the environment variables define in `.env` that are used to setup and deploy the stack
```bash
├── telegraf/
├── .env         <---
├── docker-compose.yml
├── entrypoint.sh
└── ...
```

Customize the `telegraf.conf` file which will be mounted to the container as a persistent volume

```bash
├── telegraf/
│   ├── telegraf.conf <---
├── .env
├── docker-compose.yml
├── entrypoint.sh
└── ...
```

Start the services
```bash
docker-compose up -d
```

Access the Services
- [Grafana](localhost:3000)
- [InfluxDB](localhost:8086)


## Docker Images Used (Official & Verified)

[**Telegraf**](https://hub.docker.com/_/telegraf) / `1.19`

[**InfluxDB**](https://hub.docker.com/_/influxdb) / `2.1.1`

[**Grafana**](https://hub.docker.com/r/grafana/grafana) / `latest`



## Resources

This is a modification of the following repo - https://github.com/huntabyte/tig-stack.git
- https://www.blackvoid.club/grafana-8-influxdb-2-telegraf-2021-monitoring-stack/
- https://towardsdatascience.com/get-system-metrics-for-5-min-with-docker-telegraf-influxdb-and-grafana-97cfd957f0ac
- https://github.com/phillhocking/aws-ubuntu-tig
- https://github.com/pihlajus/ruuvitag-aws-provisioning
- https://hackernoon.com/monitor-your-infrastructure-with-tig-stack-b63971a15ccf
- https://octoperf.com/blog/2019/09/19/kraken-kubernetes-influxdb-grafana-telegraf/#prerequisites

