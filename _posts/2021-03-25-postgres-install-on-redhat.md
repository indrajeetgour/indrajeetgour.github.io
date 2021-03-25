---
layout: post
title: "How to install Postgres Client on RedHat/CentOS"
author: igour
categories: [How-to, tutorial]
image: assets/images/16.jpg
---
To install the Postgres Client on the another client server, it is very easy to do.

## Just follow the following steps
I have postgres server of version 11, so do I install this client libs:
```
 yum -y install postgresql11 && yum clean
```

Onces you successfully installed, then you can use your postgres server informations to test the connectivity, like this

```
export PGPASSWORD='yourdbpassword'
[root@gcp6207qtyrdi01 rundeck-codebase]# psql -U username -p 5430 --host yourpostgresserver -d yourdb --command 'select * from yourtablename'
```
Few everything going fine than you would able to see the resultset on the client console.

#### Note - never forget to open the firewall between your posgres server host and your client server on the mentioned postgres input.


