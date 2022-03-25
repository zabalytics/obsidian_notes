# EC2 (Elastic Computing Cloud)
EC2 is a web service an AWS subscriber can request and provision a [[Compute Domain Controller |compute domain controller]]  in the AWS cloud. AWS's on-demand EC2 instance is a service that allows subscribers/users to rent virtual servers by the hour and use them to deploy their own applications. These servers are charged on an hourly basis and the rate varies depending on the instance type. 

## Creating an EC2 Instance on AWS

1. Login to AWS and navigate to the Amazon web services tab in the upper left corner
2. Select EC2 from the Compute services list. This will open the EC2 dashboard
3. Select the region you would like to set up the EC2 instance on in the upper right hand corner
4. Click the "Launch Instance" button on the EC2 dashboard
5. Select an Amazon Machine Image (AMI). There are many different images you can choose from (i.e. Windows Server with SQL Server, Deep Learning AMI (Ubuntu), MacOS Big Sur) . Select the one that matches your needs. The instance will be automatically booted with the specific OS when you launch and EC2 instance from your preferred AMI.
6. Select an EC2 instance type. These all have different amounts of CPUl, Memory, and other configurations. 
7. Configure the instance. This is where you get to select how many instances you want, get the virtual private cloud (VPC) name, etc.
  - Under purchasing options keep the "Request Spot instances" unchecked unless you want to release Spot instances rather than on-demand ones
  - Select the [[EC2 Subnets|subnets]] and IP ranges 
  -  Set the [[AWS IAM|IAM]] role
  - Set shutdown behavior. You can have it delete, but it is probably best to just stop the instance
  - Check the box that protects against accidental termination. This will make it so you cannot delete the application until this box has been unchecked
  - Enable cloudwatch if you would like detailed monitoring on a business critical instance
  - Set Tenancy. If the application running on the instance requires a high level of security, you should opt for dedicated capacity
9. Select how much storage you want on your instance. You can also add one or more [[Volume|volumes]] to the instance
10. Add [[EC2 Tags|tags]]  if desired. It is recommended to at least add a tag for PROD, Stage, or Test environment
11. Set up Security Groups.  You can do any of the following to make your instance more secure
  - restrict traffic to your instance ports.
  - Set allowable ports and IPs
  - add a security group
  - name the security group for convenience
  - define protocols for the instance
  - assign IPs that can access the instance via protocols set up
  - Setup of firewall rules
12. Set a public-private key pairs (PKP) - If you lose the key after downloading it, you will be unable to access the instance, so keep it in a safe place 
13. Launch the instance

## Connecting to your Instance by creating an Elastic IP (EIP)
Normally, when you start an instance, it gets an IP from AWS's pool. An EIP is an AWS static public IP. The public IP changes if you stop or restart the instance.

You should use an EIP to give your application a static IP on which to connect to public networks

__Steps to creating an EIP__

1. Go to "Elastic IPs" in EC2 Dashboard's resource pane
2. Click allocate Elastic IP address
3. If not already, associate this IP to a VPC scope
4. Associate your instance with the created EIP
  - Select the EIP
  - Press the "Associate Elastic IP Address"
  - Find your instance and assign the IP to it
  - Return to the instance screen to see if the EIP has been recieved (It should show on the dashboard)
5. Open terminal and ssh into EIP address

