# Redis Playground 
## An observable dev environment for understanding Redis

This is a `.Net Core 3.1` app using the `StackExchange.Redis` client library to communicate with `redis` and instrumented with `OpenTelemetry` + `Jaeger` for traces and `Prometheus` + `Grafana` for metrics all running in `docker-compose`.

## Getting Started

 - Run `./start.sh` to run the `docker-compose` and start the app.
 - Redis.Playground.App
   - http://localhost:5000/Queue/Push/{queueName}/{messageCount}
   - http://localhost:5000/Queue/Size/{queueName}
 - Grafana - http://localhost:3000 (admin/admin)
   - Import the following dashboards
     - [Redis Dashboard for Prometheus Redis Exporter 1.x](https://grafana.com/grafana/dashboards/11692)
     - [prometheus-net - AspNetCore summary](https://grafana.com/grafana/dashboards/10427)
     - [prometheus-net.DotNetRuntime CLR summary](https://grafana.com/grafana/dashboards/13399)
     - [ASP.NET Core - controller summary](https://grafana.com/grafana/dashboards/10915)
     - [Docker - docker-compose containers summary](https://grafana.com/grafana/dashboards/11467)
 - Jaeger UI - http://localhost:16686

## 150+ Talks on Redis
 - ### Use Cases
   - #### TL;DR
     - [Redis: Swiss army knife](https://www.youtube.com/watch?v=Pf47bR94Brw)
   - #### Caching
     - [Techniques to Improve Cache Speed](https://www.youtube.com/watch?v=QkUz2_kRV9g)
     - [Leveraging Redis 6 Tracking for Awesome Client-Side Caching - RedisConf 2020](https://www.youtube.com/watch?v=fcgFT1Nca14)
     - [Techniques for Synchronizing In-Memory Caches with Redis](https://www.youtube.com/watch?v=kliQLwSikO4)
     - [Increase Application Performance with SQL Auto Caching; No Code Changes - RedisConf 2018](https://www.youtube.com/watch?v=coq4rHW1Iu8)
     - [Why Your MySQL Needs Redis](https://www.youtube.com/watch?v=_4HwUVNl9Nc)
     - [Declarative Caching with Postgres and Redis](https://www.youtube.com/watch?v=IID2LQVztIM)
     - [Improve Cache Speed at Scale - RedisConf 2020](https://www.youtube.com/watch?v=mPg20ykAFU4)
     - [Scaling applications with Azure Redis Cache and Machine Learning](https://www.youtube.com/watch?v=NgERP5g_Nuw)
     - [Scaling SQL Write-Master Database Clusters](https://www.youtube.com/watch?v=ElP4EoYhROE)
   - #### Session Management
     - [Creating a Highly Available Persistent Session Management Service - RedisConf 2020](https://www.youtube.com/watch?v=Bnq_U-eGOwc)
     - [Session Management - Redis Labs](https://www.youtube.com/watch?v=uJePLpfPsug)
     - [The Life of a User Session - Redis Day 2019](https://www.youtube.com/watch?v=a2aFhWYa-1I)
   - #### Rate Limiting
     - [Rate-Limiting 30M Requests a Day - Redis Day Bengaluru 2020](https://www.youtube.com/watch?v=rZ8mhTMDoCU)
     - [Protecting your API with Redis](https://www.youtube.com/watch?v=HnSb8DFU5UA)
     - [Rate Limiting with Redis](https://www.youtube.com/watch?v=CRGPbCbRTHA)
     - [Rate limiting/monitoring with Redis - 2014](https://www.youtube.com/watch?v=lOOBH9fAfPs)
     - [Rate limiting APIs with Redis + Express.js](https://www.youtube.com/watch?v=_DqfiW08HkA)
     - [Throttling requests before they hit your application](https://www.youtube.com/watch?v=MHYHbGPzZtw)
     - [High Volume Ratelimiting with Redis](https://www.youtube.com/watch?v=p5-mS_L6S3Y)
     - [API Rate Limits with Spring Boot and Redis](https://www.youtube.com/watch?v=MHxRdXLsZkg)
     - [How to Protect Your APIs with Rate Limiting and Metering](https://www.youtube.com/watch?v=4_erD-HKu3o)
     - [Approaches for application request throttling - DotNext](https://www.youtube.com/watch?v=Q53eR7mFsRo)
   - #### Queues / Messaging
     - [Redis as a Message Bus](https://www.youtube.com/watch?v=qB474R-JG14)
     - [Build a Message Bus with Redis Streams and FastAPI](https://www.youtube.com/watch?v=LHOjW42-A40)
     - [Building Scalable, Distributed Job Queues with Redis - RakuConf 2012](https://www.youtube.com/watch?v=ztyyn7hmcJo)
     - [Delayed Message Processing with Redis Streams](https://www.youtube.com/watch?v=hkGYRYe5NE8)
     - [Distributed Queue using Redis - DSConf 2020](https://www.youtube.com/watch?v=6mkc8XXaS-I)
     - [Fail Safe Starvation Free Durable Priority Queues in Redis](https://www.youtube.com/watch?v=TyqMM8pGWc0)
     - [Resilient Testing At Scale Using Redis Queues to Manage Concurrency](https://www.youtube.com/watch?v=S7oVdnKZlG8)
     - [Redis Pub/Sub for Fast Data Ingest](https://www.youtube.com/watch?v=Zwg1C9u_3K8)
     - [High-performance messaging with Go and Redis](https://www.youtube.com/watch?v=x5__QAIxQZw)
     - [Cancellable Timeout Queues, A Use Pattern](https://www.youtube.com/watch?v=tcVAqmpdm1I)
     - [Increasing Message Delivery Rates with Redis](https://www.youtube.com/watch?v=_XcN0e43dHM)
   - #### Analytics / AI
     - [Redis Analytics Use Cases](https://www.youtube.com/watch?v=D06iijqAX1A)
     - [Real Time Log Analytics Using Probabilistic Data Structures in Redis](https://www.youtube.com/watch?v=ord1F0azUcQ)
     - [How to Use Bloom Filters in Redis](https://www.youtube.com/watch?v=Z9_wrhdbSC4)
     - [Inline Analytics Redis Fraud Mitigation](https://www.youtube.com/watch?v=UJk63asfgqA)
     - [Efficient analytics with Redis Bitmaps](https://www.youtube.com/watch?v=a-BtWlU55kk)
     - [Redis as a Time Series Data Store](https://www.youtube.com/watch?v=j9-QIwJ0woE)
     - [Making Real Time Predictive Decisions with Redis](https://www.youtube.com/watch?v=PzEWggJqAjA)
     - [Real-Time Redis Deep-Learned Detection at the Edge - RedisConf 2020](https://www.youtube.com/watch?v=lDYnJsX9v50)
     - [Using Redis for Schema Detection](https://www.youtube.com/watch?v=0525hq2uWlk)
     - [Identifying Fraudulent Online Behavior](https://www.youtube.com/watch?v=y6vY2-7UOZk)
   - #### Other
     - [Building Highly Concurrent, Low Latency Gaming System - Redis Day London 2019](https://www.youtube.com/watch?v=5jwuDM6Z3F8)
     - [Using Redis and RediSearch Module to Store & Search Volatile Data - RedisConf 2017](https://www.youtube.com/watch?v=Zsz1FhLQ2cM)
     - [Unorthodox Redis Use Cases](https://www.youtube.com/watch?v=u-p3Q1Uts1o)
   - #### Microservices / Application Architecture
     - [Implementation patterns to leverage Redis to turbo charge existing Legacy applications](https://www.youtube.com/watch?v=xQJ58dDPYL4) 
     - [Microservices and Redis: A Match made in Heaven](https://www.youtube.com/watch?v=wfyq_-tWkiY)
     - [Where is my cache? Architectural patterns for caching microservices by example](https://www.youtube.com/watch?v=BC6NvHssquI)
     - [Building Lightweight Microservices Using Redis](https://www.youtube.com/watch?v=z25CPqJMFUk)
     - [Event Driven Microservices with Event Sourcing and Redis](https://www.youtube.com/watch?v=vBb9Diz-zaQ)
     - [Redis Streams for Event-Driven Microservices](https://www.youtube.com/watch?v=QjJeKwB4_8o)
     - [Building Lightweight Microservices with Redis and Hydra](https://www.youtube.com/watch?v=zv-jmSeV9ok)
     - [Using Redis Streams to Build Event Driven Microservices and User Interface](https://www.youtube.com/watch?v=30Odhss1xVA)
     - [Using Redis Streams to Build More Resilient Services - Redis Day London 2019](https://www.youtube.com/watch?v=2z0T5djeaKY)
     - [Microservices and Redis - RedisConf 2017](https://www.youtube.com/watch?v=CykUle8UUqk)
     - [Interview: Chris Richardson Of Microservices.io](https://www.youtube.com/watch?v=q5Z8-cwGBXQ)
     - [Common Redis Use Cases for Cloud-Native Apps and Microservices](https://www.youtube.com/watch?v=v8XubeXz9Uk)
     - [Microservices Architecture in the Real World](https://www.youtube.com/watch?v=VQAaeCIe8yQ)
 - ### Redis Concepts / Internals
   - #### Data Structures
     - [Redis Data Structures for Non-Redis Users](https://www.youtube.com/watch?v=ELk_W9BBTDU)
     - [Intro to Redis Commands and Data Structures](https://www.youtube.com/watch?v=Z04lIh23yuI)
     - [Intro to Redis Data Structures and Pub/Sub vs Redis Streams](https://www.youtube.com/watch?v=O_jNJ32s6x8)
     - [Redis Hashes Explained](https://www.youtube.com/watch?v=-agsJUihrWw)
     - [Redis Lists Explained](https://www.youtube.com/watch?v=202yxNkUJyE)
     - [Redis Sets Explained](https://www.youtube.com/watch?v=6Pjz819sT7M)
     - [Redis Sorted Sets Explained](https://www.youtube.com/watch?v=XqSK-4oEoAc)
     - [Redis Bitmaps Explained](https://www.youtube.com/watch?v=5fmyc5lkwD4)
     - [Redis HyperLogLog Explained](https://www.youtube.com/watch?v=UAL2dxl1fsE)
     - [Implementing a New Data Structure for Redis](https://www.youtube.com/watch?v=pmxaztRsoF4)
   - #### Modules
     - ##### Redis Streams 
       - [Redis Streams - Redis Day TLV 2018](https://www.youtube.com/watch?v=qXEyuUxQXZM)
     - ##### RediSearch
       - [Integrating Redis with ElasticSearch](https://www.youtube.com/watch?v=2mYe4qjn304) 
       - [Amazing User Experiences with Redis and RediSearch - RedisConf 2018](https://www.youtube.com/watch?v=B_BVmJ90X8Q)
       - [Add Real-Time Full-Text Search to Your Web Site with RediSearch](https://www.youtube.com/watch?v=tfDdoVg_jXY)
       - [RediSearch Aggregation Capabilities](https://www.youtube.com/watch?v=UHZ_VFoRHcQ)
       - [Getting Started With GeoCoding With Redis](https://www.youtube.com/watch?v=0dvR9I9kK9g)
     - ##### Redis Gears 
       - [RedisGears GA](https://www.youtube.com/watch?v=J4clHQJScZQ)
     - ##### RedisAI 
       - [RedisAI in Production](https://www.youtube.com/watch?v=20Aj12ovASE)
     - ##### RedisJSON 
       - [JSON in Redis: When to use RedisJSON - Redis Day Seattle 2020](https://www.youtube.com/watch?v=zpgGkxL6ozU)
       - [ReJSON = {"id": "old dog", "activity": "new trick"}](https://www.youtube.com/watch?v=NLRbq2FtcIk)
     - ##### RedisGraph 
       - [RedisGraph 2.2: The Fastest Way to Query Your Highly Connected Data in Redis](https://www.youtube.com/watch?v=JNpHba2kRGM)
       - [A Practical Introduction to RedisGraph](https://www.youtube.com/watch?v=aGHALjV6JGc)
       - [Deep Dive into RedisGraph - RedisConf 2019](https://www.youtube.com/watch?v=4KS2MRccQX4)
       - [Redis Graph - Redis Day TLV 2018](https://www.youtube.com/watch?v=HpEa2cftbnc)
       - [RedisGraph and it's use cases](https://www.youtube.com/watch?v=d3upsk6Ra18)
     - ##### RedisTimeSeries 
       - [Intro to RedisTimeSeries](https://www.youtube.com/watch?v=rXynFOrrd-Q)
       - [Time Series Data in Real Time with Redis Time Series Module - RedisConf 2018](https://www.youtube.com/watch?v=Y2VbxNOYzVE)
     - ##### Extending Redis 
       - [Redis Lua Scripts](https://www.youtube.com/watch?v=eReTl8NhHCs)
       - [Writing Redis Modules in Rust](https://www.youtube.com/watch?v=c1E8jxWVfoI)
       - [Extend Redis With Modules](https://www.youtube.com/watch?v=EglSYFodaqw)
       - [Josiah Carlson on Redis](https://www.youtube.com/watch?v=exPureoGGPs)
   - #### Concepts / History
     - [Architecture of Redis](https://youtu.be/EUAGY5HTPYA?t=986)
     - [The Evolution of Redis Key Expiration Algorithms](https://www.youtube.com/watch?v=SyQTG0hXPxY)
     - [Anatomy of a Redis Command](https://www.youtube.com/watch?v=rgE7tZ1yH80)
     - [Designing a Redis Client for Humans](https://www.youtube.com/watch?v=zMGYz5YKYts)
     - [History of Redis Replication and Future Prospects](https://www.youtube.com/watch?v=T1htSDCYMPY)
     - [The Design of Redis Streams - Antirez](https://www.youtube.com/watch?v=Ty1rQuRJijk)
     - [Lessons Learned Running The Redis Open Source Project For 8 Years - Antirez](https://www.youtube.com/watch?v=seLT7M3OAgk)
     - [Redis: Client side caching "broadcasting mode"](https://www.youtube.com/watch?v=TW9uFIJ9xkc)
     - [A Brief History of Encrypting Your Redis Traffic](https://www.youtube.com/watch?v=ula3JoQXbtE)
     - [What Happens When Redis Runs Out of Memory](https://www.youtube.com/watch?v=W8IEzoxRMz4)
   - #### Optimization 
     - [Redis Memory Optimization](https://www.youtube.com/watch?v=0u5WqD0Q8z4)
     - [Redis Memory Optimization - RedisConf 2018](https://www.youtube.com/watch?v=h7Onll-9fuM)
   - #### Distributed Caching System Design Concepts
     - [Redis system design | Distributed cache System design](https://www.youtube.com/watch?v=DUbEgNw-F9c)
     - [Caching Architectures | Microservices Caching Patterns | System Design Primer](https://www.youtube.com/watch?v=0x-ZV_vP73k)
     - [What is Distributed Caching? Explained with Redis!](https://www.youtube.com/watch?v=U3RkDLtS7uY)  
 - ### Redis In Production
   - #### War Stories
     - [Anti-patterns with Redis](https://www.youtube.com/watch?v=V532pU-7zW8)
     - [Learn Redis the hard way... in production - DEVit 2017](https://www.youtube.com/watch?v=PHsx0Fy-knA)
     - [Redis: Going Beyond Simple Failover - NYC Redis Meetup 2014](https://www.youtube.com/watch?v=mNj97o513Ys)
     - [Processing 60 million messages a day using Redis: Lessons from the trenches](https://www.youtube.com/watch?v=pqB-PbxHAyg)
     - [Troubleshooting Redis](https://www.youtube.com/watch?v=7ydU97NOZb4)
     - [Redis Networking Nerd Down](https://www.youtube.com/watch?v=3h316lNYMyQ)
     - [Redis is Dead Long live Redis!](https://www.youtube.com/watch?v=NymIgA7Wa78)
     - [Evolving Your Distributed Cache In A Continuous Delivery World](https://www.youtube.com/watch?v=Dcr6vVHpgWI)
   - #### High Availability / Scaling
     - [Build and Deploy Containerized Redis Cache for High Availability and Performance](https://www.youtube.com/watch?v=LMphQpep3CQ)
     - [Scaling Redis To 1M Ops/Sec](https://www.youtube.com/watch?v=55TFuBMFWns)
     - [Meeting Service Level Objectives at Scale with HAProxy and Redis](https://www.youtube.com/watch?v=h8blgoqZEIM)
     - [Scaling Your Redis Workloads with Redis Cluster - AWS Online Tech Talks](https://www.youtube.com/watch?v=3Ovx5vJ17ws)
     - [App Sharded Redis w/Sentinel vs Redis Cluster - RedisConf 2019](https://www.youtube.com/watch?v=dQo8Pb7KTrg)
     - [Multi Master Redis: A Deep Dive - RedisConf 2017](https://www.youtube.com/watch?v=9QChf0jIFgY)
     - [Deep Dive into Redis Replication - RedisConf 2019](https://www.youtube.com/watch?v=esbRryo0Ty8)
   - #### Case Studies 
     - [Airbnb's Journey from Self-Managed Redis to ElastiCache for Redis - AWS re:Invent 2018](https://www.youtube.com/watch?v=eyd_8efUCwM)
     - [Redis Cluster at Flickr Yahoo! - RedisConf 2017](https://www.youtube.com/watch?v=L5WSTbPpB_M)
     - [Redis at LINE, 25 Billion Messages Per Day - RedisConf 2018](https://www.youtube.com/watch?v=IxTUXuoIWro)
     - [Monitoring and Scaling Redis at DataDog](https://www.youtube.com/watch?v=7tL2Eoiab7U)
     - [Preventing Cache Stampede with Redis and Xfetch](https://www.youtube.com/watch?v=1sKn4gWesTw)
     - [How Shopify is Scaling Up Its Redis Message Queues](https://www.youtube.com/watch?v=hu6Q6s0432A)
     - [Operationalizing Redis at Scale at Square](https://www.youtube.com/watch?v=8nyJPpbt50I)
     - [Redis at Lyft: 1,000 Instances](https://www.youtube.com/watch?v=U4WspAKekqM)
     - [Beyond Sharding @Lyft - RedisConf 2020](https://www.youtube.com/watch?v=b9SiLhF9GaU)
     - [Using Redis at Scale at Twitter - RedisConf 2017](https://www.youtube.com/watch?v=QznaOSk20nU)
     - [Redis in a Multi Tenant Environment](https://www.youtube.com/watch?v=qCBoFTjUgZw)
     - [How Roblox Keeps Millions of Users up to Date with Redis Pub/Sub - RedisConf 2017](https://www.youtube.com/watch?v=nXTxXSWBayg)
     - [How GAP scaled over 100x using Redis](https://www.youtube.com/watch?v=mxWUGaPKjtI)
     - [Processing 160 million messages a day using Redis with Wavy (Portuguese w/ English slides)](https://www.youtube.com/watch?v=N-myTniud5s)
     - [How Adobe Leverages Redis to Serve and Secure Billions of API Requests](https://www.youtube.com/watch?v=gvQRg4DJDIE)
   - #### Redis Enterprise
     - [Continuous Availability, Infinite Scaling, Secure, Cost-effective Redis - RedisConf 2017](https://www.youtube.com/watch?v=UOcluQa2XL4)
     - [Ultra Scaling with Redis Enterprise](https://www.youtube.com/watch?v=-4QHqJi9qFk)
     - [Redis Enterprise Overview - Redis Day TLV 2016](https://www.youtube.com/watch?v=yk6qGCgavHY)
     - [Troubleshooting Redis Performance Insights w/ Redis Enterprise Cluster](https://www.youtube.com/watch?v=Ox6mRDaqnUE)
     - [Redis on Flash - A Game-Changing Database Platform for Etermax](https://www.youtube.com/watch?v=EYEksrUcuaw)
     - [Redis Enterprise Flash: Scaling Data Size with Redis Enterprise at Near RAM Latency](https://youtu.be/EUAGY5HTPYA)
   - #### AWS ElastiCache for Redis
     - [Extreme Performance at Cloud Scale - RedisConf 2019](https://www.youtube.com/watch?v=CQj0sASECr8)
     - [Building Resilient Real-Time Applications with Amazon ElastiCache for Redis - AWS Online Tech Talks](https://www.youtube.com/watch?v=dqf_c2UK_zU)
     - [Fast Data at Internet Scale with Amazon ElastiCache for Redis](https://www.youtube.com/watch?v=fyMXt2wI47E)
     - [Enterprise-Class Security, High-Availability, & Scalability with Amazon ElastiCache](https://www.youtube.com/watch?v=cXMf4EQWtXg)
     - [Redis & Amazon ElastiCache: Building Real Time Apps - AWS 2019](https://www.youtube.com/watch?v=QqXRnZWRuLU)
     - [Amazon ElastiCache for Redis Global Datastore - Active-Passive Multi-Region Redis](https://www.youtube.com/watch?v=xx6X5s9uLBs)
     - [Scaling Redis Workloads with Amazon ElastiCache](https://www.youtube.com/watch?v=gPNSYnxl6Ms)
     - [Best practices: migrating Redis clusters from Amazon EC2 to ElastiCache](https://www.youtube.com/watch?v=Rpni5uPe0uI)
   - #### Chaos Engineering
     - [Redis Fault Injection](https://www.youtube.com/watch?v=JL5uqkRNBJE)
     - [Ensure Redis Reliability with Gremlin, Chaos Engineering](https://www.youtube.com/watch?v=i5QpK--35_s)
   - #### Performance
     - [The Top Redis Metrics that Matter - DataDog 2015](https://www.youtube.com/watch?v=fvByUcN4sHs)
     - [Benchmarking Redis](https://www.youtube.com/watch?v=PPydnyFt8zY)
     - [Redis benchmark in native Linux mode, Linux VM, and Docker container](https://www.youtube.com/watch?v=Qow-sXNM0pQ)
     - [Redis Reliability, Performance & Innovation](https://www.youtube.com/watch?v=A5nvOuUjOjY)
     - [High Performance Redis](https://www.youtube.com/watch?v=ccpEFUEzSXg)
     - [Benchmarking Redis By Itself and Versus Other NoSQL Databases](https://www.youtube.com/watch?v=aotCPUtahDU)
     - [Redis on NVMe SSD](https://www.youtube.com/watch?v=Zi3b9wHhrx4)
   - #### Security
     - [Exploiting Unauthenticated Redis - TryHackMe!](https://www.youtube.com/watch?v=LVlQmRM6DZ0)
     - [New Security Features in Redis 6 Open Source](https://www.youtube.com/watch?v=57SgF5iht8Y)
     - [Practical Use Cases for Access Control Lists in Redis 6](https://www.youtube.com/watch?v=BGoBM-Bl2UI)
     - [Secure Redis Cluster at Box](https://www.youtube.com/watch?v=W1FICEpaQ1A)
     - [Hack The Box: Postman Walkthrough [Redis, SSH, Webmin Exploit]](https://www.youtube.com/watch?v=rR9AUjLnM1Q)
   - #### Monitoring / Tooling
     - [RedisInsight - RedisConf 2020](https://www.youtube.com/watch?v=HBC3OSYOgj0)
     - [RedisInsight - A FREE Robust GUI Tool to Monitor Redis Data](https://www.youtube.com/watch?v=VqPdHngkz1I)
     - [Monitoring Redis data using RedisInsight - OSConf 2020](https://www.youtube.com/watch?v=BVXFBhKeUxk)
     - [Prometheus Exporter and Grafana with Redis](https://www.youtube.com/watch?v=5m474BwV660)
