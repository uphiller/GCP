#google-fluentd이용한 에러수집

This sample demonstrates how to use Stackdriver on Google Compute Engine

Running on Compute Engine

Create a compute instance on the Google Cloud Platform Developer's Console

SSH into the instance you created

Follow the instructions to Install the Stackdriver Logging Agent

#instructions
Update packages and install required packages sudo apt-get update && sudo apt-get install git-core openjdk-8-jdk maven

curl -sSO https://dl.google.com/cloudagents/install-logging-agent.sh

sha256sum install-logging-agent.sh

sudo bash install-logging-agent.sh

sudo rm install-logging-agent.sh

vi /etc/google-fluentd/config.d/forward.conf

<source>
  type forward
  port 24224
</source>
Restart the logging agent

sudo service google-fluentd restart

#sample source
https://github.com/GoogleCloudPlatform/java-docs-samples/tree/master/compute/error-reporting

#google docs
https://cloud.google.com/error-reporting/docs/quickstart


