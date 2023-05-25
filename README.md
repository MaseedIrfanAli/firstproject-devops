# Prerequisites
#
- JDK 1.8 or later
- Maven 3 or later
- MySQL 5.6 or later

# Technologies 
- Spring MVC
- Spring Security
- Spring Data JPA
- Maven
- JSP
- MySQL
# Database
Here,we used Mysql DB 
MSQL DB Installation Steps for Linux ubuntu 14.04:
- $ sudo apt-get update
- $ sudo apt-get install mysql-server

Then look for the file :
- /src/main/resources/accountsdb
- accountsdb.sql file is a mysql dump file.we have to import this dump to mysql db server
- > mysql -u <user_name> -p accounts < accountsdb.sql

# ==========================================================================================================

1.Create a free tier AWS account
2.Create a user with admin access
3.Create alarms
Billing-> Billing DashBoard-> check access for user if there then check billing preference tab
and keep threshold to alert.
3.Create *.website.com domain at AWS Cert Manager
tag Name:cert ::
key+value copy and past in domain in godady or other domain websites..
5.Create Security groups
SG_ELB ->80 Ingress.
SG_APP->SG_ELB,SSH Ingress,.
SG_Backend -> SG_APP Ingress,SSH,Itself.
6.Create key-pair.
7.route and give tags for internal IP to app01.projectname.in,db01.projectname.in,mc01.projectname.in,rbmq01.projectname.in.
8.change the application properties file with desired routing domain .
9.launch the instance with user data.
10.mvn build the code in local and upload the to aws.
create a bucket and copy or upload the code by awscli local.
11. After upload you need to download form there so you should create a user withrole .
12. download and copy the target .war file to to /var/lib/web/ROOT.War by deleting existing ROOT.
13. Create Image and Lunch config for cofig of scalling.
delete the bucket user and access and after practice please delete Route53,loadbalancer if any it may cause billing alerts.


