# Apache Jmeter

JMeter script to test a CRUD REST API

## Tools

* Apache Jmeter 5.5

## REST API

CRUD API under test: https://github.com/harishkannarao/MySpringBoot

#### Running the api in local

```
docker-compose -f docker_local/docker-compose.yml up --build -d

mvn spring-boot:run -pl JdbcExample/JdbcApplication
```

## Run Jmeter with html report

```
jmeter -n -t REST_API_Test_Plan.jmx -l logs/jmeter_result.jtl -j logs/jmeter.log -e -o report
```

## Run Jmeter without html report

```
jmeter -n -t REST_API_Test_Plan.jmx -l logs/jmeter_result.jtl -j logs/jmeter.log
```

## Generate html report from existing jtl file

```
jmeter -j logs/jmeter.log -g logs/jmeter_result.jtl -o report
```