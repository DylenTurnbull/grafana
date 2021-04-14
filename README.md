# Setting up Prometheus and Grafana

## nfs-client-provisioner

- Go to the nfs sub-directory and follow the read me instructions to deploy the nfs-client-provisioner


## Prometheus

- From the top menu bar select Apps
- Select the Launch button
- In the search field search for "prom"
- Locate the Prometheus option and select it
- From the screen caps below make the following config changes.
- Once complete click the Launch option

![Prometheus Config](/images/prom-config-1.png)

![Prometheus Config](/images/prom-config-2.png)

## Grafana

- From the top menu bar select Apps
- Select the Launch button
- In the search field search for "Graf"
- Locate the Grafana option and select it
- From the screen caps below make the following config changes.
- Once complete click the Launch option

![Prometheus Config](/images/graf-config-1.png)

![Prometheus Config](/images/graf-config-2.png)


## Accessing the Prometheus and Grafana sites

Prometheus
http://10.1.1.7:32322

Grafana
http://10.1.1.7:32323

**Login**: admin **Pass**: Same as UDF pattern

## Adding the Prometheus Data Source

From the left navigation bar locate the following option and select "Data Sources"

![Prometheus Config](/images/datasource.png)

Select Prometheus as the data source

![Prometheus Config](/images/prom-datasource.png)

Make the following changes to target the Prometheus data source.

![Prometheus Config](/images/prom-http.png)

Select Save and Test, you should get a green indicator saying it works.

![Prometheus Config](/images/save.png)

## Importing the KIC Grafana Dashboard

Navigate to the following menu and select Manage 

![Prometheus Config](/images/dashboard.png)

## Importing the NGINX Official KIC Grafana Dashboard

- Locate the KIC dashboard in the dash dir of this repo
- Select it in VSCode
- Do a select all on the contents of the NGINXPlusKIC-4-12-21.json file
- Copy and past it in to the large field in the Grafana window as seen below.
- Select load to complete the import.

![Prometheus Config](/images/load.png)

## Viewing the Dashboard

To view the dashboard follow the menu selections as seen below.

- Select the NGINX Plus Ingress Controller dashboard.

![Prometheus Config](/images/view.png)

## Finished

Now that the dash is imported feel free to have a look around and tinker about with the dash as well as the demo site it is tracking.