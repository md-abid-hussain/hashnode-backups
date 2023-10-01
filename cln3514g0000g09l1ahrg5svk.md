---
title: "12 Factor App methodology : Part 1"
seoTitle: "12 factor app methodology"
seoDescription: "Set of best practices for building modern applications."
datePublished: Thu Sep 28 2023 12:14:48 GMT+0000 (Coordinated Universal Time)
cuid: cln3514g0000g09l1ahrg5svk
slug: 12-factor-app-methodology-part-1
canonical: https://12factor.net/
tags: devops, kodekloud

---

I've decided to take advantage of KodeKloud's one-week free course access to learn about DevOps. So I decided that I should share whatever I learn and in this way I'll be able to make notes as well as write blog 😅

<hr>

### Why 12 factor app methodology 
In the past, provisioning a server for deploying our application was a cumbersome process. It would often take several days to get the server up and running. Once our app was hosted on that server, it became tightly coupled and dependent on it indefinitely. The code was written to run exclusively on that specific server. Additionally, scaling required us to allocate more resources to that server, further limiting our flexibility and agility.

Fast forward to today, we're in an era where SaaS startups experience user growth from hundreds to millions within a matter of months. Provisioning and hosting our app have become incredibly streamlined. Cloud providers such as GCP, AWS, and Azure can provision a server in a matter of minutes. The expected uptime for platforms is 99.99%, ensuring that the platform remains fully operational at all times. Consequently, we no longer need to bring down our application to scale or patch the server

To achieve this, we need to ensure that our application can run on any infrastructure without being tied to a specific setup. In simple terms, we aim to make our application <b>portable</b>, allowing us to run it anywhere without needing to modify the source code.

In order to achieve this applications needs to develop keeping certain principle in mind. About a decade ago engineers from <a href="https://www.heroku.com/">heroku</a> (a cloud provider) put together 12 factor to create such application which is <a href="https://12factor.net/"> 12 Factor App</a>

<hr>

### List of 12 factors
<ol>
<li><b>Codebase :</b> Having one codebase</li>
<li><b>Dependencies :</b> Declare and isolate dependencies</li>
<li><b>Config :</b> Store config in the environment</li>
<li><b>Backing services :</b> To treat backing services as attached resources</li>
<li><b>Build, run, release :</b> Separate build and run stages</li>
<li><b>Processes :</b> Execute the app as one or more stateless processes</li>
<li><b>Port Binding :</b> Export services via port binding</li>
<li><b>Concurrency :</b> Scale out via process model</li>
<li><b>Disposability :</b> Fast startup and graceful shut down</li>
<li><b>Dev/prod parity :</b> Keeping development and production stage as similar as possible</li>
<li><b>Logs :</b> Treat logs as event stream</li>
<li><b>Admin Processes :</b> Running admin and management task as one of the processes</li>
</ol>
