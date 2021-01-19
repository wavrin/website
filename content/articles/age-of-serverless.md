---
title: The Age of Serverless
description: The future is extremely bright for serverless technologies. It's nothing new, but the tools and options are continuing to expand.
alt: The Age of Serverless
timestamp: January 18, 2021
date:1/18/2021
---

The future is extremely bright for serverless technologies. As a consultant I am seeing accelerating adoption of them and I can't imagine this slowing down. Serverless isn't new, but the tools and options are continuing to expand.

One thing that surprised me is how long we've been using serverless technologies. [Amazon S3](https://aws.amazon.com/s3/) (Simple Storage Service) was launched in 2006. And yes, S3 is a serverless technology!

Serverless is a bit of an abstract term. There are servers involved, but as a developer you don't have to worry about them. You are completely abstracted away from the traditional duties of managing servers. Let someone else worry about that and focus on your business logic.

Here are some serverless options I'm excited about:

## Hosting
I've been using [AWS Amplify](https://aws.amazon.com/amplify/)for a few years to host so-called JAMSTACK sites. There are a lot of frameworks that can serve as static-site generators: [Gridsome](https://gridsome.org/), [NuxtJS](https://nuxtjs.org/), [Next.js](https://nextjs.org/) to name a few. In each case, these tools create a build that Amplify can host. Amplify can simply point to a Github repository and each time the code base is updated, Amplify will grab the code, rebuild, and deploy. No need to worry about scaling.

Amplify does a lot more than just host a static-generated site - something I will explore in a future article.

### GraphQL
[AWS AppSync](https://aws.amazon.com/appsync/) is a managed GraphQL API service. But I think it qualifies as serverless because it will scale automatically for you. You do not have to worry about the volume of API calls, as AppSync will scale up and down automatically.

### Database
Amazon RDS is a wonderful *managed service* for a database. But it's not a serverless option, because you do have to pick the size of the EC2 instance your database will run on (which introduces constraints like CPUs, RAM and network speed). You will have to worry about scaling yourself (increasing size of EC2 instance, for example). RDS makes this pretty easy, but for a truly serverless option you can go with [RDS Aurora Serverless](https://aws.amazon.com/rds/aurora/serverless/). This option will automatically scale up and down depending on your application's need.

### Glue for all of it
In this article I won't get into too many details about the [AWS Cloud Development Kit](https://aws.amazon.com/cdk/) (AWS CDK), but wanted to briefly mention it. "Infrastructure as Code" is so important, especially when dealing with so many different services. There are lots of options - if you are only working within AWS, you can use [CloudFormation](https://aws.amazon.com/cloudformation/); if you use multiple clouds (or just don't want to be locked into an AWS-specific tool) you can use[Terraform](https://www.terraform.io/). AWS CDK lets you define your application resources using your preferred programming language. The serverless technologies above can be managed from your codebase - which is pretty handy. AWS CDK will then create CloudForm templates - so if you them if needed. Again, AWS CDK can do a lot and deserves a future article.




