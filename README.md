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

![ss1](/images/Screen Shot 2021-01-26 at 11.59.34 AM.png)
