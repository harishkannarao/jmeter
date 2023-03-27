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
jmeter -n -t REST_API_Test_Plan.jmx -l REST_API_Test_Plan.jtl -j REST_API_Test_Plan.log -e -o report
```

## Run Jmeter without html report

```
jmeter -n -t REST_API_Test_Plan.jmx -l REST_API_Test_Plan.jtl -j REST_API_Test_Plan.log
```

## Generate html report from existing jtl file

```
jmeter -g REST_API_Test_Plan.jtl -o report
```