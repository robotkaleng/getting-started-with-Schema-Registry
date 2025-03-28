<div align="center" padding=25px>
    <img src="images/confluent.png" width=50% height=50%>
</div>

# <div align="center">Getting Started with Kafka in Java on Confluent Cloud</div>
## <div align="center">Lab Guide</div>

## **Agenda**
1. [Introduction to Kafka and Java](#step-1)
1. [Prerequisites for Setting Up](#step-2)
1. [Create a Confluent Cloud Account and Cluster](#step-3)
1. [Create a New Java Project](#step-4)
1. [Set Up Kafka Cluster on Confluent Cloud](#step-5)
1. [Create Kafka Topic on Confluent Cloud](#step-6)
1. [Build a Kafka Producer](#step-7)
1. [Build a Kafka Consumer](#step-8)
1. [Produce Events to Kafka](#step-9)
1. [Consume Events from Kafka](#step-10)

***

## **Prerequisites**

Before starting, make sure you have the following:

1. **Java 8+** installed on your system.
2. **Apache Maven** installed for building Java projects.
3. An **IDE** (e.g., IntelliJ IDEA, Eclipse) to write and run your Java code.
4. Access to **Confluent Cloud**.

For details on setting up these prerequisites, please refer to the [prerequisites section](https://developer.confluent.io/get-started/java/#prerequisites).

***

## **Objective**

In this guide, you will learn how to set up a simple Kafka producer and consumer in Java using Confluent Cloud. You'll go through the process of creating a Kafka project, setting up Kafka in Confluent Cloud, and using the producer and consumer APIs to send and receive messages.

---

## <a name="step-1"></a>Step 1: Introduction to Kafka and Java

Kafka is a distributed event streaming platform used to build real-time data pipelines and streaming applications. It can handle trillions of events a day. In this step, you’ll learn the basics of Kafka and how it integrates with Java to build stream-processing applications.

You can read a detailed introduction to Kafka and Java in the [documentation here](https://developer.confluent.io/get-started/java/#introduction).

---

## <a name="step-2"></a>Step 2: Prerequisites for Setting Up

Before starting to write Java code with Kafka, make sure you have the following prerequisites:

- **Java 8+**: Ensure you have Java 8 or higher installed on your system.
- **Apache Maven**: A build automation tool that will help manage dependencies.
- **Confluent Cloud Account**: You will need a Confluent Cloud account to create and manage Kafka clusters.

For more information on the setup process, check out the [prerequisites section](https://developer.confluent.io/get-started/java/#prerequisites).

---

## <a name="step-3"></a>Step 3: Create a Confluent Cloud Account and Cluster

To begin working with Kafka on Confluent Cloud, you first need to sign up for an account and create a cluster.

1. **Sign Up for Confluent Cloud:**
    - Go to [Confluent Cloud sign-up page](https://www.confluent.io/confluent-cloud/tryfree/).
    - Sign up for a new account or log in to your existing account.
    - You will receive **free credits** upon signing up, which you can use during this tutorial.

2. **Create a Cluster in Confluent Cloud:**
    - Log into Confluent Cloud at [confluent.cloud](https://confluent.cloud).
    - In the top-right corner, click **+ Add Environment** to create a new environment (or use the default environment).
    - After selecting an environment, click **Create Cluster**.
    - Choose **Basic** cluster type for development purposes.
    - Select your preferred cloud provider (AWS, GCP, or Azure) and region.
    - Name your cluster and click **Launch Cluster**.
    - Wait for the cluster to be ready. This might take a few minutes.

3. **Obtain Connection Details:**
    - Once your cluster is set up, navigate to the **Cluster** page in Confluent Cloud and note down the **bootstrap server URL** and **API key pair** that you will use to configure your producer and consumer.

For detailed instructions, visit the [Kafka setup guide](https://developer.confluent.io/get-started/java/#kafka-setup).

---

## <a name="step-4"></a>Step 4: Create a New Java Project

To start using Kafka in Java, create a new Maven-based Java project. This project will include all the necessary dependencies for Kafka.

1. Open your IDE and create a new **Maven project**.
2. Add the required dependencies for Kafka in the `pom.xml` file. You can find the necessary configuration and examples in the [Create Project guide](https://developer.confluent.io/get-started/java/#create-project).

---

## <a name="step-5"></a>Step 5: Set Up Kafka Cluster on Confluent Cloud

After creating your Kafka cluster in Confluent Cloud, you need to set it up by creating topics and configuring your producer and consumer to connect to the cluster.

1. In Confluent Cloud, navigate to the **Cluster** page.
2. Under the **Topics** section, create a new topic called `my-topic`.
    - Click **Create Topic** and follow the prompts to set up your topic.
    - Set the number of partitions and replication factor according to your requirements.

For detailed instructions on creating and managing topics, visit the [Create Topic guide](https://developer.confluent.io/get-started/java/#create-topic).

---

## <a name="step-6"></a>Step 6: Create Kafka Topic on Confluent Cloud

Kafka topics are logical channels where data is written and read. You need to create a topic in Confluent Cloud before sending or receiving messages.

To create a topic in Confluent Cloud:

1. Go to the **Topics** section of your cluster in Confluent Cloud.
2. Click **Create Topic**, give it a name (e.g., `my-topic`), and specify the number of partitions.
3. Click **Create** and wait for the topic to be ready.

---

## <a name="step-7"></a>Step 7: Build a Kafka Producer

A Kafka producer sends data to a Kafka topic. The producer sends records to a Kafka broker, which is then stored in the corresponding topic.

Follow the instructions in the [Build Producer guide](https://developer.confluent.io/get-started/java/#build-producer) to write a simple Kafka producer in Java. You will learn how to configure the producer to connect to your Confluent Cloud Kafka cluster and send messages to the `my-topic` topic.

---

## <a name="step-8"></a>Step 8: Build a Kafka Consumer

A Kafka consumer reads data from Kafka topics. The consumer subscribes to topics and reads the data in the order it was produced.

To build a Kafka consumer, follow the guide in the [Build Consumer documentation](https://developer.confluent.io/get-started/java/#build-consumer). Here, you'll learn how to configure the consumer to connect to your Confluent Cloud Kafka cluster and read messages from the `my-topic` topic.

---

## <a name="step-9"></a>Step 9: Produce Events to Kafka

Now that you’ve set up your producer, it’s time to start producing events to Kafka. In this step, you'll send records containing events to your Kafka topic.

For step-by-step instructions on how to produce events to Kafka using the producer you built, refer to the [Produce Events guide](https://developer.confluent.io/get-started/java/#produce-events).

---

## <a name="step-10"></a>Step 10: Consume Events from Kafka

In this final step, you'll set up the consumer to read the events you produced to Kafka. The consumer will continuously poll Kafka for new events and process them as they arrive.

To learn how to consume events from Kafka, check out the [Consume Events guide](https://developer.confluent.io/get-started/java/#consume-events).

---

## **Conclusion**

Congratulations! You've successfully set up a Kafka producer and consumer in Java using Confluent Cloud. You now have a basic understanding of how to interact with Kafka using the Java programming language and Confluent Cloud.

For further learning, you can explore additional Kafka features like stream processing with Kafka Streams, connectors, and more advanced configurations. The Confluent documentation offers a wealth of resources to help you expand your knowledge and build more sophisticated applications.

---
