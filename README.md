# Saving AWS Infrastructure Costs

# What this blog targets?
This blog is going to focus on saving operational infrastructure costs. This is not going to focus on cost efficient design. In an agile world, there are typically many AWS accounts, many teams sharing a single AWS accounts, etc. And there are multiple deployments happening for each project, each project having different components.  For eg. if there are 5 teams sharing an AWS account and 5 components per team and an average of 1 deployment per component per day, we are looking at 25 deployments per day.

This is a common scenario in a typical CI/CD world where there are many build, tests and deployments happening at a single point of time. We all agree that this brings engineering efficiency as we can move features faster to market.  

However, we have a few operational overhead.
## 1. Cleaning up of unwanted EC2 instances.
## 2. Cleaning up of unwanted Auto Scaling Groups/Launch Configurations.
## 3. Cleaning up of AMI Images and EBS volumes.

If left unattended, these tend to slowly pile up the overall costs (Except #2).

To save costs, we have to follow the following strategy

1. Identify a way for finding out unwanted resources (EC2, AMI, etc.)
2. Identify a way for cleaning up those resources.

I'm going to start a open source project which will focus on the above mentioned area.
