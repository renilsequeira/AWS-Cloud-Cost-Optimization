# AWS-Cloud-Cost-Optimization

AWS Cloud Cost Optimization - Identifying Stale Resources

Project Overview
This project focuses on optimizing AWS cloud costs by identifying and removing stale resources, specifically targeting Elastic Block Store (EBS) snapshots that are no longer associated with any active EC2 instance. The solution utilizes AWS Lambda to automate the identification and deletion process, helping to reduce storage costs.

Table of Contents
Introduction
Installation
Usage
Configuration
Testing
Contributing
License

Introduction

Problem Statement

Over time, AWS environments can accumulate stale resources, leading to unnecessary storage costs. This project addresses the issue by creating a Lambda function that identifies EBS snapshots without any active associations and removes them.

Solution Overview

The Lambda function fetches all EBS snapshots owned by the AWS account and retrieves a list of active EC2 instances (both running and stopped). For each snapshot, it checks if the associated volume is not linked to any active instance. If a stale snapshot is found, it is deleted, optimizing storage costs.



