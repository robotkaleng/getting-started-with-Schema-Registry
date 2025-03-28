<div align="center" padding=25px>
    <img src="images/confluent.png" width=50% height=50%>
</div>

# <div align="center">Getting Started with Stream Processing</div>
## <div align="center">Lab Guide</div>

## **Agenda**
1. [Introduction to Stream Processing](https://developer.confluent.io/get-started/java/#introduction)
2. [Prerequisites](https://developer.confluent.io/get-started/java/#prerequisites)
3. [Create Your Project](https://developer.confluent.io/get-started/java/#create-project)
4. [Set Up Kafka](https://developer.confluent.io/get-started/java/#kafka-setup)
5. [Create Your First Topic](https://developer.confluent.io/get-started/java/#create-topic)
6. [Build Your Producer](https://developer.confluent.io/get-started/java/#build-producer)
7. [Build Your Consumer](https://developer.confluent.io/get-started/java/#build-consumer)
8. [Produce Events](https://developer.confluent.io/get-started/java/#produce-events)
9. [Consume Events](https://developer.confluent.io/get-started/java/#consume-events)

***

## **Architecture Diagram**

<div align="center">
    <img src="images/architecture.png" width=75% height=75%>
</div>

This workshop will be utilizing mongoDB Atlas, BigQuery, and Data Studio instances that are being managed by Confluent. You will not be able to access these instances outside of the workshop time. To test ksqlDB and connectors outside of the workshop, you can take a look at the ksqlDB [quickstart](https://docs.confluent.io/cloud/current/get-started/ksql.html) and fully-managed connectors [page](https://docs.confluent.io/cloud/current/connectors/index.html#kafka-connect-cloud).

***

## **Prerequisites**

1. Confluent Cloud Account
    * Sign-up for a Confluent Cloud account [here](https://www.confluent.io/confluent-cloud/tryfree/).
    * Once you have signed up and logged in, click on the menu icon at the upper right hand corner, click on “Billing & payment,” then enter payment details under “Payment details & contacts”.

    > **Note:** You will create resources during this workshop that will incur costs. When you sign up for a Confluent Cloud account, you will get free credits to use in Confluent Cloud. This will cover the cost of resources created during the workshop. More details on the specifics can be found [here](https://www.confluent.io/confluent-cloud/tryfree/).

1. Ports `443` and `9092` need to be open to the public internet for outbound traffic. To check, try accessing the following from your web browser:
    * portquiz.net:443
    * portquiz.net:9092

***

## **Objective**

In this workshop, you will learn how Confluent Cloud can enable you to quickly and easily stand up a streaming ETL pipeline. You will gain hands-on experience in building an end-to-end ETL pipeline, extracting & loading data from out-of-the-box source & target systems with connectors, transforming data in real-time with ksqlDB, and much more. By the end of the workshop, you will have a clear understanding of your upcoming ETL implementation, how to get started with Confluent Cloud, and the resources available to assist with development.

This workshop is ideal for those looking to build a foundation for data processing pipelines and ETL use cases with Confluent Cloud.

***

## **Steps Overview**

### 1. [Introduction to Stream Processing](https://developer.confluent.io/get-started/java/#introduction)

Start by understanding the basics of stream processing, Kafka, and how to integrate these into your applications.

### 2. [Prerequisites](https://developer.confluent.io/get-started/java/#prerequisites)

Ensure you have the required prerequisites in place for the tutorial, such as a Confluent Cloud account and open ports for necessary traffic.

### 3. [Create Your Project](https://developer.confluent.io/get-started/java/#create-project)

In this step, you'll create a Java project to interact with Confluent Cloud's Kafka services. You’ll set up the necessary dependencies and configurations.

### 4. [Set Up Kafka](https://developer.confluent.io/get-started/java/#kafka-setup)

Learn how to configure and set up Kafka in your Confluent Cloud account, including cluster selection and configuration.

### 5. [Create Your First Topic](https://developer.confluent.io/get-started/java/#create-topic)

Here, you'll create a Kafka topic in Confluent Cloud to start producing and consuming events.

### 6. [Build Your Producer](https://developer.confluent.io/get-started/java/#build-producer)

Develop your Kafka producer application in Java to send events to the Kafka topic created earlier.

### 7. [Build Your Consumer](https://developer.confluent.io/get-started/java/#build-consumer)

Next, you'll build a Kafka consumer in Java to consume events from the Kafka topic.

### 8. [Produce Events](https://developer.confluent.io/get-started/java/#produce-events)

Learn how to produce events from your producer application and send them to Kafka for processing.

### 9. [Consume Events](https://developer.confluent.io/get-started/java/#consume-events)

Finally, consume events from the Kafka topic in your consumer application and process the events.

***

## <a name="step-1"></a>Step 1: Introduction to Stream Processing

To start, familiarize yourself with the basics of stream processing and Kafka. Stream processing enables the real-time processing of data streams, while Kafka acts as the underlying messaging system that efficiently handles these streams.

Read more about the introduction to stream processing [here](https://developer.confluent.io/get-started/java/#introduction).

***

## <a name="step-2"></a>Step 2: Prerequisites

Before you proceed, ensure that you meet all the necessary prerequisites. This includes having a Confluent Cloud account and making sure that the required ports are open.

You can find the full list of prerequisites [here](https://developer.confluent.io/get-started/java/#prerequisites).

***

## <a name="step-3"></a>Step 3: Create Your Project

Create a Java project to interact with Kafka and Confluent Cloud. This step includes setting up your environment and dependencies.

You can follow the instructions for setting up your project [here](https://developer.confluent.io/get-started/java/#create-project).

***

## <a name="step-4"></a>Step 4: Set Up Kafka

Set up your Kafka environment in Confluent Cloud, create a cluster, and configure it for your use case.

Find detailed instructions on setting up Kafka [here](https://developer.confluent.io/get-started/java/#kafka-setup).

***

## <a name="step-5"></a>Step 5: Create Your First Topic

Create a Kafka topic to begin producing and consuming data. This is the first step in setting up your messaging system.

Learn how to create your first Kafka topic [here](https://developer.confluent.io/get-started/java/#create-topic).

***

## <a name="step-6"></a>Step 6: Build Your Producer

Create a Kafka producer to send events to the Kafka topic. This involves writing the Java code to send data to Kafka.

Find the step-by-step guide for building your producer [here](https://developer.confluent.io/get-started/java/#build-producer).

***

## <a name="step-7"></a>Step 7: Build Your Consumer

Develop a Kafka consumer to read events from the Kafka topic. This allows your application to process the incoming events.

Learn how to build your Kafka consumer [here](https://developer.confluent.io/get-started/java/#build-consumer).

***

## <a name="step-8"></a>Step 8: Produce Events

Produce events from your Kafka producer and observe how they appear in the topic.

Learn how to produce events [here](https://developer.confluent.io/get-started/java/#produce-events).

***

## <a name="step-9"></a>Step 9: Consume Events

Consume the events produced earlier in your Kafka consumer application.

Find instructions on how to consume events [here](https://developer.confluent.io/get-started/java/#consume-events).

***

## <a name="step-10"></a>Step 10: Clean Up Resources

Once you've completed the workshop, clean up your resources to prevent unnecessary charges.

For cleanup instructions, refer to the guide in your Confluent Cloud dashboard.

***

## <a name="confluent-resources-and-further-testing"></a>Confluent Resources and Further Testing

Here are some additional resources for further exploration:

* [Confluent Cloud Basics](https://docs.confluent.io/cloud/current/client-apps/cloud-basics.html)
* [Confluent Cloud Quickstart](https://docs.confluent.io/cloud/current/get-started/index.html)
* [ksqlDB Quickstart](https://docs.confluent.io/cloud/current/get-started/ksql.html)
* [Confluent Demos/Examples](https://docs.confluent.io/platform/current/tutorials/examples/ccloud/docs/ccloud-demos-overview.html)
* [ksqlDB Tutorials](https://kafka-tutorials.confluent.io/)
* [Confluent Hub Connectors](https://www.confluent.io/hub/)

