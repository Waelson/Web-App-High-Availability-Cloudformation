# Web Application Highly Available on AWS
Template to creation web app infrastructure highly available. Infrastructure as code based in AWS Cloudformation.
<br/>
<h4>Solution Diagram:</h4>
<img src="https://github.com/Waelson/web-app-high-availability-cloudformation/blob/master/Diagram-CloudFormation.png">

<h4>Main Points</h4>
<ul>
  <li>I tried all single point of failures.</li>
  <li>All EC2 instances are accessible just via load balancer. Note that all instances belong to private subnet isolating them all external traffic.</li>  
</ul>
