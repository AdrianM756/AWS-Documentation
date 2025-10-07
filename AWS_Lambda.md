# What is AWS Lambda?

AWS Lambda is a **serverless, event-driven compute service** provided by Amazon Web Services (AWS). It allows you to run code for virtually any type of application or backend service without provisioning or managing servers.

## Key Concepts

* **Serverless:** You don't have to worry about the underlying infrastructure (servers, operating systems, patches, scaling). AWS automatically manages all of that for you.
* **Event-Driven:** Lambda functions are typically triggered by **events**. An event could be:
    * An image uploaded to an **Amazon S3** bucket.
    * A record added to an **Amazon DynamoDB** table.
    * An HTTP request via **Amazon API Gateway**.
    * A scheduled event from **Amazon EventBridge**.
* **Functions (Code):** Your code, written in a supported language (like Python, Node.js, Java, etc.), is packaged and uploaded to Lambda as a "function." This function is the core unit of execution.
* **Execution Environment:** When an event occurs, Lambda spins up a temporary execution environment to run your function, handles the request, and then shuts down the environment when it's finished.

## How it Works

1.  **Upload Code:** You package your code and its dependencies into a deployment package (ZIP file or container image) and upload it to AWS Lambda.
2.  **Define Trigger:** You specify which AWS service or event will invoke your function.
3.  **Execute:** When the trigger's event occurs, Lambda automatically:
    * Launches an execution environment.
    * Runs your code.
    * Scales out instantly to handle peak load (running multiple copies of your function concurrently).
4.  **Pay Per Use:** You are billed only for the time your code is running, measured in milliseconds, and the number of requests (invocations).

## Primary Benefits

| Benefit | Description |
| :--- | :--- |
| **No Server Management** | AWS handles all server administration, operating system updates, and scaling. |
| **Automatic Scaling** | Lambda automatically and precisely scales your application to meet demand. |
| **Cost Optimization** | You pay only for the requests served and the compute time consumed, making it highly cost-effective for variable workloads. |
| **High Availability** | Your functions run on highly available and redundant infrastructure. |

***

*The content above represents the information about AWS Lambda in standard Markdown format.*
