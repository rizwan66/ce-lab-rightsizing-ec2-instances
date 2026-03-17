{\rtf1\ansi\ansicpg1252\cocoartf2867
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fswiss\fcharset0 Helvetica;}
{\colortbl;\red255\green255\blue255;}
{\*\expandedcolortbl;;}
\paperw11900\paperh16840\margl1440\margr1440\vieww11520\viewh8400\viewkind0
\pard\tx720\tx1440\tx2160\tx2880\tx3600\tx4320\tx5040\tx5760\tx6480\tx7200\tx7920\tx8640\pardirnatural\partightenfactor0

\f0\fs24 \cf0 # Lab M7.03 - Rightsizing EC2 Instances\
 \
## What I Did\
- Launched 3 EC2 instances of different sizes (t3.medium, t3.large, m5.xlarge)\
- Installed CloudWatch agent and collected CPU + memory metrics\
- Ran stress tests to simulate varied workloads\
- Analyzed utilization and created a rightsizing report\
- Resized over-provisioned instances and verified operation\
 \
## Key Findings\
- api-server (t3.large) averaged 2% CPU \'97 downsized to t3.small\
- data-processor (m5.xlarge) averaged 2% CPU \'97 downsized to t3.medium\
- Projected monthly savings: $133.59\
 \
## Screenshots\
- cloudwatch-metrics.png\
- rightsizing-report-table.png\
- post-resize-verification.png}