{\rtf1\ansi\ansicpg1252\cocoartf2867
\cocoatextscaling0\cocoaplatform0{\fonttbl\f0\fnil\fcharset0 HelveticaNeue-Bold;}
{\colortbl;\red255\green255\blue255;\red193\green193\blue193;\red19\green19\blue19;}
{\*\expandedcolortbl;;\cssrgb\c80000\c80000\c80000;\cssrgb\c9412\c9412\c9412;}
\paperw11900\paperh16840\margl1440\margr1440\vieww20880\viewh14840\viewkind0
\deftab720
\pard\pardeftab720\sa51\partightenfactor0

\f0\b\fs26 \cf2 \cb3 \expnd0\expndtw0\kerning0
# EC2 Rightsizing Report\
\
## Analysis Period\
- **Date:** [Today's date]\
- **Duration:** 30 minutes of monitoring\
- **Method:** CloudWatch metrics + synthetic load testing\
\
## Instance Analysis\
\
| Instance Name | Current Type | vCPUs | RAM (GB) | Avg CPU % | Avg Mem % | Recommended Type | Monthly Savings |\
|---------------|-------------|-------|----------|-----------|-----------|-----------------|----------------|\
| web-server | t3.medium | 2 | 4 | 65% | 55% | t3.medium (keep) | $0.00 |\
| api-server | t3.large | 2 | 8 | 2% | 12% | t3.small | $26.28 |\
| data-processor | m5.xlarge | 4 | 16 | 2% | 8% | t3.medium | $107.31 |\
\
## Pricing Reference (us-east-1, On-Demand)\
- t3.small: $0.0208/hr \uc0\u8594  ~$15.17/mo\
- t3.medium: $0.0416/hr \uc0\u8594  ~$30.37/mo\
- t3.large: $0.0832/hr \uc0\u8594  ~$60.74/mo\
- m5.xlarge: $0.192/hr \uc0\u8594  ~$140.16/mo\
\
## Total Projected Monthly Savings: $133.59\
\
## Recommendations\
1. **web-server (t3.medium):** Properly sized \'97 CPU peaks at 65%. Keep current type.\
2. **api-server (t3.large):** Severely over-provisioned. Downsize to t3.small.\
3. **data-processor (m5.xlarge):** Severely over-provisioned. Downsize to t3.medium.\
}