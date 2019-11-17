---
title: "Ingest data to Elasticsearch"
chapter: false
weight: 30
---

1. Navigate to the `main` method of the `ProcessTaxiStream` class and run it. However, as soon as it has started to execute, you can terminate it again by clicking the red square.

1. Edit the runtime parameters of the `main` method by choosing **Edit Configurations**

	![](/images/intellij-9-edit-configuration.png)

1. Under **Program arguments**, enter `--ElasticsearchEndpoint` followed by the **ElasticsearchEndpoint** that you have noted earlier from the Elasticsearch Service console

	![](/images/intellij-10-configuration-details.png)

1. Confirm with **OK** and execute the program again by clicking on the green arrow

1. Navigate to the Dashboard in Kibana and click on **nyc-tlc-dashboard** to view the visualization of the data generated by the Flink application

	![](/images/kibana-5-visualizatio-partial.png)

	{{% notice info %}}
If you cannot see any new data in the visualization, you may need to adapt the time range in the upper left corner of the Kibana dashboard. The output of the Java producer application will tell you the time of events that are currently ingested into the Kinesis stream.
	{{% /notice %}}

1. Once you have verified that the data generated by the Flink application is visualized by Kibana, stop the Flink application in IntelliJ. Also terminate the Java producer application that is ingesting events into the Kinesis stream by navigating to the Terminal in IntelliJ and pressing **Ctrl-C**.