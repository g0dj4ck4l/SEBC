**1. What is ubertask optimization?**
Ubertask optimization runs "sufficiently small" jobs sequentially within a single JVM. "Small" is defined by the mapreduce.job.ubertask.maxmaps, mapreduce.job.ubertask.maxreduces, and mapreduce.job.ubertask.maxbytes settings.

**2. Where in CM is the Kerberos Security Realm value displayed?**
Search for default_realm under Administration > Settings in CM

**3. Which CDH service(s) host a property for enabling Kerberos authentication?**
All CDH core services have a property for enabling Kerberos Authentication: HDFS, Zookeeper, Hive, Hue, Oozie and YARN.

**4. How do you upgrade the CM agents?**
You can use an upgrade wizard that is invoked when you connect to the Admin Console or manually install the Cloudera Manager Agent packages

**5. Give the tsquery statement used to chart Hue's CPU utilization?**
select cpu_system_rate + cpu_user_rate where serviceName=HUE

**6. Name all the roles that make up the Hive service**
Hive Metastore Server, WebHCat Server, HiveServer2 and Gateway

**7. What steps must be completed before integrating Cloudera Manager with Kerberos?**
Before integrating Cloudera Manager with Kerberos, as reported in this document https://www.cloudera.com/documentation/enterprise/5-8-x/topics/cm_sg_intro_kerb.html, the following steps are needed:

a. Set up a working KDC. Cloudera Manager supports authentication with MIT KDC and Active Directory.
b. Configure the KDC to allow renewable tickets with non-zero ticket lifetimes.
c. For MIT KDC, are needed the following settings:
```
max_life = 1d  
max_renewable_life = 7d
kdc_tcp_ports = 88
```
d. Kerberos client/libs must be installed on ALL hosts in the cluster.
e. Create an account for Cloudera Manager that has the permissions to create other accounts in the KDC
