# Operational concepts

## Administration

### Configuration
The Portal can be configured using two methods:

### appsettings.json
If you build the Portal, you can modify the appsettings.json for each backend service, to individually configure to a certain extend. This file contains all possible config entries for the application.

### Helm Chart
The most relevant config properties are exposed as environment variables and must be set in the Helm chart so the application can run at all. Check the Portal Helm chart in Git for all available variables.

### DB Migration File
Static Data migration files provide a certain configuration possibility by adding or deleting static data records before the deployment. Be aware that touching static data files will always impact the application business process. It is suggested to always test the application with the planned changes carefully in INT before releasing to a productive env.

## Disaster-Recovery
Note: will be added soon

## Scaling
If the number of consumers raises, the IRS can be scaled up by using more resources for the Deployment Pod. Those resources can be used to utilize more parallel threads to handle Job execution.

## Clustering
Note: will be added soon

## Logging
The portal supports application and db logging. Details are stored here: https://github.com/catenax-ng/tx-portal-assets/blob/945546d91065b8870aa8f69ce94b48eac7a5ade2/docs/Technical%20Details/Auditing.md

## Monitoring
Note: Prometheus and Grafana are planned
