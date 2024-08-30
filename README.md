NOTE: Peering Connection mens connecton b/w the Two vpcs B/w the Communication process
What is peering it is a twoway connection of the proess to communicate b/w the two diffrent vpcs an d transfer b/w two vpcs.
Creation of the process was connect the two public servers and conncet the private inside of the pubilc for using to the peerconnction.
-
Step1: Go to vpcs 
      -> create the  vpc
-> Name tag optional
      VPCA  (write)
-> IPV4 CIDR
     10.0.0.0/24 (write)
                               (create vpc)
 Step2: Go to vpcs 
      -> create the  vpc
-> Name tag optional
      VPCB  (write)
-> IPV4 CIDR
     20.0.0.0/24 (write)
                               (create vpc) 
NOTE: Write the name Route table (VPC1)
Step3: Create the subnets
-> VPC ID
      VPCA (write)
-> Subnet 1 of 1
      Vpca1subnet (write)
  -> IPV4 Subnet CIDR block
         10.0.0.0/28 
                                ( create)
step4: Like this one more subnet create
 Create the subnets
-> VPC ID
      VPCB (write)
-> Subnet 1 of 1
      Vpcb2subnet (write)
  -> IPV4 Subnet CIDR block
         20.0.0.0/28 
                                ( create)
Step5: Associate with internet gateway go to their and create
  -> Name tag
        internet  (write)
                                       (create internet gatway)
Step6: Attach to the vpc
-> Availlable vpcs
        fill this one
                                      (attach to the gateway)
step6: Allow the internet server for the traffic based
 go to the route tables and first edit routes and after add route then save changes.

 Step7: create the instances two
       vpcA
       vpcB
       -> both are public instances and give to the Enable option
step8: create to the one more private instance it was Disable give after lunch the instances.

When VPC was agin using peering to connctions public one more based process after publicserver run inside of the private server for the purpose we are using perring.
-
Step9: Go to the vpc and connect the peering connection
-> create the peering
        Name: Peering
-> VPC ID: VPCA
-> Vpc ID (Accepter)
    VPCA  (write)
                    ( creating peering)
Step10: Goto the Actions And Accept the request
Step11: Go to the route tables and also edit the routes both two



This is connect to the public server after inside connect the private server process using some commands
-

 ,     #_
   ~\_  ####_        Amazon Linux 2023
  ~~  \_#####\
  ~~     \###|
  ~~       \#/ ___   https://aws.amazon.com/linux/amazon-linux-2023
   ~~       V~' '->
    ~~~         /
      ~~._.   _/
         _/ _/
       _/m/'
[ec2-user@ip-10-0-0-4 ~]$ sudo su -
[root@ip-10-0-0-4 ~]# ping google.com\
> ^c
-bash: !!: event not found
> ping google.com
ping: google.comping: Name or service not known
[root@ip-10-0-0-4 ~]# vi vinu.pem
[root@ip-10-0-0-4 ~]# chmod 400 "vinu.pem"
[root@ip-10-0-0-4 ~]# ssh -i "vinu.pem" ec2-user@10.0.0.6
The authenticity of host '10.0.0.6 (10.0.0.6)' can't be established.
ED25519 key fingerprint is SHA256:QB9itxEzKz6Zy74GpwZaoVk6Digk5w43Q6ZIC9OTIJY.
This key is not known by any other names
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '10.0.0.6' (ED25519) to the list of known hosts.
   ,     #_
   ~\_  ####_        Amazon Linux 2023
  ~~  \_#####\
  ~~     \###|
  ~~       \#/ ___   https://aws.amazon.com/linux/amazon-linux-2023
   ~~       V~' '->
    ~~~         /
      ~~._.   _/
         _/ _/
       _/m/'
[ec2-user@ip-10-0-0-6 ~]$ sudo su -
[root@ip-10-0-0-6 ~]# ping google.com
PING google.com (142.250.74.14) 56(84) bytes of data.
       
 
        
  
