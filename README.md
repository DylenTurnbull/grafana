# Setting up Prometheus and Grafana

## nfs-client-provisioner

- Go to the nfs sub-directory and follow the read me instructions to deploy the nfs-client-provisioner


## Prometheus

- From the top menu bar select Apps
- Select the Launch button
- In the search field search from "prom"
- Locate the Prometheus option and select it
- From the screen games below make the following - - - - config changes.
- Once complete click the Launch option

![Prometheus Config](/images/prom-config-1.png)

![Prometheus Config](/images/prom-config-2.png)

## Grafana

- From the top menu bar select Apps
- Select the Launch button
- In the search field search from "Graf"
- Locate the Grafana option and select it
- From the screen games below make the following - - - - config changes.
- Once complete click the Launch option

![Prometheus Config](/images/graf-config-1.png)

![Prometheus Config](/images/graf-config-2.png)


## Accessing the Prometheus and Grafana sites

Prometheus
http://10.1.1.7:32322

Grafana
http://10.1.1.7:32323

login: admin
pass: **Same as UDF pattern**

## Adding the Prometheus Datasource

From the left navigation bar locate the following option and select "datasource"

![Prometheus Config](/images/datasource.png)

Select Prometheus as the data source

![Prometheus Config](/images/prom-datasource.png)

make the following cahnges to targe the Prometheus data source.

![Prometheus Config](/images/prom-http.png)

Select Save and Test

![Prometheus Config](/images/save.png)

## Importing the KIC Grafana Dashboard

Navigate to the following menu and select Manage 

![Prometheus Config](/images/dashboard.png)

Locate the KIC dashboard in the dashboard dir of this repo select it in VSCode
Do a select all on the contents of the .jason file
Copy and past it in to the large field in the Grafana window.
