# cisco-telemetry-demo
Artifacts for sending Cisco Streaming Telemetry data into Splunk IMT

This provides a way to stream sample data for Cisco Streaming Telemetry into Splunk IMT.

## REQUIREMENTS
You must have Docker and Docker Compose installed.  This can be on your laptop or any host you like.

## USAGE GUIDE
Download docker-compose.yaml from this repo (or make a local copy of the repo if you like).  Edit the docker-compose.yaml file and paste in your Splunk IMT access token on the appropriate line.  Also, update the realm if you need.  Do NOT use quotation marks around the token.

Launch a terminal and cd into the directory with the docker-compose.yaml file, then type:
```docker-compose up```

The containers will download and start, and you will see their output on your screen. The data will be flowing into your Splunk IMT account.

## DASHBOARDS

Now...how to visualize the data in Splunk IMT? There are no built-in dashboards for this. I built a Dashboard Group that you can create in your account.  Start by downloading "Cisco Router.json" from this repo.

In your Splunk IMT account, go to the Dashboards page.  Then click on the big + sign in the upper right, select Import in the menu, then Dashboard Group.  It will prompt you to select a file.  Select the "Cisco Router.json" file.  It should import and create a group with two dashboards in it, pictured below.

![ss1](/images/ss1.png)
![ss2](/images/ss2.png)

You have the option to select from three routers named dr01, dr02, and dr03 at the top of each dashboard.

To explore all the metrics, click on Metrics at the top, then search on "cisco" as pictured below...

![ss3](/images/ss3.png)

The data could take a few minutes to appear on the first run since we have to create new MTS for all of it.  Also, the data is limited; that is, it does not represent all the data that you could possibly stream with Cisco.  The full scope of metrics that Cisco provides is vast.  This is more of a prototype to show it can be done, using some standard metrics.

I hope it is useful.  Enjoy!
