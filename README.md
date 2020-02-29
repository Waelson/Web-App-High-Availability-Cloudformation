# Highly Available Web Application on AWS
Template to create infrastructure highly available to web app. Infrastructure as code based on AWS Cloudformation.
<br/>
<h4>How to use:</h4>
Before you begin to use this repository, check you have installed AWS CLI in your machine. If you haven't installed it, please consider to visit <a href="https://docs.aws.amazon.com/cli/latest/userguide/install-bundle.html">AWS CLI Site</a> for more informations.
<br/><br/>
<ul>
  <li>Into repository you will find two shell scripts files to create and update stack into Cloudformation. Use them to manipulate your Cloudformation stack or as reference to learning about Cloudformation commands using AWS CLI. </li>
  <li>Create stack: <code>./create.sh &#60;your-stack-name&#62; &#60;cloudformation-script-yml-file&#62; &#60;parameter-file&#62;</code></li>
  <li>Update stack: <code>./update.sh &#60;your-stack-name&#62; &#60;cloudformation-script-yml-file&#62; &#60;parameter-file&#62;</code></li>
  <li>Note #1: Scripts must to be execute in following order: First, <code>networks.yml</code> responsable for creation all network configurations and last <code>servers.yml</code> to create EC2 instances and other resources associate it.</li>
  <li>Note 2#: If you need to change IP range, check <code>network-params.json</code> file to update configurations.</li>
</ul>

<h4>Main points architecture:</h4>
<ul>
  <li>All single points of failure eliminated. Remember, resources like Internet Gateway and Load Balancer are managed by AWS team.</li>
  <li>Included redundancy through Auto Scaling Group and database replication.</li>
  <li>All resources  are distributed between two availability zones. So, we guarantee more availability to architecture.</li>
  <li>All EC2 instances are accessible just via load balancer. Note that all instances belong to private subnet, isolating them all external traffic.</li>  
  <li>Important Note: Script files don't create database. Therefore, I recommend you to create database through web console (RDS - Relational Database Service) and associate it your private subnet.</li>
</ul>
<h4>Solution diagram:</h4>
<img src="https://github.com/Waelson/web-app-high-availability-cloudformation/blob/master/Diagram-CloudFormation.png">


