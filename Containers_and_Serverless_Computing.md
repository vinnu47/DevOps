## Docker Containers and Microsoftservices  

> Every VM/instance need an **operating system** which uses significant resources  
> A **container** includes all the code, settings and dependecies for running the application  
> Each container is **isolated** from other containers  
> Containes are very resource **efficient**  
> Containers **start** up very quickly  

![alt text](./Images/image10.png)  

- Docker utilizes containerization to package an application and its dependencies into a single container image
- Docker provides Docker Hub, a cloud-based registry service for sharing container images and automating workflows
- Containers are lightweight because they share the host system's kernel
- Docker is ideal for microservices architectures and building cloud-native applications  

## Cloud-Native Applications

![alt text](./Images/image11.png)

## Microservices: Attributes and Benefits

|   Microservices Attribute               |                             Microservices Benefit                                                            |
|:----------------------------------------|--------------------------------------------------------------------------------------------------------------|
| use of APIs                             | Easier integrations between application components; assists with lose coupling                               |
| Independently deployable blocks of code | Can be scaled and maintained independently                                                                   |
| Business-oriented architecture          | Development organized around business capabilities; teams may be cross-functional and services may be reused |
| Flexible use of technologies            | Each microservice can be written using different technologies (e.g. programming languages)                   |
| Speed and agility                       | Fast to deplo and update.Easy to include high availability and fault tolerance for each microservice         |

## Amazon ECS 

![alt text](./Images/image12.png)  

### Amazon ECS key Features  

- Serverless with AWS Fargate - managed for you and fully scalable 
- Fully managed container orchestration - control plane is managed for you  
- Docker support - run and manage Docket containers with integration into the Docker Compose CLI  
- Windows container support - ECS supports management of Windows containers  
- Elastic Load Balancing integration - distribute traffic across containers using ALB or NLB  
- Amazon ECS Anywhere- enables the use of Amazon ECS control plane to manage on-premises implementations  

### Amazon ECS Components
> cluster - logical grouping of tasks or services  
> Container instance - EC2 instance running the ECS agent  
> Task Definition - Blueprint that describes how a docker container should launch  
> Task - A running container using settings in a task definition  
> Image - A Docker image referenced in the task definition  
> Service - Defines long running tasks - can control task count with Auto Scaling and attach and ELB  

### Amazon ECS Images
- Containers are creaed from a read only template called an image which has the instructions for creating a Docker container  
- Images are built from a Dockerfile   
- Only Docker containers are supported on ECS  
- Images are stored in a registry such as DockerHub or Amazon Elastic Container Registry(ECR)  
- ECR is a manged AWS Docker registry service that is secure, scalable and reliable  
- ECR support private Docker repositories with resource-based permissions using AWS IAM in oder to access repositories and images  
- You can use the Docker CLI to push, pull and manage images  

### Amazon ECS Tasks and Task Definations
- A task definition is required to run Docker containers in Amazon ECS  
- A task defination is a text file in JSON fromat that describes one or more containers, up to maximum of 10  
- Task definitions use Docker images to launch containers  

### Launch Types -EC2 AND Fargate

![alt](./Images/image13.png)

### ECS and IAM Roles

![alt text](./Images/image14.png)

## Serverless Services

- With severless there are no instances to manage   
- You dont need to provision hardware  
- There is no management of operating systems of software  
- Capacity provisioning and patching is handled automatically  
- Provides automatic scaling and high availability  
- Can be very cheap!  

![alt text](./Images/image15.png)

### AWS Lambda

![alt text](./Images/image16.png)

- Languages - Lambda natively supports Java, Go, PowerShell, Node.js, C#, Python and Ruby code   

- Ececuting Role(IAM Role) - this role grants the function permissions to access AWS services and resources    

- Memory and Timeout - you can specify the amount of memory allocated to a function and the maximum executing time   

- Monitoring and Logging - integrates with Amazon CloudWatch  

### Lambda Function Invocation

- Lambda fucntions run in response to events from various AWS services or direct invocation from the AWS SDKs or API    

- Functions can invoked synchronously or asynchronsouly:  
 - with synchronous invocation, applications wait for the function to process the event and return a response  
 - with asynchronous invocation, Lambda queues the event for processing and returns a response immediately  
- Lambda scales horizontally by running multiple instances of a function in parallel, up to the concurrency limit  

### Lambda to an Amazon VPC

![alt](./Images/image17.png)

## Application Integration Services

### Event-Driven Architecture
![alt](./Images/image18.png)

### Amazon Simple Queue Service (SQS)
![alt text](./Images/image19.png)

### Amazon Simple Notification Service (SNS)
![alt text](./Images/image20.png)

### Amazon EventBridge
Amazon EventBridge is a serverless event bus that connects loosely coupled application components together  

### Application Integration Services Comparison

|  Service                    |   what it does                                                    | Example use cases                                                       |
|:----------------------------|-------------------------------------------------------------------| ------------------------------------------------------------------------|
| Simple Queue Service        | Messaging queue; store and forward patterns                       | Building distributed / decoupled application                            |
| Simple Notification Service | set up, operate, and send notifications from the cloud            | Send email notification when CloudWatch alarm is triggered              |
| Step Functions              | Coordination of AWS services with visual workflow                 | Oder processing workflows                                               |
| Amazon MQ                   | Message broker service for Apache Active MQ and RabbitMQ          | Need a message queue that supports industry standard APIs and protocols |
| Amazon EventBridge          | Serverless event bus for connecting applications and AWS services | Create event driven application                                         |

## Serverless Application with REST API
![alt text](./Images/image21.png)

### Rest API with Amazon API Gateway
![alt text](./Images/image22.png)

- A resource represents a path in your API  

- Methods are created within resources and represent client-facing interfaces by which the client calls the API to access back-end resorces  

![alt text](./Images/image23.png)

- Event Sources - supports events from AWS services, SaaS applications, and custom applications    
- Default and custome Event Buses - Offers a default bus for AWS events and supports creating custom buses for peronsal or third party app events  
- Event filtering and routing- Events can be filtered and routed to differnet targets based on content-based filtering rules  
- scalability and reliability - scales automatically with the number of events, handling millions of events per second  


