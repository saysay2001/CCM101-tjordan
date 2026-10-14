# Research: Multi-Tier Architecture

## What is Two-Tier Architecture?

A Two-Tier Architecture is a system design that separates an application into two main parts: the Web/Application Tier and the Database Tier. These two tiers communicate with each other to process requests and manage data.

## 1. The Web/Application Tier

The Web/Application Tier handles the user interface and receives HTTP requests from users. It processes user actions, runs application logic, and communicates with the database to retrieve or save information.

## 2. The Database Tier

The Database Tier stores and manages persistent data, such as user accounts, passwords, records, and other application information. It receives queries from the Web/Application Tier and returns the requested data.

## 3. Why Separate Them?

Separating the web server and database into two containers makes the system easier to manage, maintain, and troubleshoot. It also improves security by allowing the database to remain isolated from direct user access. Additionally, each container can be updated or scaled independently without affecting the other tier unnecessarily.
