# AWS-WAF-CAF-Capstone-Project
# Project Overview
This project involves a comprehensive evaluation and architectural redesign of a two-tier web application (Frontend and Backend) being migrated from an on-premises environment to AWS. The goal was to ensure the new cloud-native solution adheres to the AWS Well-Architected Framework (WAF) and the AWS Cloud Adoption Framework (CAF).

# My Approach
# 1. Risk Identification
I began by analyzing the existing "lift-and-shift" plan to identify critical weaknesses. The primary concerns identified were:

* Availability: The single-AZ deployment created a single point of failure.
* Security: Permissive security groups increased the risk of unauthorized lateral movement.
* Data Integrity: The lack of an automated backup strategy posed a risk of permanent data loss.
  

# 2. Well-Architected Evaluation (WAF)
Using the five pillars of the WAF, I evaluated the workload to identify strengths and areas for improvement. My focus was on transforming manual processes into automated, resilient systems.

* Operational Excellence: Recommended Infrastructure as Code (IaC).
* Reliability: Proposed a Multi-AZ architecture with automated failover.
* Security: Implemented Least Privilege access and Web Application Firewalls (WAF).
  
# 3. Readiness Assessment (CAF)
I utilized the six perspectives of the AWS CAF to assess the organization's migration readiness. This step ensured that the transformation wasn't just technical, but also addressed Governance, People (Culture), and Business strategy.

# 4. Architectural Redesign
The final solution features a VPC-based architecture spread across two Availability Zones. It utilizes an Application Load Balancer, EC2 Auto Scaling, and Amazon RDS Multi-AZ to ensure the application is highly available, secure, and ready for production-level traffic.
