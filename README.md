osTicket-IT-Helpdesk-System

A self-hosted osTicket IT Helpdesk built on Windows Server 2022 using IIS, PHP, and MySQL, featuring ticket management, agents, teams, help topics, SLAs and ticket resolution workflows
# osTicket IT Helpdesk System

A Windows Server-based IT Helpdesk system built using **osTicket, IIS, PHP, and MySQL**.

This project simulates a small organization's internal IT support environment, including agents, teams, help topics, ticket assignment, priorities, SLA management, and ticket resolution.

This project is part of my **IT Support / Systems Administration Home Lab** and demonstrates practical experience with Windows Server, IIS, PHP, MySQL, and IT service management.

Project Overview

The objective of this project was to deploy and configure a functional **IT Helpdesk system** that can be used to manage technical support requests.

The system allows users to:

- Submit IT support tickets
- Select appropriate help topics
- Describe technical issues
- Track ticket status
- Receive responses from IT agents

IT support agents can:

- View submitted tickets
- Assign tickets to teams
- Assign tickets to individual agents
- Respond to users
- Set ticket priorities
- Manage and resolve tickets
- Work with SLA requirements

Lab Environment

TICKET-01

- Windows Server 2022
- IIS
- PHP
- MySQL
- osTicket

Supporting Infrastructure

The helpdesk is part of a larger virtualized Windows environment containing:

                    HOME LAB VM
                       │
          ┌────────────┴────────────┐
          │                         │
       DC-01                    TICKET-01
 Windows Server 2022          Windows Server 2022
 Active Directory             IIS
 DNS                          PHP
                              MySQL
                              osTicket
          │                         │
          └────────────┬────────────┘
                       │
                   CLIENT-01
                   Windows 11


MySQL Configuration

A dedicated MySQL database was created for osTicket.

Database
Database: osticket
Database User
Username: osticket
Host: localhost

A dedicated database account was used instead of the MySQL root account.

The osTicket application uses this account to access its database.

osTicket Configuration

The osTicket installation was completed successfully and configured for an internal IT helpdesk environment.

The following components were configured:

Agents
Teams
Departments
Help Topics
Ticket priorities
SLA policies
Ticket assignment
Ticket responses
Ticket resolution

Agents

The following fictional agents were created for the helpdesk:

Agent	Department
Alessandro Bastoni	ICT Team
Daniel Mokoena	ICT Maintenance
Federico Chiesa	Hardware Support
Nicolo Barella	Cybersecurity
Sandro Tonali	Service Desk
Vlad Von Castin	Network Support

The player names are used as fictional identities for the purpose of this home-lab project.

Teams / Departments

The helpdesk was divided into several teams:

ICT Team
ICT Maintenance
Hardware Support
Cybersecurity
Service Desk
Network Support

These teams simulate different areas of an organization's IT department.

Help Topics

The following help topics were configured:

Computer Issue
Password / Account Issue
Network Problem
Printer Problem
Software Installation
Security Incident
Other IT Issue

Help Topics allow incoming support requests to be categorized and routed to the appropriate IT team.

SLA Configuration

SLA policies were configured to simulate different levels of ticket urgency.

Priority	Response Target
Critical	1 hour
High	4 hours
Normal	8 hours
Low	24 hours

These SLA values are used for demonstration purposes within the home lab and do not represent a real organization's contractual SLA.

Ticket Workflow

The ticket workflow was tested from creation through resolution.

User
  │
  │ Submit IT Issue
  ▼
osTicket
  │
  │ Select Help Topic
  ▼
Ticket Created
  │
  │ Team Assignment
  ▼
IT Support Team
  │
  │ Agent Assignment
  ▼
IT Agent
  │
  │ Investigate
  │ Respond
  ▼
Ticket Resolved

The following ticket operations were tested:

Ticket creation
User identification
Help Topic selection
Team assignment
Agent assignment
Priority management
Agent responses
Ticket resolution

Testing

A test ticket was created to verify the helpdesk workflow.

Example Ticket

Help Topic:

Computer Issue

Issue:

Computer unable to connect to network

The ticket was then:

Created
Assigned to a team
Assigned to an agent
Investigated
Responded to
Resolved

This confirmed that the core osTicket ticket lifecycle was functioning correctly

Security Configuration

After installation, the osTicket configuration file was secured.

Configuration file:

C:\inetpub\wwwroot\osticket\upload\include\ost-config.php

Write/Modify permissions were removed after installation so the web server could no longer modify the configuration unnecessarily.

The osTicket setup directory was also removed after installation


Phase 1 - Completed

The following tasks have been completed:

 Windows Server 2022 environment
 IIS installation
 PHP installation
 PHP configuration
 PHP extensions configured
 MySQL installation
 osTicket database created
 osTicket database user created
 osTicket installed
 IIS configured for osTicket
 Agents created
 Teams configured
 Departments configured
 Help Topics configured
 Ticket priorities configured
 SLA configuration
 Ticket creation tested
 Ticket assignment tested
 Agent response tested
 Ticket resolution tested
 Configuration file secured
 
 Phase 2 - Planned Improvements

Future improvements to the project include:

 Active Directory integration
 LDAP authentication
 Domain user integration
 Email / SMTP integration
 Automated email notifications
 Password reset through email
 Knowledge Base configuration
 Advanced SLA automation
 HTTPS / SSL configuration
 IIS security hardening
 Logging and monitoring
 Security testing
