### In this article, I will cover the ACID and BASE model which is very important with respect to designing systems.

<br>

### Table of contents:


- [Introduction](#introduction)
- [ACID MODEL](#acid-model)
- [BASIC MODEL](#basic-model)
- [Comparison of ACID and BASE model](#comparison-of-acid-and-base-model)
- [Examples](#examples)
- [Conclusion](#conclusion)


<br>


# Introduction

So we all have been learning ACID and BASE since our high school which is combining them will give you salt and water which is very important for our life.

<br>

***Although this is correct but the concept I am talking about is entirely different.***

<br>

> So what is ACID and BASE model ?
> 
>**Let's find out**

<br>

![ACID-and-BASE-model](/content/images/2023/03/ACID-and-BASE-model.png)

<br>

The ACID and BASE models are two different approaches to ensuring consistency and reliability in database systems.

<br>

# ACID MODEL

ACID model  is a set of properties that ensure the reliability of transactions in a database system. The ACID acronym stands for Atomicity, Consistency, Isolation, and Durability. Let's understand each property.

<br>

> **Atomicity:** This property ensures that a transaction is treated as a single, indivisible unit of work. Either all operations within the transaction are completed successfully, or none of them are completed at all ( 1 0r 0). This means that if a failure occurs during the transaction, the database remains in a consistent state.

<br>

For example, if you transfer money from one bank account to another, the transaction should be atomic. If the transaction fails midway, the amount should not be deducted from the sender's account and should not be credited to the receiver's account.

<br>

> **Consistency:** This property ensures that the database remains in a valid state at all times. A transaction must bring the database from one valid state to another, satisfying all constraints, such as referential integrity, domain constraints, and other rules. In simpler words, that the data in a database is always accurate and up-to-date. It means that the database remains in a valid state at all times, satisfying all constraints, such as referential integrity, domain constraints, and other rules.

<br>

For example, if a database stores information about employees, each employee record should have a unique ID. If a transaction attempts to add a record with a duplicate ID, the transaction should be rolled back to maintain the consistency of the database.

<br>

> **Isolation:** This property ensures that multiple transactions can execute concurrently without interfering with each other. Each transaction appears to execute in isolation from other transactions, even if they access the same data.

<br>

For example, if two transactions attempt to update the same record simultaneously, the isolation property ensures that only one of the transactions can make the change, while the other transaction waits until the first transaction is complete.

<br>

> **Durability:** This property ensures that once a transaction is committed, its effects are permanent and cannot be undone, even in the event of a system failure. This means that the database can recover from a failure and remain in a consistent state. 

<br>

For example, if a power outage occurs during a transaction, the durability property ensures that the transaction's effects are still permanent and will not be lost when the system comes back online.

<br>

> **The ACID model is widely used in traditional relational database management systems (RDBMS) and is essential for maintaining data integrity and consistency.**

<br>

# BASIC MODEL

The BASE model is an alternative to the ACID model that focuses on scalability and availability. The properties of the BASE model include:

<br>

> **Basically Available:** This property ensures that the system is always available for use, even if some of its nodes are down or unavailable. This means that the system can continue operating even if it cannot provide the full range of services.

<br> 

For example, if a node in a distributed system fails, the system can continue to operate without that node, even if it means that some of the services are not available.

<br>

> **Soft state:** This property allows the state of the system to change over time, even without input. This means that the system can operate without synchronization and permits temporary inconsistencies between nodes.

<br>

For example, if two nodes in a distributed system are not synchronized, they may temporarily have different versions of the same data. However, the system will eventually become consistent over time.

<br>

> **Eventually consistent:** This property ensures that the system will eventually become consistent, even if it may not be consistent at all times. This means that the system can trade off immediate consistency for scalability and availability.

<br>

For example, if a distributed system receives a large number of requests, it may prioritize availability over consistency to ensure that the system remains responsive, even if the data is not always consistent.

<br>

> **Confused ?**
> 
> *Let's make thing more simpler.*

<br>

# Comparison of ACID and BASE model

<table class="infobox biography vcard" style="table-layout:fixed;white-space:normal;"><tbody><tr><th colspan="1" style="text-align:center;font-size:125%;font-weight:bold;max-width:2px"><div class="fn" style="display:inline"></div></th></tr>

<tr><th scope="row" style="text-align:center;border:1px solid #c8ccd1" >ACID MODEL</th><th scope="row" style="text-align:center;border:1px solid #c8ccd1">BASE MODEL</th></tr>
    
<tr style="min-width:2px"><td style="border:1px solid #c8ccd1" class="role">It emphasizes strong consistency guarantees.</td><td style="border:1px solid #c8ccd1;" class="role">It emphasizes more on availability and partition tolerance</td>
<tr style="min-width:2px"><td style="border:1px solid #c8ccd1" class="role">Transactions are atomic and isolated</td><td style="border:1px solid #c8ccd1;" class="role">Transactions may be partially completed or have weaker isolation guarantees</td>
<tr style="min-width:2px"><td style="border:1px solid #c8ccd1" class="role">Ensures that the database is always in a consistent state</td><td style="border:1px solid #c8ccd1;" class="role">Does not guarantee immediate consistency; may sacrifice consistency for availability or performance</td>
<tr style="min-width:2px"><td style="border:1px solid #c8ccd1" class="role">Usually used in traditional RDBMS systems	</td><td style="border:1px solid #c8ccd1;" class="role">Used in distributed databases and NoSQL systems</td>
<tr style="min-width:2px"><td style="border:1px solid #c8ccd1" class="role">May result in higher latency and lower throughput due to strong consistency guarantees</td><td style="border:1px solid #c8ccd1;" class="role">May provide higher throughput and lower latency due to weaker consistency guarantees</td>


</tbody></table>

I hope this make things more clear to you.

<br>

# Examples
<br>

 The ACID model is commonly used in traditional relational database management systems, such as Oracle, SQL Server, and MySQL. These database systems are used in a variety of industries and applications, including finance, healthcare, e-commerce, and more. For example, a bank may use an ACID-compliant database to store customer account information and transaction history.

On the other hand, the BASE model is commonly used in distributed databases and NoSQL systems. These systems are used in large-scale web applications, such as social networks, e-commerce websites, and big data analytics platforms. For example, a social media platform like Facebook may use a NoSQL database to store user profiles, posts, and interactions.


# Conclusion
<br>

> *In both cases, the choice of the database model depends on the specific requirements of the application. If strong consistency guarantees are required, such as in financial transactions, the ACID model may be more appropriate. However, if high availability and scalability are more important, such as in a social network with millions of users, the BASE model may be a better fit.*

<br>

*That's all in this article*
**Thank you**

<br>

