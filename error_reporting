Stackdriver sample for Google Compute Engine

This sample demonstrates how to use Stackdriver on Google Compute Engine

Running on Compute Engine

Create a compute instance on the Google Cloud Platform Developer's Console
SSH into the instance you created
Update packages and install required packages sudo apt-get update && sudo apt-get install git-core openjdk-8-jdk maven
Follow the instructions to Install the Stackdriver Logging Agent
Create /etc/google-fluentd/config.d/forward.conf and add

<source>
  type forward
  port 24224
</source>
Restart the logging agent

sudo service google-fluentd restart

Clone the repo

git clone https://github.com/GoogleCloudPlatform/java-docs-samples.git

Navigate to the Stackdriver sample folder

java-docs-samples/compute/stackdriver

Make sure that openjdk 8 is the selected java version

sudo update-alternatives --config java

Use maven to package the class as a jar

mvn clean package

Switch to the target folder and execute the jar file

java -jar compute-stackdriver-1.0-SNAPSHOT-jar-with-dependencies.jar

On the Developer's Console, navigate to Stackdriver Error Reporting and verify that the sample error was logged.
