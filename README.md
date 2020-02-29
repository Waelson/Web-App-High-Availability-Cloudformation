# Web Application Highly Available on AWS
Template to creation web app infrastructure highly available. Infrastructure as code based on AWS Cloudformation.
<br/>
<h4>Main points architecture:</h4>
<ul>
  <li>All single points of failure eliminated. Remember, resources like Internet Gateway and Load Balancer are managed by AWS team.</li>
  <li>Included redundancy through Auto Scaling Group and database replication.</li>
  <li>All resources  are distributed between two availability zones. Do, we guarantee more availability to architecture.</li>
  <li>All EC2 instances are accessible just via load balancer. Note that all instances belong to private subnet isolating them all external traffic.</li>  
</ul>
<h4>Solution diagram:</h4>
<img src="https://github.com/Waelson/web-app-high-availability-cloudformation/blob/master/Diagram-CloudFormation.png">


