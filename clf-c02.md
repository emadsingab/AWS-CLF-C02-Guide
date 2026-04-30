<div class="page-kicker">AWS Certification Notes</div>

# AWS CLF-C02 Complete Revision Guide

<div class="guide-hero">

<div>
<span class="pill">Cloud Practitioner</span>
<span class="pill amber">CLF-C02</span>
<span class="pill blue">Exam Focused</span>

## Full Study Document

This page contains the complete revision guide, service summaries, traps, keywords, and question mapping.

</div>

</div>

---

# AWS Certified Cloud Practitioner CLF-C02 — Complete Exam Revision Guide

---

# PART 1: Quick Answer Table

| Q | Answer | Keywords | Scenario | Service / Solution | Trap |
|---|---|---|---|---|---|
| Q1 | C | Snowball Edge, transfer files, no cost | Data transfer INTO S3 is free | AWS Snowball Edge | Transfer OUT of S3 to Snowball costs money; daily use after 10 days costs money |
| Q2 | B | EC2, vulnerabilities, best practices | Assess application vulnerabilities | Amazon Inspector | Trusted Advisor gives general recommendations; Inspector does automated security scans |
| Q3 | B | on-premises storage exceeded, file sharing, local performance | Extend file storage to cloud | AWS Storage Gateway (file gateway) | S3 mounting is not native file protocol; WorkDocs is for collaboration |
| Q4 | C | EC2 to S3 access, security best practices | Secure EC2-to-S3 access | IAM Role for EC2 | Never hardcode keys in application code |
| Q5 | C | DynamoDB, shared responsibility | Customer responsibility for DynamoDB | Access to DynamoDB tables | AWS manages patching, encryption infrastructure; customer manages access/data |
| Q6 | C | AWS CAF perspective, foundational capabilities | CAF governance perspective | Governance | Sustainability and Reliability are Well-Architected pillars, not CAF perspectives |
| Q7 | C | Docker, cluster size, scheduling, managed | Managed container service without provisioning | AWS Fargate | ECS requires you to manage EC2 instances; Fargate is serverless |
| Q8 | C | NoSQL on EC2, AWS responsibility | Shared responsibility with EC2 | Patch physical infrastructure | Customer patches guest OS; AWS patches physical hardware |
| Q9 | A, E | EC2 rightsizing | Tools for rightsizing EC2 | AWS Cost Explorer + AWS Compute Optimizer | CodeGuru is for code review; SageMaker is ML |
| Q10 | C, D | Trusted Advisor benefits | What Trusted Advisor does | Cost savings + Security monitoring | Trusted Advisor does NOT create/rotate keys or manage containers |
| Q11 | A | on-premises to cloud advantage | Migration advantage | Eliminate data center costs | Not ALL operational expenses are eliminated; cloud still has variable costs |
| Q12 | B | IaC templates, manage deployed services | Manage and govern IaC templates | AWS Service Catalog | CloudFormation deploys; Service Catalog governs who can deploy what |
| Q13 | C | visualize, understand, manage costs over time | Cost visualization tool | AWS Cost Explorer | Pricing Calculator is for pre-deployment estimates |
| Q14 | A, D | discover, transform, visualize data | Data integration and visualization | AWS Glue + Amazon QuickSight | Redshift is warehousing; QLDB is ledger database |
| Q15 | B | global team, migration, AWS best practices | Expert migration help | AWS Professional Services | AMS manages operations; Professional Services helps with strategy/migration |
| Q16 | D | 2-month workload, must not be interrupted | Short-term, no interruption | On-Demand Instances | Reserved = 1-3 year commitment; Spot = can be interrupted |
| Q17 | B | deploy quickly, no manual resource creation | Fast app deployment | AWS Elastic Beanstalk | CloudFormation requires writing templates; Beanstalk is PaaS |
| Q18 | B | protect from accidental deletion/overwriting | S3 data protection | S3 Versioning | Lifecycle moves data; policies control access; encryption protects data |
| Q19 | D | infrastructure as code | IaC service | AWS CloudFormation | CodePipeline = CI/CD; CodeDeploy = deployments |
| Q20 | B | consistent traffic, 1-year, no disruption | Steady workload, long term | Reserved Instances | Spot = interruptible; On-Demand = no commitment discount |
| Q21 | A | dedicated network connection, on-premises to AWS | Private dedicated connection | AWS Direct Connect | VPN goes over public internet; Direct Connect is private physical connection |
| Q22 | B | physical location, global infrastructure | AWS physical location | AWS Region | DataSync = data transfer; Connect = contact center |
| Q23 | B | protect information, risk assessment | Well-Architected Framework pillar | Security | Reliability = recovery; Operational Excellence = processes |
| Q24 | B | internet gateway, VPC | Purpose of internet gateway | Allow VPC to internet communication | NAT gateway allows private subnets OUT only, not inbound |
| Q25 | D | monolith to microservices | Well-Architected design principle | Loosely coupled dependencies | Tight coupling = monolith (bad); loose coupling = microservices (good) |
| Q26 | C | password rotation, access key audit | Compliance credential audit | IAM Credential Report | Access Analyzer checks external sharing; Artifact is compliance docs |
| Q27 | B, D | cost threshold notification | Cost alert | AWS Budgets + Amazon CloudWatch | Cost Explorer shows history; Cost and Usage Report is raw data |
| Q28 | D | security FAQs | Security questions resource | AWS Knowledge Center | Artifact = compliance docs; Inspector = vulnerability scans |
| Q29 | A, B | customer responsibilities | Shared responsibility | Configure security groups + classify assets | AWS manages physical; customer manages data and access config |
| Q30 | B, E | Well-Architected pillars | Framework pillars | Reliability + Operational Excellence | Availability, Scalability, Responsive design = NOT pillars |
| Q31 | A | text and email from apps | Notification service | Amazon SNS | SQS = queue; SES = email only |
| Q32 | B | programmatic access, CLI, API | Access keys | Access Keys | SSH keys = server login; KMS keys = encryption |
| Q33 | B | stateless, fault tolerant, 3 hours | Batch jobs, interruptible | Spot Instances | On-Demand = uninterruptible; Reserved = long-term |
| Q34 | A, C | agility, cloud computing | Cloud agility concept | Speed of implementation + ability to experiment | Economies of scale = cost; global reach = geography |
| Q35 | A | SQL injection attacks | Web application protection | AWS WAF | Shield = DDoS; NACLs = IP/port filtering at subnet |
| Q36 | C | S3 bucket or IAM role shared externally | External access detection | IAM Access Analyzer | GuardDuty = threat detection; Systems Manager = operational |
| Q37 | B | compliance reports before migration | Compliance documentation | AWS Artifact | Macie = data classification; Support = technical help |
| Q38 | A | ecommerce migrated to cloud, direct cost | Customer's direct cost | Application software licenses | Hardware, power, physical security = AWS responsibility |
| Q39 | C | IAM security best practices | Account security | Enable MFA | Root user keys = dangerous; broad permissions = against least privilege |
| Q40 | B, E | elasticity | Cloud elasticity | Rightsize resources + procure easily when needed | Pay-as-you-go = billing model not elasticity |
| Q41 | A | audit API calls | API audit | AWS CloudTrail | CloudWatch = metrics; Inspector = vulnerabilities |
| Q42 | A | Lambda, customer responsibility | Shared responsibility, Lambda | Managing code in Lambda function | AWS manages hardware, OS, runtime for Lambda |
| Q43 | B | 5TB S3, occasional queries, cost-effective | Query S3 data | Amazon Athena | Redshift = warehousing; Kinesis = streaming |
| Q44 | C | no additional cost | Free AWS service | AWS Organizations | Config, SageMaker, CloudWatch have costs |
| Q45 | C | CAF, people perspective | CAF capability | Cloud fluency | Data architecture = Platform; Strategic partnership = Business |
| Q46 | C, D | upfront commitment, production, lowest cost | Long-term EC2 commitment | Reserved Instances + Savings Plans | Spot = interruptible; Dedicated Hosts = most expensive |
| Q47 | C | geographic location for RDS deployment | Choose deployment region | AWS Regions | Wavelength = 5G edge; Direct Connect = physical connection |
| Q48 | B | cost estimate before deployment | Pre-deployment cost planning | AWS Pricing Calculator | Free Tier = free usage; Cost Explorer = historical |
| Q49 | A | global, minimal latency, images/videos | Global content delivery | Amazon CloudFront | S3 replication = copies data not edge-caches; VPN = security |
| Q50 | C | economies of scale benefit | Cloud computing benefit | Lower variable costs | Fixed expense is traded for variable |
| Q51 | C | define cloud resources as code, programming language | IaC with programming languages | AWS CDK | CLI = commands; CloudFormation = JSON/YAML templates |
| Q52 | C | temporary credentials, multiple AWS APIs | Temporary authentication | AWS STS | IAM users = permanent; API Gateway = API management |
| Q53 | A | CSPM, aggregates alerts, standardized format | Security posture management | AWS Security Hub | GuardDuty = threat detection; EventBridge = event routing |
| Q54 | B | always free | Free service | IAM | S3, ELB, WAF all have costs |
| Q55 | C | NoSQL, auto scale throughput | Managed NoSQL | Amazon DynamoDB | Aurora = relational; Redshift = analytics |
| Q56 | C | DynamoDB, customer responsibility | Shared responsibility, DynamoDB | Manage database access permissions | Patching, hosting = AWS responsibility |
| Q57 | C | test environment, interruptible, not continuous | Non-critical, interruptible | Spot Instances | On-Demand = no commitment; Reserved = long-term |
| Q58 | A | sensitive data in S3, PII | Data classification in S3 | Amazon Macie | Inspector = EC2 vulnerabilities; GuardDuty = threats |
| Q59 | A, C | block network traffic | Network blocking | Security Groups + Network ACLs | VPC Flow Logs = logging only; CloudTrail = API logging |
| Q60 | B | identify when EC2 was terminated | Event identification | AWS CloudTrail | CloudWatch = metrics; Compute Optimizer = rightsizing |
| Q61 | D | MySQL-compatible, fully managed | Compatible managed database | Amazon Aurora | DynamoDB = NoSQL; Redshift = data warehouse |
| Q62 | C | hybrid, extend AWS to on-premises | Hybrid architecture | AWS Outposts | Snowmobile = large data migration; Fargate = containers |
| Q63 | C | PostgreSQL, OLTP, managed | Managed relational database | Amazon RDS | DynamoDB = NoSQL; Athena = serverless queries |
| Q64 | B, C | Windows virtual desktops, remote access, secure | Virtual desktops | Amazon AppStream 2.0 + Amazon WorkSpaces | ECS = containers; VPN = connectivity |
| Q65 | A | misconfigured security groups, unrestricted ports | Security group monitoring | AWS Trusted Advisor | CloudWatch = metrics; GuardDuty = threats |
| Q66 | A | key-value database, sub-millisecond latency | High-performance NoSQL | Amazon DynamoDB | Aurora = relational; Neptune = graph |
| Q67 | B | ML workload, months, no specific time, lowest cost | Interruptible ML compute | Spot Instances | On-Demand = no long-term discount; Reserved = commitment |
| Q68 | B, C | disaster recovery, EC2 | DR solutions for EC2 | AMIs + EBS Snapshots | Reserved Instances = pricing; Shield = DDoS |
| Q69 | B | CLI from web browser, pre-authenticated | Browser-based CLI | AWS CloudShell | Cloud9 = IDE; WorkSpaces = virtual desktop |
| Q70 | B | hundreds of VPCs, Direct Connect, scale | Simplify multi-VPC connectivity | AWS Transit Gateway | VPC endpoints = private service access; Route 53 = DNS |
| Q71 | D | operational readiness, product launch, no additional charge | Event management support | AWS Enterprise Support | Business Support offers IEM for additional fee |
| Q72 | B | schedule credential rotation, least overhead | Automatic credential rotation | AWS Secrets Manager | Systems Manager Parameter Store = config storage, no auto-rotation |
| Q73 | C | on-premises to cloud, private connection | Private dedicated connection | AWS Direct Connect | PrivateLink = within AWS; VPN = encrypted over public internet |
| Q74 | C | EBS encryption | EBS encryption key management | AWS KMS | ACM = SSL/TLS certs; Systems Manager = operational |
| Q75 | A | manage AWS services via web interface | AWS management interface | AWS Management Console | CLI = command line; SDK = programming |
| Q76 | B, C | advantages of AWS Cloud | Cloud advantages | Economies of scale + Go global in minutes | Variable expenses REPLACE capital; hardware management is reduced not eliminated |
| Q77 | D | withstand failures, minimal downtime | Architecture resilience | High availability | Agility = speed; Elasticity = scaling; Scalability = capacity |
| Q78 | D | repeatable infrastructure, dev and prod | IaC for environments | AWS CloudFormation | CodeDeploy = app deployment; Shield = security |
| Q79 | B | customer responsibility | Shared responsibility | Configure firewalls and networks | AWS patches RDS OS; AWS maintains physical |
| Q80 | B | highly available, fast failover, multi-region | Global application performance | AWS Global Accelerator | WAF = web filtering; Direct Connect = private connection |
| Q81 | C | ecommerce apps, send messages each other | App messaging | Amazon SQS | Auto Scaling = capacity; Kinesis = streaming |
| Q82 | A, C | consolidated billing benefits | AWS Organizations billing | Volume discounts + One bill | Installment payment = not a feature |
| Q83 | D | review S3 ACLs and bucket policies | S3 access review | Access Analyzer for S3 | S3 Lens = storage metrics; IAM Identity Center = SSO |
| Q84 | A | compliance reports about AWS | Compliance documentation | AWS Artifact | Inspector = vulnerability; Marketplace = software |
| Q85 | A | deploy app close to end users | CDN/edge deployment | Amazon CloudFront | Auto Scaling = capacity; AppSync = mobile sync |
| Q86 | C | network performance, AWS global network | Global network optimization | AWS Global Accelerator | Transit Gateway = VPC connectivity; VPC = networking |
| Q87 | A | highly durable object storage | Object storage durability | Amazon S3 | EFS = file system; EBS = block storage |
| Q88 | D | EC2 with database, AWS responsibility | Shared responsibility, EC2 | OS installations (hypervisor/AMI) | Database backups, patches = customer responsibility |
| Q89 | B, D | advantages of AWS Cloud | Cloud migration benefits | Pay-as-you-go + No capacity guessing | Security responsibility shared, not transferred |
| Q90 | C | hybrid cloud storage, on-premises access to cloud | Hybrid storage bridge | AWS Storage Gateway | DataSync = one-time data migration; EBS = block storage |
| Q91 | A | cost estimates for AWS use cases | Pre-migration cost estimate | AWS Pricing Calculator | Budgets = alerts; Cost Explorer = historical analysis |
| Q92 | A | integrate AWS features into application | Developer tool | AWS Software Development Kit (SDK) | CodeDeploy = deployment; Lambda = serverless |
| Q93 | C | Well-Architected design principle | Best practice | Learn from operational failures | Monolithic = bad; manual config = bad |
| Q94 | C | grant only required permissions | IAM concept | Least privilege access | Restricted access = too vague; token access = mechanism |
| Q95 | D | firewall at subnet level | Subnet-level firewall | Network ACL | Security Group = instance level; WAF = Layer 7 web |
| Q96 | B | data warehouse, no manage infrastructure | Serverless data warehouse | Amazon Redshift Serverless | Aurora = relational DB; Lambda = functions |
| Q97 | B, E | reduce costs, cloud computing | Cost reduction | Adjust capacity on demand + Eliminate data center costs | AWS does NOT offer discounts for idle EC2; data transfer OUT has cost |
| Q98 | B | grant access across AWS accounts | Cross-account access | IAM Role | IAM group = user grouping; IAM tag = metadata |
| Q99 | C | AWS responsibility | Shared responsibility | Maintenance of physical and environmental controls | App patches, security groups, IAM = customer |
| Q100 | D | automate infrastructure, scale across regions | IaC at scale | AWS CloudFormation | Config = compliance tracking; Trusted Advisor = recommendations |
| Q101 | A | CAF platform perspective capability | CAF capability | Data architecture | Data protection = Security; Data governance = Governance |
| Q102 | B | most cost-effective architecture | Cloud best practice | Rightsizing | Loose coupling = architecture; Redundancy = reliability |
| Q103 | B | tape library backup, no workflow change | Extend tape library to cloud | AWS Storage Gateway | EBS = block storage; Lambda = functions |
| Q104 | B | plan service usage, set alerts | Budget planning tool | AWS Budgets | Cost Explorer = visualization; Cost and Usage Report = raw data |
| Q105 | B, C | customer responsibilities | Shared responsibility | Client-side encryption + Configure IAM | AWS establishes global infrastructure; patches RDS |
| Q106 | A, E | security best practices for new developer | IAM security | Least privilege + minimum password length | Never share root; never grant admin to developers |
| Q107 | B | multiple accounts, compute, billing discounts | Multi-account billing | Consolidated Billing (Organizations) | Pay-as-you-go = no discount commitment; Spot = interruptible |
| Q108 | C | EC2 to AWS services, secure access | EC2 service access | IAM Roles | Security groups = network; Firewall Manager = WAF rules across accounts |
| Q109 | A | Windows file server, fully managed | Windows file system | Amazon FSx | EKS = Kubernetes; ECS = containers |
| Q110 | D | NFS workload migration | Storage Gateway type for NFS | Amazon S3 File Gateway | Tape Gateway = tape backup; FSx File Gateway = Windows SMB |
| Q111 | C | track API activity, when API call made | API monitoring | AWS CloudTrail | CloudWatch = metrics; Inspector = vulnerabilities |
| Q112 | C | uninterruptible, SQS processing, years | Long-term continuous workload | Savings Plans | Spot = interruptible; On-Demand = most expensive long-term |
| Q113 | B | product recommendations, customer data | ML personalization | Amazon Personalize | Polly = text-to-speech; Rekognition = image analysis |
| Q114 | B | identify capability gaps, CAF | CAF phase | Align | Envision = outcomes; Launch = pilots; Scale = expand |
| Q115 | B | SQL injections, cross-site scripting | Web application protection | AWS WAF | Inspector = vulnerabilities; GuardDuty = threats |
| Q116 | A | create, test, manage EC2 AMIs | AMI automation | EC2 Image Builder | AMI itself = template; Beanstalk = PaaS |
| Q117 | B | continuous vulnerability scanning, EC2 | Automated security assessment | Amazon Inspector | GuardDuty = threat detection; Detective = investigation |
| Q118 | B | weekly, 5-hour processing | Weekly compute workload | Amazon EC2 | Lambda = 15 min limit; CodeDeploy = deployment |
| Q119 | C | inbound/outbound traffic logs, VPC | Network traffic logging | VPC Flow Logs | CloudTrail = API logs; IAM = access control |
| Q120 | A | centralized config and secrets, cost-effective | Config/secret storage | AWS Systems Manager Parameter Store | Secrets Manager = auto-rotation (costs more); Config = compliance |
| Q121 | C | full control of compute resources, containers | Containers with full control | Amazon EC2 | Fargate = serverless containers; EKS = Kubernetes managed |
| Q122 | D | create accounts, group accounts, apply policies | Multi-account management | AWS Organizations | IAM = user access; CloudFormation = IaC |
| Q123 | C | store/retrieve S3 files, industry-standard file protocols | S3 via file protocols | Amazon S3 File Gateway | DataSync = migration; Snowball = offline migration |
| Q124 | A | block SQL injection | Web attack prevention | AWS WAF | NACLs = IP filtering; Security Groups = instance firewall |
| Q125 | A | unified tool, consistent AWS interaction | CLI tool | AWS CLI | ECS = containers; VPN = connectivity |
| Q126 | C | evaluate AWS, best practice in 5 categories | AWS account assessment | AWS Trusted Advisor | Shield = DDoS; WAF = web attacks |
| Q127 | B | configuration management, patch management, CAF | CAF operations capability | Operations perspective | Platform = tech architecture; Security = identity |
| Q128 | B, D | steady, predictable, uninterruptible | Long-term, cost-effective | Reserved Instances + Savings Plans | Spot = interruptible; Dedicated Hosts = expensive |
| Q129 | A | once a year, 24 hours, uninterruptible | Short infrequent workload | On-Demand Instances | Reserved = requires year+ commitment; Spot = interruptible |
| Q130 | C | shared control, AWS + customer | Shared responsibility | Patch management | Physical security = AWS only; data = customer only |
| Q131 | B, E | migrate workloads, chargeback to departments | Cost separation | Consolidated Billing + Multiple AWS Accounts | Edge locations = CDN; Config = compliance |
| Q132 | D | AWS responsibility | Shared responsibility | Apply updates to Nitro Hypervisor | Client-side encryption, IAM = customer |
| Q133 | B | benefit of AWS Cloud | Cloud benefit | Pay-as-you-go pricing | Fixed expense increases; agility = speed not pricing |
| Q134 | C | CAF business perspective capability | CAF business | Data monetization | Culture evolution = People; Event management = Operations |
| Q135 | C | Enterprise vs Business Support additional benefit | Enterprise Support benefit | Designated Technical Account Manager (TAM) | Full Trusted Advisor = Business+; 24/7 phone = Business+ |
| Q136 | C | interrupt running EC2 if capacity unavailable | Pricing model with interruption | Spot Instances | On-Demand = no interruption; Reserved = committed |
| Q137 | C, D | CAF security perspective capabilities | CAF security | Incident response + Infrastructure protection | Observability = Operations; Availability = Operations |
| Q138 | C | run EC2 for 1+ year, discounted hourly rate | Long-term EC2 commitment | EC2 Instance Savings Plans | Graviton = processor type; Auto Scaling = capacity |
| Q139 | B | eliminate underutilized CPU | Cloud characteristic | Elasticity | Agility = speed; Reliability = uptime; Durability = data persistence |
| Q140 | B, E | loosely coupled architecture | Decoupling services | Amazon SQS + AWS Step Functions | WorkSpaces = virtual desktop; Trusted Advisor = recommendations |
| Q141 | A | custom spending threshold alerts | Budget alerts | AWS Budgets | Cost Explorer = analysis; Organizations = multi-account |
| Q142 | A | define and track business outcomes, CAF governance | CAF governance capability | Benefits management | Risk management = Governance too but less specific; Portfolio = Platform |
| Q143 | B | quickly and securely move files, long distances, S3 | Fast S3 uploads | S3 Transfer Acceleration | Versioning = protection; ACLs = access control |
| Q144 | A | run 12 hours, stop after, experimental | Short experimental workload | On-Demand Instances | Spot = interruptible; Reserved = long commitment |
| Q145 | B | CAF phase, accelerate business outcomes | CAF transformation phase | Envision | Align = gaps; Launch = pilots; Scale = expand |
| Q146 | B | customer responsibility, S3 data | Customer responsibility | Application data security | Maintenance of hardware = AWS; VPC components = AWS |
| Q147 | A | EC2 in geographic disaster areas, high availability | Multi-region resilience | EC2 instances in multiple AWS Regions | CloudFront locations = edge, not compute HA |
| Q148 | D | monolith to microservices, migrate to AWS | Migration strategy | Refactor | Rehost = lift and shift; Replatform = some optimization |
| Q149 | C | IAM user, access key instead of password | Access key purpose | Access through CLI | Root user = different; Management Console = password |
| Q150 | B | environment with one or more data centers | AWS infrastructure component | Availability Zone | VPC = virtual network; Outposts = on-premises extension |
| Q151 | A | 50 petabytes, least operational overhead | Large data migration | AWS Snowmobile | Snowball Edge = up to 210TB; DMS = database migration |
| Q152 | A | lightweight laptops, robust app, no high-end hardware | Stream desktop apps to browser | Amazon AppStream 2.0 | Beanstalk = app deployment; WorkSpaces = full virtual desktop |
| Q153 | D | query server logs, cost-effective storage | Log storage | Amazon S3 | Aurora = relational DB; EBS = block storage |
| Q154 | D | recommended design principle | Well-Architected principle | Avoid monolithic architecture | Tight coupling = bad practice |
| Q155 | A | audit API activity | API audit | AWS CloudTrail | WAF = web filtering; Config = configuration compliance |
| Q156 | A | customer responsibility, guest OS | Shared responsibility | Management of guest operating systems | Host OS, virtualization = AWS responsibility |
| Q157 | D | automatically add/remove EC2, varying workloads | Dynamic scaling | Amazon EC2 Auto Scaling | Spot = pricing; Snow = data migration |
| Q158 | C | automate credential rotation, least management | Credential rotation | AWS Secrets Manager | CloudHSM = hardware key management; KMS = encryption keys |
| Q159 | B | recognize and classify sensitive data | Data classification | Amazon Macie | GuardDuty = threats; Inspector = vulnerabilities |
| Q160 | C, D | root user best practices | Root user security | Enable MFA + Create IAM user for daily tasks | Root user should never be shared or used for daily tasks |
| Q161 | D | critical RDS, high availability, < 5 min recovery | RDS high availability | Multi-AZ deployment | Read replicas = performance; snapshots = backup |
| Q162 | A | EC2, 1 year continuous, most cost-effective | Year-long commitment | Reserved Instances | Spot = interruptible; On-Demand = no discount |
| Q163 | A | S3 to on-premises transfer, security responsibility | Data security responsibility | The company (customer) | AWS secures infrastructure; customer secures data |
| Q164 | B | recover from infrastructure disruptions, acquire resources | Well-Architected pillar | Reliability | Security = protection; Performance = efficiency |
| Q165 | D | identify S3 buckets shared with other accounts | External access check | IAM Access Analyzer | Lake Formation = data lake; CloudWatch = metrics |
| Q166 | C | interactive BI dashboards, ML insights | Business intelligence | Amazon QuickSight | Athena = queries; Kendra = search; Redshift = warehousing |
| Q167 | B | scale infrastructure based on demand | Cloud value proposition | Resource elasticity | Decoupled architecture = design principle |
| Q168 | B | access sensitive S3 data, security best practice | S3 access best practice | IAM roles for applications | CRR = replication; WAF = web filtering |
| Q169 | D | agility advantage | Cloud agility | Provision and deprovision resources quickly | Pay-as-you-go = cost; multi-region = availability |
| Q170 | C | SAML 2.0, central user portal | SSO for third-party apps | AWS IAM Identity Center | IAM = user management; Cognito = mobile/web users |
| Q171 | D | AWS service availability and operations | Service status | AWS Health Dashboard | EventBridge = events; Service Catalog = product catalog |
| Q172 | A | inbound/outbound VPC traffic capture | VPC network logging | VPC Flow Logs | Inspector = vulnerabilities; NAT = network translation |
| Q173 | C | customer always responsible for | Shared responsibility constant | Customer data | Networking, encryption keys = can be managed by either |
| Q174 | B | compliance reports on demand | Compliance on-demand | AWS Artifact | Secrets Manager = credentials; Security Hub = aggregation |
| Q175 | C | check EC2 vulnerabilities using templates | Automated assessment | Amazon Inspector | WAF = web; Trusted Advisor = general recommendations |
| Q176 | C | on-premises info: hostname, IP, MAC | Migration discovery | AWS Application Discovery Service | DataSync = data transfer; DMS = database migration |
| Q177 | C | increase security | Security best practice | Rotate access keys regularly | Programmatic access for all = risk; inline policies = harder to manage |
| Q178 | A | analyze and assess readiness for migration | Migration readiness | AWS Cloud Adoption Framework (AWS CAF) | Pricing Calculator = costs; Well-Architected = architecture |
| Q179 | B | Amazon S3 core functionality | S3 description | Object storage, high performance, security, scalability | S3 is NOT block storage or file system |
| Q180 | C | on-demand, replace fixed expenses | Cloud pricing benefit | Pay-as-you-go pricing | High availability = architecture; economies of scale = cost reduction |
| Q181 | A, C | connect on-premises to VPC | Network connectivity | AWS VPN + AWS Direct Connect | VPC peering = VPC-to-VPC; CloudFront = CDN |
| Q182 | B | nonrelational database, no manage hardware | Managed NoSQL | Amazon DynamoDB | Aurora = relational; Redshift = analytics |
| Q183 | B, C | rightsize AWS resources | Rightsizing actions | EC2 instance types based on utilization + S3 Lifecycle policies | Multi-AZ = high availability not rightsizing |
| Q184 | B | apply security rules to specific EC2 instances | Instance-level security | Security groups | Network ACLs = subnet level; WAF = web layer |
| Q185 | C, E | reliability pillar design principles | Reliability principles | Scale to meet demand + Recover from failure automatically | Traceability = Security; Global deployment = Performance |
| Q186 | A | 2TB transfer, no cost | Free data transfer | Inbound data transfer from internet | Outbound to internet = cost; between AZs = may cost |
| Q187 | C | reuse templates, deploy multiple resources | Template-based infrastructure | AWS CloudFormation | Marketplace = software; AMI = EC2 image |
| Q188 | D | send/store/receive messages, FIFO order | Message queue with ordering | Amazon SQS (FIFO) | Step Functions = workflow; SNS = pub/sub; Kinesis = streaming |
| Q189 | D | browser-based, pre-authenticated, from Console | Browser CLI | AWS CloudShell | Lightsail = simple apps; Cloud9 = IDE |
| Q190 | B, E | PostgreSQL-compatible managed service | Managed PostgreSQL | Amazon RDS + Amazon Aurora | DynamoDB = NoSQL; Athena = query |
| Q191 | D | cargo ships, intermittent connectivity, edge computing | Edge computing, offline | AWS Snowball Edge | IoT Core = connected devices; Storage Gateway = hybrid |
| Q192 | B | EC2 to SNS permission | EC2 service access | IAM Roles | ACM = SSL certs; Security Hub = aggregation |
| Q193 | B | limited knowledge, quickly deploy Node.js | Fast PaaS deployment | AWS Elastic Beanstalk | CloudFormation = IaC templates; OpsWorks = Chef/Puppet |
| Q194 | A | CDN, global, low latency, secure | Content delivery | Amazon CloudFront | ELB = load balancing within region |
| Q195 | D | third-party software for AWS workload | Software purchasing | AWS Marketplace | Resource Access Manager = sharing; License Manager = licenses |
| Q196 | C | SMB protocol, highly reliable, scalable file storage | Windows file system | Amazon FSx for Windows File Server | EFS = Linux NFS; EBS = block storage |
| Q197 | A | centrally configure VPC security groups, multiple accounts | Cross-account security rules | AWS Firewall Manager | GuardDuty = threats; Detective = investigation |
| Q198 | D | AWS responsibility | Shared responsibility | Maintain physical hardware | IAM, security groups, encryption = customer |
| Q199 | B | EC2 in private subnet, OS updates, no internet access | Private subnet internet access | NAT Gateway | VPC endpoint = AWS services; PrivateLink = private services |
| Q200 | A, D | AWS responsibilities | Shared responsibility | Securing virtualization layer + Patching RDS OS | Security groups, IAM = customer |
| Q201 | B | infrequent data, 12-hour retrieval, cost-effective | Archival with moderate retrieval | S3 Glacier Flexible Retrieval | One Zone-IA = lower durability; Standard-IA = fast retrieval costs more |
| Q202 | D | services used in date range | Access analysis | IAM Access Analyzer | S3 ACLs = bucket access; ACM = certificates |
| Q203 | D | engage third-party consultants for AWS | Partner network | AWS Partner Network (APN) | Service Catalog = product catalog; Organizations = accounts |
| Q204 | C | QuickSight dashboards from billing data | Billing data export | AWS Cost and Usage Report | Budgets = alerts; Anomaly Detection = ML-based |
| Q205 | A | cloud-based storage, locally cached, on-premises replacement | Hybrid cloud storage | AWS Storage Gateway | Snowcone = small edge device; Backup = centralized backup |
| Q206 | B | organize resources, track costs at detailed level | Cost tagging | Tags + Cost allocation tags | CloudWatch dashboards = monitoring; Billing = high level |
| Q207 | D | plan, schedule, run hundreds of thousands of computing jobs | Batch processing | AWS Batch | Step Functions = workflow; SQS = messaging |
| Q208 | A, D | high availability, low latency, failover across regions | Global failover | Amazon Route 53 + AWS Global Accelerator | NLB, ALB = single region; S3 Transfer Acceleration = S3 only |
| Q209 | A | Auto Scaling, scale capacity | Auto Scaling function | Scale number of EC2 in/out | Scaling size up/down = vertical scaling |
| Q210 | B, D | benefits of AWS Cloud | Cloud benefits | Deploy globally in minutes + Economies of scale | Capital expenses INCREASE; hardware management stays needed |
| Q211 | D | DDoS, always-on detection, automatic mitigation | DDoS protection | AWS Shield | WAF = web attacks; ELB = load balancing |
| Q212 | C | model and provision using programming languages | IaC with code | AWS CDK | CloudFormation = YAML/JSON; Systems Manager = operational |
| Q213 | D | up to 90% discount | Cheapest EC2 option | Spot Instances | Reserved = up to 72%; Savings Plans = up to 72% |
| Q214 | B | instance-level firewall | Instance firewall | Security groups | Network ACL = subnet level; Trusted Advisor = recommendations |
| Q215 | D | develop, test, launch quickly | Cloud computing advantage | Increase speed and agility | Economies of scale = cost; capacity guessing = planning |
| Q216 | B | manage permissions as employees change teams | Permission management | IAM Roles | IAM groups = static groupings; individual policies = overhead |
| Q217 | B | store and encrypt database passwords | Password storage | AWS Secrets Manager | Shield = DDoS; IAM = access control |
| Q218 | C | retrieve security/compliance docs, submit to auditor | Compliance documentation | AWS Artifact | Inspector = vulnerabilities; Systems Manager = operational |
| Q219 | A, B | encrypt objects at rest in S3 | S3 encryption types | SSE-S3 + SSE-KMS | TLS/SSL = in-transit encryption; TDE = database encryption |
| Q220 | C | social media login credentials integration | Identity federation | Amazon Cognito | Directory Service = Active Directory; IAM = AWS access |
| Q221 | B | track, record, audit configuration changes | Configuration compliance | AWS Config | Shield = DDoS; Inspector = vulnerabilities |
| Q222 | B | Linux EC2, 3h 5min 6sec billing | EC2 billing precision | Billed per second for Linux | Linux billed per second after first minute |
| Q223 | C | DDoS protection for website | DDoS protection | AWS Shield | Resource Access Manager = sharing; Amplify = web apps |
| Q224 | D | customize assessment, projected running costs | Migration cost assessment | Migration Evaluator | Trusted Advisor = best practices; Inspector = security |
| Q225 | A | centrally manage AWS environments, automate accounts, SCPs | Multi-account governance | AWS Organizations | Cost Explorer = cost; Budgets = alerts |
| Q226 | A, D | verify AWS services operating normally | AWS service health | AWS Personal Health Dashboard + AWS Service Health Dashboard | Systems Manager = operational; Trusted Advisor = recommendations |
| Q227 | C | migrate PostgreSQL to RDS | Database migration | AWS Database Migration Service (DMS) | Migration Hub = tracking; Application Migration = server migration |
| Q228 | B | AWS Compute Optimizer | Cloud concept demonstrated | Rightsizing | Elasticity = scaling; Global reach = geography |
| Q229 | B | identify sensitive data, S3 | Sensitive data detection | Amazon Macie | Inspector = vulnerabilities; IAM = access control |
| Q230 | B | stateful workload, 3 years | Long-term workload | Reserved Instances | Spot = interruptible; On-Demand = no long-term discount |
| Q231 | B | enable EBS encryption | Who enables EBS encryption | AWS customers | KMS manages keys but customer enables encryption |
| Q232 | B | AWS CloudTrail purpose | CloudTrail function | Record API calls | CloudTrail is NOT for patching or compliance checking of config |
| Q233 | C | requires customer to update/patch guest OS | Customer OS responsibility | Amazon EC2 | DynamoDB, S3, Aurora = fully managed |
| Q234 | C | resources shared externally | External sharing detection | AWS IAM Access Analyzer | OpenSearch = search; Fargate = containers |
| Q235 | B | retain full control of patch management | Customer-managed patching | Amazon EC2 | Lambda, RDS = AWS manages OS |
| Q236 | D | support concierge | Concierge access support level | AWS Enterprise Support | Business = no concierge; Developer = basic |
| Q237 | C | visually design serverless applications | Serverless visual design | AWS Application Composer | Lambda = serverless execution; Batch = batch jobs |
| Q238 | D | same security software as on-premises | Third-party software | AWS Marketplace | Support Center = technical help; Management Console = UI |
| Q239 | C | AWS responsibility for EC2 | Shared responsibility, EC2 | Configuration of infrastructure devices | Security groups, OS = customer; encryption = customer choice |
| Q240 | D | PostgreSQL, infrequent use, least overhead | Serverless, infrequent database | Amazon Aurora Serverless | RDS = still requires provisioning; EC2 = most overhead |
| Q241 | D, E | DynamoDB, AWS responsibilities | Shared responsibility, DynamoDB | Provide endpoints + Manage infrastructure/OS | Data classification, access = customer |
| Q242 | C | globally accessible ecommerce, scalable DNS | DNS for global app | Amazon Route 53 | EC2 = compute; VPC = networking |
| Q243 | D | customer maintenance task | Customer responsibility | EC2 updates and security patches | Physical, hardware, network switch = AWS |
| Q244 | D | improve security posture, user activity API calls | API activity review | AWS CloudTrail | WAF = web; Detective = investigation |
| Q245 | D | experimental workloads, 3-6 months | Short-term, experimental | On-Demand Instances | Savings Plans = 1-3 year; Dedicated = physical server |
| Q246 | B | Enterprise Support, new product launch, no extra charge | Event management | AWS Infrastructure Event Management (IEM) | Basic/Developer/Business = IEM available for extra fee |
| Q247 | A | separate and track costs per business unit | Cost separation | AWS Organizations (one account per unit) | DynamoDB = database; Billing console = view only |
| Q248 | B | time-series database, trillions of events | Time-series data | Amazon Timestream | Neptune = graph; Forecast = predictions |
| Q249 | A | shared control between AWS and customer | Shared responsibility | Configuration management | Physical controls = AWS only; IAM = customer only |
| Q250 | A | stateless workloads, unused EC2 capacity | Optimize unused capacity | Spot Instances | Dedicated = physical isolation; Reserved = commitment |
| Q251 | D | rarely accessed, can be regenerated, lowest cost | Cheapest S3 class with risk | S3 One Zone-IA | Intelligent-Tiering = unknown patterns; Glacier = archival |
| Q252 | C | adopt AWS at scale, operational support | Operational support | AWS Managed Services (AMS) | CAF = framework; Well-Architected = architecture review |
| Q253 | D | Typescript, Python, Java, .NET | IaC with programming languages | AWS CDK | CloudFormation = YAML/JSON; CLI = commands |
| Q254 | D | always-up, right-sized, 1 year, most savings | Maximum cost savings for 1 year | Standard Reserved Instances | Convertible = flexible instance type but less discount |
| Q255 | D | tape library running out of space | Extend tape to cloud | AWS Storage Gateway | EFS = NFS file system; S3 = object storage |
| Q256 | A | Free Tier expires or usage exceeded | Free Tier behavior | Standard pay-as-you-go rates | Account is NOT frozen; no penalty for prior usage |
| Q257 | D | monitor workload performance, cloud services meet business needs | CAF perspective | Operations | Business = outcomes; Platform = technology |
| Q258 | A | identify transformation opportunities, evaluate readiness | Migration strategy | AWS CAF | AMS = operations; Well-Architected = architecture |
| Q259 | D | baseline of on-premises, projected costs for cloud | Migration cost baseline | Migration Evaluator | Compute Optimizer = rightsizing existing; Cost Explorer = historical |
| Q260 | B | consolidate billing for two accounts | Billing consolidation | AWS Organizations | Systems Manager = operational; License Manager = licenses |
| Q261 | C | workloads perform intended functions, recover quickly | Well-Architected pillar | Reliability | Performance efficiency = resource use; Security = protection |
| Q262 | B | ETL data, managed | ETL service | AWS Glue | Athena = query; S3 = storage |
| Q263 | C | petabytes, no internet connection | Large offline data migration | AWS Snowmobile | DataSync = network-based; Direct Connect = private network |
| Q264 | C | receive alerts for overall operating costs | Cost alerts | AWS Budgets | EventBridge = events; Savings Plans = pricing |
| Q265 | C | Enterprise Support Concierge team | Concierge function | Billing and account inquiries | Concierge does NOT do architecture or technical support |
| Q266 | B | 3-year simulation, no interruption | Long-term uninterrupted | Reserved Instances | Spot = interruptible; Dedicated Hosts = expensive |
| Q267 | C | spending commitment, discounts | Commitment-based discounts | Savings Plans | Detective = security; Pricing Calculator = estimates |
| Q268 | B, C | Well-Architected pillars | Framework pillars | Performance efficiency + Cost optimization | High availability, continuous development = NOT pillars |
| Q269 | C | EC2, worldwide, minimize latency | Global content delivery with EC2 origin | CloudFront with EC2 as source | Multiple AZs = regional HA; multiple accounts = billing |
| Q270 | C | remote locations, no internet, capture data | Edge data collection | AWS Snow Family | Outposts = on-premises cloud extension; Transfer Family = SFTP |
| Q271 | D, E | benefits when moving on-premises to AWS | Migration benefits | High availability + Economies of scale | AWS trains staff = false; TAMs = paid support |
| Q272 | A | stateless services, short-term, lowest cost | Short-term stateless | Spot Instances | On-Demand = more expensive; Reserved = commitment |
| Q273 | B, D | Trusted Advisor benefits | Trusted Advisor features | Cost optimization recommendations + Security checks | SQS access, IAM approval = not Trusted Advisor functions |
| Q274 | B | archive infrequently accessed data | S3 cost saving | S3 Lifecycle | Versioning = protection; Object Lock = compliance; Inventory = reporting |
| Q275 | D | use Regions to increase availability globally | Cloud computing advantage | Global reach | Pay-as-you-go = cost; economies of scale = cost |
| Q276 | D | 10TB, intermittent connectivity | Edge data processing | AWS Snowball Edge | DMS = database; DataSync = network migration |
| Q277 | B | operational excellence design principle | Well-Architected principle | Make frequent, small, reversible changes | Going global = Performance; hardware = cost |
| Q278 | D | serverless computing benefit | Serverless benefit | Management of infrastructure offloaded to AWS | Security responsibility still shared; monitoring still needed |
| Q279 | C | temporary security credentials, AWS users | Temporary credentials | AWS STS | IAM policies = permissions; IAM groups = user grouping |
| Q280 | D | SQL injection, detailed logging | Web application firewall with logging | AWS WAF | Network Firewall = VPC; RDS = database; GuardDuty = threats |
| Q281 | D | 12 months, active at all times | Year-long, no interruption | Reserved Instances | On-Demand = more expensive; Spot = interruptible |
| Q282 | C, D | customer responsibilities | Shared responsibility | Guest OS config + Encryption options | Infrastructure config, hardware = AWS |
| Q283 | B | verify MFA for all users | MFA status check | IAM Credential Reports | Cost and Usage = billing; Artifact = compliance docs |
| Q284 | D | manage security alerts, single dashboard | Security aggregation | AWS Security Hub | GuardDuty = threats; Inspector = vulnerabilities; Macie = data |
| Q285 | B | run workloads effectively, reduce management overhead | Well-Architected pillar | Operational excellence | Reliability = recovery; Cost optimization = spending |
| Q286 | C | monitor S3 for PII, immediate alert | PII detection in S3 | Amazon Macie | GuardDuty = threats; Detective = investigation |
| Q287 | C | download security and compliance reports | On-demand compliance | AWS Artifact | Security Hub = aggregation; Shield = DDoS |
| Q288 | C | IAM users list, credential status | Credential audit | IAM Credential Report | Trusted Advisor = best practices; Management Console screenshots = manual |
| Q289 | A | security group task | Security group use | Allow access through specific port only | Security groups cannot deny; they only allow |
| Q290 | A | GPU workloads | EC2 instance type | Accelerated computing instances | Compute optimized = CPU-intensive but no GPU |
| Q291 | A, D | network ACL features | NACL characteristics | Stateless + Process rules in order (lowest number first) | Security groups = stateful; NACLs = stateless |
| Q292 | B, C | CAF platform perspective capabilities | CAF platform | Data engineering + CI/CD | Infrastructure protection = Security; Change management = Operations |
| Q293 | B | apply latest security patches | Customer responsibility | Amazon EC2 instances | DynamoDB, RDS, S3 = AWS manages OS |
| Q294 | D | unknown access patterns, cost-effective | S3 storage for unknown patterns | S3 Intelligent-Tiering | Standard = frequent access; One Zone-IA = risk |
| Q295 | C, D | CAF security perspective capabilities | CAF security | Incident response + Infrastructure protection | Observability = Operations; Availability = Operations |
| Q296 | B | managed policy insufficient | IAM solution | Create a custom IAM policy | Shield = DDoS; KMS = encryption |
| Q297 | B | who manages IAM access keys rotation | Key rotation responsibility | The customer | AWS does NOT auto-rotate keys |
| Q298 | C | run pre-installed third-party firewall on EC2 | Third-party software | AWS Marketplace | NACLs = AWS network; Security groups = AWS network |
| Q299 | C | quickly deploy cloud resources, minutes | Cloud benefit | Agility | Elasticity = scaling; Reliability = uptime |
| Q300 | D | entirely AWS responsibility | Pure AWS responsibility | Physical and environmental controls | Password policy, IAM, guest OS = customer |
| Q301 | C | root user characteristic | Root user description | First sign-in identity when account created | MFA can be set for all users; Management Console accessible to all |
| Q302 | D | determine what action made EC2 inaccessible | Event investigation | AWS CloudTrail | CloudWatch Logs = application logs; Inspector = vulnerabilities |
| Q303 | A | quickly provision and manage via scripts | Scripted management | AWS CLI | CodeBuild = build; CAF = framework |
| Q304 | C | migrate unstructured data, inflight encryption, validation | Data migration with security | AWS DataSync | Application Migration = server migration; Migration Hub = tracking |
| Q305 | B | deploy multiple test environments, fast, repeatable | Repeatable environment deployment | AWS CloudFormation | EC2 = compute; QuickSight = BI |
| Q306 | D | quickly implement CI/CD pipeline | CI/CD quick setup | AWS CodeStar | Config = compliance; Cognito = identity |
| Q307 | D | AWS Outposts as part of deployment | Deployment model | Hybrid | On-premises = no cloud; Cloud-native = all cloud |
| Q308 | D | fully managed graph database | Graph database | Amazon Neptune | Aurora = relational; FSx = file system |
| Q309 | D | desktop environments for employees | Virtual desktops | AWS WorkSpaces | WAF = web security; Fargate = containers |
| Q310 | A | capture information about network traffic in VPC | Network traffic info | VPC Flow Logs | Inspector = vulnerabilities; Route tables = routing |
| Q311 | B | ephemeral storage, deleted when EC2 stops | Ephemeral storage | EC2 Instance Store | EBS = persistent; EFS = shared file system |
| Q312 | A | Windows file shares from on-premises, no new infrastructure | Windows SMB from on-premises | Amazon FSx File Gateway | DataSync = network migration; Snow = offline migration |
| Q313 | B | durable, static content, lowest cost, infinitely scalable | Object storage | Amazon S3 | EBS = block; Storage Gateway = hybrid |
| Q314 | D | EC2 Auto Scaling based on CPU | Auto Scaling trigger | Amazon CloudWatch alarm | SQS = messages; SNS = notifications |
| Q315 | B | attract digitally fluent workforce, diverse | CAF perspective | People | Business = outcomes; Operations = delivery |
| Q316 | D | migrate on-premises databases to managed cloud | Database migration | AWS DMS | Storage Gateway = storage; DataSync = file migration |
| Q317 | C | Windows workloads, SMB protocol, fully managed | Windows file server | Amazon FSx for Windows File Server | EFS = Linux; FSx for Lustre = HPC |
| Q318 | B | query CSV files in S3, simple query, least overhead | Serverless S3 queries | Amazon Athena | S3 Select = single object query; Redshift = warehouse |
| Q319 | B | no-cost platform, community Q&A | Community Q&A | AWS re:Post | Knowledge Center = FAQ articles; IQ = paid experts |
| Q320 | A | search text in documents stored in S3 | Document search | Amazon Kendra | Rekognition = images; Polly = text-to-speech |
| Q321 | B, C | AWS services using global edge locations | Edge location services | Amazon CloudFront + AWS Global Accelerator | Fargate = containers; Wavelength = 5G edge; VPC = regional |
| Q322 | C | relational database, no manage hardware | Managed relational DB | Amazon RDS for MySQL | ECS = containers; ElastiCache = caching |
| Q323 | B | deploy quickly, minimize AWS resource management complexity | PaaS deployment | AWS Elastic Beanstalk | Config = compliance; Personalize = ML |
| Q324 | A | access AWS services from application code | Developer access | AWS Software Development Kit | Management Console = UI; CodePipeline = CI/CD |
| Q325 | B | security misconfigurations, unexpected behaviors, CAF | CAF security capability | Threat detection | Identity and access = IAM; Platform engineering = Platform |
| Q326 | C | private network connection, corporate network | Private dedicated connection | AWS Direct Connect | Route 53 = DNS; VPC peering = VPC-to-VPC |
| Q327 | C, E | connect two VPCs | VPC connectivity | VPC Peering + AWS Transit Gateway | Route 53 = DNS; Direct Connect = on-premises |
| Q328 | C | text to lifelike voices | Text-to-speech | Amazon Polly | Transcribe = speech-to-text; Rekognition = images |
| Q329 | A | application stacks, pre-configured instances | Simple pre-configured servers | Amazon Lightsail | Athena = queries; Outposts = on-premises |
| Q330 | A, C | Savings Plans supported services | Savings Plans coverage | Amazon EC2 + Amazon SageMaker | RDS, Redshift, DynamoDB = NOT covered by Savings Plans |
| Q331 | C | rightsizing recommendations, no additional cost | Free rightsizing tool | AWS Cost Explorer | Well-Architected Tool = architecture; CloudWatch = metrics |
| Q332 | B | petabyte-scale data warehouse, no manual management | Managed data warehouse | Amazon Redshift | DocumentDB = MongoDB; Neptune = graph |
| Q333 | C | classify books based on content, NLP | Text classification | Amazon Comprehend | Redshift = analytics; CloudSearch = search |
| Q334 | C | AWS responsibility | Shared responsibility | Protection of physical network infrastructure | Encryption, authentication, firewalls = customer |
| Q335 | A, B | CAF cloud transformation recommendations | CAF phases | Envision + Align | Assess, Mobilize, Migrate = AWS MAP phases not CAF |
| Q336 | A | IAM users list, credential status | Credential reporting | IAM Credential Report | IAM Identity Center = SSO; Access Analyzer = external sharing |
| Q337 | C | update components regularly, small reversible changes | Well-Architected pillar | Operational excellence | Security = protection; Reliability = recovery |
| Q338 | A | track tags, buckets, prefixes for S3 objects | S3 object inventory | S3 Inventory Report | S3 Lifecycle = storage tier transitions |
| Q339 | C | authenticate multiple accounts, single credentials | Single sign-on | AWS IAM Identity Center | IAM = user management; Control Tower = governance |
| Q340 | B | control incoming/outgoing network at instance level | Instance network control | Security groups | Shield = DDoS; Network Access Analyzer = analysis |
| Q341 | A | deploy application globally | Global deployment | Multi-Region architecture | Single-Region = limited geography |
| Q342 | C | web application to interact with AWS services | Web-based management | AWS Management Console | CloudShell = browser CLI; Marketplace = software |
| Q343 | A | minimum permissions to perform operations | Least privilege access | AWS IAM | CloudWatch = monitoring; Macie = data classification |
| Q344 | B, C | CAF governance perspective capabilities | CAF governance | Cloud financial management + Application portfolio management | Identity = Security; Innovation = Business |
| Q345 | D | single location to track migration progress | Migration tracking | AWS Migration Hub | Application Discovery = discovery; Service Catalog = product catalog |
| Q346 | A, D | connect to Amazon Linux 2 EC2 | EC2 connection methods | EC2 Instance Connect + Systems Manager Session Manager | RDP = Windows; Batch = batch jobs; Connect = contact center |
| Q347 | D | deploy resources on demand, release when not needed | Cloud architecture concept | Elasticity | High availability = uptime; Resilience = recovery |
| Q348 | B | requires root user sign-in | Root user tasks | Delete an AWS account | IAM user deletion = IAM; EC2 = IAM users can do |
| Q349 | C | S3 Intelligent-Tiering | What it offers | Automatic cost savings based on access patterns | It does NOT pay upfront; NOT for archival |
| Q350 | A | can tolerate interruptions, largest discount | Cheapest interruptible option | Spot Instances | Convertible Reserved = flexibility not cheapest |
| Q351 | A | identify measurable business outcomes | CAF phase | Envision | Align = gaps; Launch = pilots |
| Q352 | A | allow inbound traffic from internet to VPC | VPC component | Internet Gateway | NAT gateway = outbound only; WAF = web filtering |
| Q353 | D | create infrastructure from code | IaC | AWS CloudFormation | EKS = Kubernetes; Outposts = hybrid |
| Q354 | C | well-architected design guideline | Cloud application design | Design for automated recovery from failure | Static data near compute = irrelevant; tightly coupled = bad |
| Q355 | B | 75 petabytes, most cost-effective | Very large data migration | AWS Snowmobile | Snowball Edge = up to 210TB; Direct Connect = network |
| Q356 | B, E | Well-Architected pillars | Framework pillars | Performance efficiency + Operational excellence | Resource scalability, system elasticity = NOT pillars |
| Q357 | C | dedicated, low-latency, consistent network | Dedicated network connection | AWS Direct Connect | Global Accelerator = application; VPN = encrypted but internet |
| Q358 | A, E | sustainability design principles | Sustainability pillar | Maximize EC2 utilization + Reduce user reinstallations | Minimize EC2 = wasteful; managed services = YES |
| Q359 | A, D | lower TCO of computing | Cloud cost advantage | Replace capital with pay-as-you-go + Economies of scale | AWS does NOT eliminate IT staff need; not single pricing model |
| Q360 | C | data must remain on-premises, low latency to AWS | Hybrid on-premises | AWS Outposts | Local Zones = latency but data goes to cloud; Wavelength = 5G |
| Q361 | D, E | serverless AWS services | Serverless | AWS Fargate + AWS Lambda | Outposts = on-premises; EC2 = managed servers; EKS = requires nodes |
| Q362 | C | per-socket, per-core, per-VM software licenses | BYOL licensing | Dedicated Hosts | Dedicated Instances = isolated but no license control; Spot = interruptible |
| Q363 | D | replace impaired EC2 instances | Automated replacement | AWS Auto Scaling | ECS = containers; GuardDuty = threats |
| Q364 | B | on-premises, low-latency access to AWS cloud data | Hybrid storage access | AWS Storage Gateway | CloudFront = CDN; Backup = centralized backup |
| Q365 | B | CloudFront purpose | CDN description | Secure delivery, global, low latency | Auto Scaling = capacity; Route 53 = DNS |
| Q366 | D | deployment and management of applications | PaaS | AWS Elastic Beanstalk | CodeGuru = code review; Fargate = containers |
| Q367 | C | NLP into BI dashboards, ask questions | BI with NLP | Amazon QuickSight Q | Macie = data; Lex = chatbots |
| Q368 | B | backbone network, edge locations, reduce latency to S3 | Fast S3 uploads | S3 Transfer Acceleration | CRR = replication; Event Notifications = triggers |
| Q369 | B | NoSQL database in AWS Cloud | Managed NoSQL | Amazon DynamoDB | Aurora = relational; RDS = relational |
| Q370 | C | relational database, MySQL and PostgreSQL compatible | AWS proprietary relational DB | Amazon Aurora | Redshift = analytics; Neptune = graph |
| Q371 | D | isolate failures between dependent components | Architecture design | Loosely couple components | Monolithic = tightly coupled; automation = operations |
| Q372 | B | deploy applications globally, edge locations | Cloud benefit | Global reach | Economy of scale = cost; Agility = speed |
| Q373 | C | monitor and troubleshoot application logs | Monitoring and logging | Amazon CloudWatch | CloudTrail = API audit; EC2 = compute |
| Q374 | A | AWS Compute Optimizer, sizing recommendations | Sizing recommendations | Amazon EC2 | RDS, Lightsail = not primary Compute Optimizer targets |
| Q375 | B | collect configuration, usage, behavior of on-premises | Migration planning data | AWS Application Discovery Service | Resource Groups = organization; Service Catalog = governance |
| Q376 | B | publishers and subscribers | Pub/sub messaging | Amazon SNS | Lambda = serverless; CloudWatch = monitoring |
| Q377 | A | monthly predicted total AWS cost before migration | Pre-migration cost estimate | AWS Pricing Calculator | Compute Optimizer = rightsizing; Application Migration = migration |
| Q378 | B | monitor AWS resources and applications in real time | Real-time monitoring | Amazon CloudWatch | Trusted Advisor = recommendations; Cost Explorer = cost analysis |
| Q379 | B | CAF business perspective capability | CAF business | Data science | Program management = Governance; Observability = Operations |
| Q380 | A | reduce costs, usage commitment, EC2 | Commitment-based EC2 savings | Compute Savings Plans | Auto Scaling = capacity; On-Demand = no commitment discount |
| Q381 | D | data and analytics architecture | CAF perspective | Platform | Security = protection; Governance = compliance |
| Q382 | A, C | CAF people perspective capabilities | CAF people | Organizational alignment + Organization design | Portfolio management = Governance; Risk management = Governance |
| Q383 | A | bridge between technology and business | CAF perspective description | People | Governance = risk; Operations = delivery |
| Q384 | C | patch management for managed services | AWS responsibility | Patch underlying infrastructure for managed services | App data security, IAM = customer |
| Q385 | C | IAM resources shared with another account | External sharing detection | IAM Access Analyzer | Credential report = internal; Cognito = mobile users |
| Q386 | C | structured allocation of computing resources | Well-Architected pillar | Performance efficiency | Reliability = recovery; Operational excellence = processes |
| Q387 | A, D | CAF governance perspective capabilities | CAF governance | Program and project management + Risk management | Product management = Business; Event management = Operations |
| Q388 | A | AWS Managed Services (AMS) scope | AMS feature | Landing zone and network management | Customer app development = customer; log monitoring = customer |
| Q389 | B | migrate on-premises NoSQL to DynamoDB | NoSQL database migration | AWS DMS | Migration Hub = tracking; Migration Evaluator = cost baseline |
| Q390 | C | finding correct EC2 instance types, lowest cost | Resource optimization | Rightsizing | Auto Scaling = capacity; Storage tiering = S3 |
| Q391 | D | manage sign-in for workforce, centrally | Workforce identity management | AWS IAM Identity Center | Cognito = mobile/web users; Security Hub = aggregation |
| Q392 | B | MFA device status report for all users | MFA reporting | IAM Credential Reports | Cost and Usage = billing; Detailed Billing = billing |
| Q393 | C | ML to analyze log data, security investigations | Security investigation with ML | Amazon Detective | Inspector = vulnerabilities; QuickSight = BI |
| Q394 | B | social media sign-in for mobile app | Social identity federation | Amazon Cognito | Lambda = functions; Secrets Manager = credentials |
| Q395 | A | data-driven business cases for cloud planning | Migration business case | Migration Evaluator | Billing Conductor = billing; Forecast = time-series predictions |
| Q396 | A | AWS Cost Explorer cloud concept | Cloud concept | Rightsizing | Reliability = uptime; Resilience = recovery |
| Q397 | D | Java web app, managed service, auto provision | PaaS for web apps | AWS Elastic Beanstalk | ECS = containers; Lambda = functions; EKS = Kubernetes |
| Q398 | D | connect to AWS and deploy programmatically | Programmatic AWS access | AWS SDKs | QuickSight = BI; PrivateLink = private connectivity |
| Q399 | D | rightsize underutilized EC2 | Rightsizing recommendation | AWS Compute Optimizer | Config = compliance; Anomaly Detection = cost spikes |
| Q400 | C | central data protection policy, compute/storage/DB | Centralized backup | AWS Backup | Batch = batch jobs; Elastic DR = disaster recovery |
| Q401 | A | categorize and track costs by business categories | Cost categorization | Cost allocation tags | Organizations = multi-account; Security Hub = security |
| Q402 | A | migrate data between AWS storage services | Storage data migration | AWS DataSync | Direct Connect = network; Lake Formation = data lake |
| Q403 | A, E | cost-effectiveness of AWS Cloud | Cloud economics | Trade fixed for variable expenses + Economies of scale | Deploying globally = agility; patching = security |
| Q404 | C | support development innovations, continuously improve | Well-Architected pillar | Operational excellence | Reliability = recovery; Security = protection |
| Q405 | B | consolidate billing, one account pays for all | Multi-account billing | AWS Organizations | Trusted Advisor = recommendations; Budgets = alerts |
| Q406 | B | set spending limits, receive notifications | Budget management | AWS Budgets | Cost and Usage = raw data; Cost Explorer = analysis |
| Q407 | D, E | access to TAM | TAM access | Enterprise On-Ramp + Enterprise Support | Business = no designated TAM |
| Q408 | C | examples of AWS Cloud solution designs | Architecture examples | AWS Architecture Center | Marketplace = software; Service Catalog = governance |
| Q409 | B | responsibility using Amazon RDS | Customer RDS responsibility | Create IAM policies to control access | Infrastructure provisioning, OS patching = AWS |
| Q410 | A | advantage AWS provides users | Cloud advantage | Eliminate need to guess capacity | Hardware control, OS control = not cloud advantages |
| Q411 | C | RDS high availability feature | RDS HA | Multi-AZ deployment | Read replicas = performance; Blue/green = deployment strategy |
| Q412 | D | check IAM access keys not rotated recently | Key rotation check | AWS Trusted Advisor | WAF = web; Shield = DDoS; Cognito = identity |
| Q413 | D | control network traffic between EC2 instances, native | Instance-level network control | Security groups | Network ACLs = subnet; WAF = web layer |
| Q414 | D, E | components of VPC | VPC components | Internet Gateway + Subnet | API Gateway = not a VPC component; S3 = not in VPC |
| Q415 | D | application available if individual component fails | Fault tolerance design | Loose coupling | Automation = operational; Rightsizing = cost |
| Q416 | D | identify and protect sensitive data in S3 | S3 sensitive data | Amazon Macie | IAM Access Analyzer = external sharing; Inspector = EC2 vulnerabilities |
| Q417 | C | limit network access at subnet level | Subnet-level access control | Network ACL | Shield = DDoS; WAF = web layer; Security group = instance level |
| Q418 | C | manage encryption keys in cloud | Hardware key management | AWS CloudHSM | License Manager = licenses; ACM = SSL certs; Directory Service = AD |
| Q419 | B | launch third-party intrusion detection from AWS account | Third-party security software | AWS Marketplace | Security Hub = aggregation; Quick Starts = reference deployments |
| Q420 | C | range of technologies to experiment quickly | Cloud agility | Access range of technologies to experiment | Pay-as-you-go = cost; geographic expansion = global reach |
| Q421 | B | release application changes automatically | Automated deployment | AWS CodeDeploy | AppFlow = data integration; PrivateLink = private connectivity |
| Q422 | D | manage identities and permissions at scale | CAF perspective | Security | Operations = delivery; Platform = technology; Governance = risk |
| Q423 | C | store and retrieve encrypted credentials | Secret storage and retrieval | AWS Secrets Manager | Encryption SDK = encrypt data; Security Hub = aggregation |
| Q424 | C | frequent, small, reversible changes | Well-Architected pillar | Operational excellence | Security = protection; Cost optimization = spending |
| Q425 | B | deploy AWS WAF rules | WAF deployment target | Application Load Balancer | EC2 = compute; Trusted Advisor = recommendations; NLB = TCP |
| Q426 | B | global audience, minimum latency, EC2 website | CDN for EC2-hosted site | Amazon CloudFront | Route 53 = DNS; ELB = regional load balancing |
| Q427 | B | reduce interdependencies between components | Design principle | Loose coupling | Scalability = capacity; Automation = operational |
| Q428 | B, E | provide access to RDS, CLI and SDK only | Least privilege access | Programmatic access only + RDS-specific IAM policy | Administrator access = too broad |
| Q429 | D | reporting app, once a week, can be shut down | Infrequent, variable workload | On-Demand Instances | Capacity Reservations = pay even if unused |
| Q430 | A | discover, prepare, move, integrate data, serverless | Data integration serverless | AWS Glue | Data Exchange = third-party data; Athena = query; EMR = big data |
| Q431 | C | development/test, not fully utilized, occasional unavailability | Non-critical interruptible | Spot Instances | On-Demand = no interruption guarantee |
| Q432 | A | sudden demand increases, lowest cost response | Dynamic scaling | AWS Auto Scaling | Compute Optimizer = rightsizing; Cost Explorer = analysis |
| Q433 | B | organize users, grant group permissions | User organization | AWS IAM | Security groups = network; Resource groups = tag-based |
| Q434 | C, E | Lambda, customer responsibilities | Shared responsibility, Lambda | Write business logic code + Provide IAM access to Lambda | Infrastructure, OS, runtime = AWS |
| Q435 | B | identify who accessed service, what action | API access investigation | AWS CloudTrail | CloudWatch = metrics; Inspector = vulnerabilities |
| Q436 | B | enforce compliance, govern deploy/manage/decommission | Governance tool | AWS Service Catalog | CloudWatch = monitoring; GuardDuty = threats |
| Q437 | B | "security of the cloud" | Shared responsibility definition | Security of cloud infrastructure | Availability, IAM, customer environments = customer |
| Q438 | D | unstructured data, durable, easy to query | NoSQL for unstructured data | Amazon DynamoDB | RDS = structured/relational; Aurora = relational |
| Q439 | B, E | CAF perspectives | CAF perspectives | Security + Business | Cloud fluency = People capability; Architecture = not a perspective |
| Q440 | B | container infrastructure, serverless, no operations | Serverless containers | AWS Fargate | Lightsail = simple apps; EC2 = requires management |
| Q441 | B | different locations, same geographic area, multiple power grids | HA in same region | Multiple Availability Zones in same AWS Region | Edge locations = CDN; multiple Regions = different geographies |
| Q442 | B | distribute incoming HTTP traffic evenly | Load balancing HTTP | Application Load Balancer | EC2 Auto Scaling = scaling capacity; Gateway LB = security appliances |
| Q443 | B | connect VPCs and on-premises to central hub | Network hub | AWS Transit Gateway | Virtual private gateway = VPN endpoint; Internet gateway = internet |
| Q444 | B | CPU-intensive workload, multiple EC2 | CPU-optimized EC2 | Compute optimized instances | General purpose = balanced; Storage optimized = I/O |
| Q445 | B | cloud router, simplify peering | Network hub/router | AWS Transit Gateway | Direct Connect = dedicated line; Route 53 = DNS |
| Q446 | B | twice each year, lowest cost, S3 | Infrequent with fast retrieval | Amazon S3 Glacier Instant Retrieval | Standard = frequent; Intelligent-Tiering = unknown patterns |
| Q447 | A | improve security in AWS account | Security improvement | Require MFA for privileged users | Root user cannot be removed; access keys for root = dangerous |
| Q448 | D, E | ways to improve security | Security improvements | Enable MFA + AWS Trusted Advisor security checks | Broadest permissions = worst security |
| Q449 | C | manage encryption keys in cloud | Hardware key management | AWS CloudHSM | License Manager = licenses; Directory Service = AD |
| Q450 | D | store files, public URL download | Public file storage | Amazon S3 | Redshift = analytics; EBS = block storage; EFS = shared file system |
| Q451 | C | deploy without provisioning infrastructure | PaaS | AWS Elastic Beanstalk | CloudFormation = IaC; CodeBuild = build |
| Q452 | C | insights from data, interactive dashboards | BI dashboards | Amazon QuickSight | SageMaker = ML; Rekognition = images; Kinesis = streaming |
| Q453 | D | some data accessed yearly, some daily, cost-effective | Variable access patterns | S3 Intelligent-Tiering | Standard = frequent; Glacier = archival |
| Q454 | A, C | economic benefits of AWS Cloud | Cloud economics | Consumption-based pricing + Economies of scale | Perpetual licenses = opposite; BYOH = not cloud |
| Q455 | C | local data center to AWS + local, hybrid | Migration type | On-premises to hybrid | Cloud native means all cloud; hybrid means both |
| Q456 | D | infrequently used data, archives, long-term backups | Long-term archival | Amazon S3 Glacier Flexible Retrieval | FSx for Lustre = HPC; EBS = block storage |
| Q457 | A | AWS issued reports, certifications, attestations | Compliance documentation | AWS Artifact | Trusted Advisor = recommendations; Config = compliance tracking |
| Q458 | B | interactive BI dashboards, ML insights | BI with ML | Amazon QuickSight | Glue Studio = ETL; Athena = query |
| Q459 | D | low-latency on-premises, data residency requirements | Hybrid on-premises | AWS Outposts | Wavelength = 5G; Ground Station = satellite; Transit Gateway = connectivity |
| Q460 | D | contact center, AI features | Cloud contact center | Amazon Connect | Wavelength = 5G; Direct Connect = network |
| Q461 | C | acquire resources when needed, release when done | Cloud concept | Elasticity | Scalability = capacity; Reliability = uptime |
| Q462 | B | stable, 1 year, most cost-effective | Year-long stable workload | Reserved Instances | Spot = interruptible; On-Demand = no discount |
| Q463 | A | securely log in to Linux EC2 | Linux authentication | SSH keys | VPN = network; end-to-end encryption = protocol; Route 53 = DNS |
| Q464 | A | serverless compute for application | Serverless compute | AWS Lambda | CloudFormation = IaC; Beanstalk = PaaS; ELB = load balancing |
| Q465 | C | automatically adjust EC2 instances based on load | Auto Scaling | Auto Scaling groups | Dedicated Hosts = isolation; Reserved = pricing |
| Q466 | A | consistent network, minimal latency, real-time feeds | Dedicated network | AWS Direct Connect | VPN = encrypted but internet; Connect = contact center |
| Q467 | D | custom applications, different instance types and configs | Custom compute deployment | Amazon EC2 | Lambda = serverless; Cognito = identity |
| Q468 | C | monitor and block malicious HTTP/HTTPS to CloudFront | Web application firewall | AWS WAF | GuardDuty = threats; Inspector = vulnerabilities |
| Q469 | B, C | PostgreSQL-compatible hosting | PostgreSQL hosting | Amazon Aurora + Amazon EC2 | S3 = object storage; OpenSearch = search |
| Q470 | C | generate information for external auditors | Audit information | AWS Config | Cognito = identity; FSx = file system; Inspector = vulnerabilities |
| Q471 | C | ISP and colocation facility required | Implementation requirement | AWS Direct Connect | VPN = no colocation needed; Connect = contact center |
| Q472 | A | EC2 high availability, natural disaster | Multi-region resilience | Multiple AWS Regions | Edge locations = CDN; CloudFront = content delivery |
| Q473 | D | file sharing between multiple EC2 instances | Shared file system | Amazon EFS | Direct Connect = network; Backup = backups |
| Q474 | D | multiple logins across AWS accounts in organization | Cross-account SSO | AWS IAM Identity Center | VPC = networking; Cognito = mobile/web |
| Q475 | B | WorkSpaces, AWS responsibility | Shared responsibility, WorkSpaces | Environmental safety and security of AWS infrastructure | MFA, IAM, CloudTrail = customer |
| Q476 | B | host domain name for website on AWS | DNS hosting | Amazon Route 53 | Lambda = functions; CloudFront = CDN; Direct Connect = network |
| Q477 | C | third-party IdP, no extra login credentials | Federated identity | AWS IAM Identity Center | Directory Service = AD integration; Resource Access Manager = sharing |
| Q478 | A, C | move commercial relational DB to open-source | Database migration | AWS DMS + AWS Schema Conversion Tool | SDKs = development; Systems Manager = operations |
| Q479 | D | on-demand, self-service, compliance control reports | Compliance self-service | AWS Artifact | Config = compliance tracking; GuardDuty = threats |
| Q480 | C | migrate workload, no changes | Migration with no changes | Rehost (lift and shift) | Repurchase = different product; Refactor = redesign |
| Q481 | B, C | CMS incompatible with cloud, least effort | Easy migration strategies | Rehost + Repurchase | Refactor = most effort; Replatform = some changes |
| Q482 | C, E | IAM best practices | IAM recommendations | Rotate credentials + Configure MFA | Root user = bad; shared keys = bad |
| Q483 | D | AWS responsibility | Shared responsibility | Hardware and infrastructure | Network config, encryption, IAM = customer |
| Q484 | D | graph query, fraud detection, credit cards | Graph database | Amazon Neptune | DocumentDB = MongoDB; Timestream = time-series |
| Q485 | D | detect and analyze images and videos | Image/video ML analysis | Amazon Rekognition | Connect = contact center; Lightsail = simple apps |
| Q486 | B | track, measure, review, forecast carbon emissions | Sustainability tracking | AWS Customer Carbon Footprint Tool | Health Dashboard = service status; QuickSight = BI |
| Q487 | A | highly repeatable infrastructure configurations | Repeatable IaC | AWS CloudFormation | CodeDeploy = app deployment; CodeBuild = build |
| Q488 | B | voice calls and web chat for customer service | Cloud contact center | Amazon Connect | Aurora = database; WorkSpaces = virtual desktops |
| Q489 | C | data warehouse environment | Data warehouse | Amazon Redshift | RDS = relational; DynamoDB = NoSQL; Aurora = relational |
| Q490 | D | network layer DDoS attacks | DDoS protection | AWS Shield | WAF = application layer; Firewall Manager = rule management |
| Q491 | C, D | advantages of moving to AWS Cloud | Cloud advantages | Increased speed and agility + Massive economies of scale | AWS does NOT assume all security responsibility |
| Q492 | A | securely and reliably run containers at scale | Container orchestration | Amazon ECS | Aurora = database; Athena = queries |
| Q493 | B | VPC firewall at subnet level | Subnet firewall tool | Network ACL | Security group = instance level; Traffic Mirroring = monitoring |
| Q494 | C | batch, fault-tolerant, can handle interruptions, optimize cost | Interruptible batch | Amazon EC2 Spot Instances | Macie = data; Neptune = graph |
| Q495 | B | send alerts when CloudWatch alarm invoked | Alarm notifications | Amazon SNS | CloudTrail = API logs; SQS = queue; EventBridge = event routing |
| Q496 | A | highly available, scalable DNS | DNS service | Amazon Route 53 | Lightsail = simple apps; Amplify = web/mobile apps |
| Q497 | D | customer task, shared responsibility | Customer task | Update guest OS on EC2 | Lambda, DynamoDB, S3 infrastructure = AWS |
| Q498 | B, C | EC2 customer responsibilities | EC2 customer tasks | Patch guest OS + Encrypt data at rest | Hypervisor patching, hardware = AWS |
| Q499 | D | MySQL to AWS managed service | Migration strategy | Replatform | Rehost = no changes; Refactor = redesign |
| Q500 | D | monolith to microservices | Migration strategy | Refactor | Rehost = lift and shift; Replatform = some optimization |
| Q501 | B | track cloud costs by department and project | Cost tracking | Cost allocation tags | Consolidated billing = single bill; Marketplace = software |
| Q502 | A | invoke Lambda when EC2 enters "stopping" state | Event-driven Lambda | Amazon EventBridge | Config = compliance; SNS = notifications; CloudFormation = IaC |
| Q503 | A | MariaDB on-premises, move to cloud, least overhead | Managed MariaDB | Amazon RDS | Neptune = graph; DynamoDB = NoSQL |
| Q504 | D | governance, compliance, risk auditing | Governance audit trail | AWS CloudTrail | MFA = security; Lambda = functions; SNS = notifications |
| Q505 | A | implement CloudTrail, AWS Cloud design principle | Design principle | Activate traceability | Serverless = Lambda; operations as code = CloudFormation |
| Q506 | C | threat detection, continuously monitor accounts, S3 | Threat detection | Amazon GuardDuty | Shield = DDoS; Firewall Manager = rule management; Inspector = vulnerabilities |
| Q507 | A | become more responsive to customers, organizational transformation | CAF organization transformation | Realign teams to focus on products and value streams | New products = Business transformation; data platform = Technology |
| Q508 | B | rightsize EC2, least operational overhead | Rightsizing approach | Change size and type based on utilization | Adding AZs = availability; different payment = cost model |
| Q509 | A | user sign-up, authentication, mobile/web | Mobile/web identity | Amazon Cognito | Config = compliance; GuardDuty = threats |
| Q510 | C | lower usage costs, aggregate usage all AWS users | Cloud benefit | Economies of scale | Capacity guessing = planning; global reach = geography |
| Q511 | D | IAM, principle of least privilege | Customer responsibility | Use IAM per least privilege | CloudFront, CloudWatch, DynamoDB = AWS manages |
| Q512 | D | manage cloud resources by IaC templates, compliance | IaC governance | AWS Service Catalog | Artifact = compliance docs; Resource Explorer = search; License Manager = licenses |
| Q513 | D | monitor CPU utilization | Performance monitoring | Amazon CloudWatch | Config = compliance; Trusted Advisor = recommendations; CloudTrail = API |
| Q514 | A | estimate costs for as-is infrastructure | Pre-migration cost estimate | AWS Pricing Calculator | Well-Architected = architecture; CAF = strategy |
| Q515 | A | deliver and share custom AMIs | AMI sharing/distribution | AWS Marketplace | Data Exchange = third-party data; Organizations = accounts |
| Q516 | D | enable inbound internet access, VPC | VPC internet access | Internet Gateway | NAT = outbound; VPN = encrypted; VPC endpoint = AWS services |
| Q517 | D | infrastructure as code support | IaC service | AWS CloudFormation | CodeDeploy = deployment; Beanstalk = PaaS |
| Q518 | A | millions of queries per second, scale | High-throughput database | Amazon DynamoDB | Cloud9 = IDE; ElastiCache for Memcached = caching |
| Q519 | A | proactively detect compromised instances, threats | Threat detection | Amazon GuardDuty | WAF = web attacks; Shield = DDoS; Inspector = vulnerabilities |
| Q520 | B | full set of Trusted Advisor checks, lowest cost | Trusted Advisor access | AWS Business Support | Developer = 7 basic checks; Enterprise = also full but more expensive |
| Q521 | D | partially migrate to serverless, pay upfront | Flexible savings plan for migration | Compute Savings Plan | Convertible Reserved = still EC2 only; EC2 Savings Plan = EC2 family only |
| Q522 | B, D | benefits of AWS Cloud for mobile app | Cloud benefits | Increased speed for new projects + Flexibility to scale | Capital expense = wrong; physical security control = on-premises |
| Q523 | C | WORM model compliance | S3 compliance feature | S3 Glacier Vault Lock | Versioning = multiple versions; MFA delete = deletion protection |
| Q524 | B | batch, can handle interruptions | Interruptible batch workloads | Spot Instances | Reserved = commitment; Dedicated = physical isolation |
| Q525 | C | PostgreSQL, highly available, fault tolerant | RDS HA | RDS with multiple Availability Zones | Single AZ = not HA; snapshots = backup not HA |
| Q526 | D | most secure password storage | Secure password storage | AWS Secrets Manager | S3 = object storage; CloudFormation parameters = plaintext risk |
| Q527 | B, E | global infrastructure component relationships | Infrastructure relationships | More edge locations than Regions + More AZs than Regions | Edge locations are NOT AZs |
| Q528 | C | DNS resolution | DNS service | Amazon Route 53 | CloudFront = CDN; VPC = networking; Direct Connect = network |
| Q529 | B | specific geographic area compliance | Infrastructure feature | Global footprint | Scalability = capacity; Availability = uptime |
| Q530 | C, D | cost-effective for dynamic usage | Cloud cost effectiveness | Elasticity + Pay-as-you-go | Reliability = uptime; Security = protection |
| Q531 | C | operational even with component failures | Reliability design | Design for automatic failover | Quarterly testing = good but not primary design; single EC2 = bad |
| Q532 | A | what Pricing Calculator does | Pricing Calculator function | Project monthly AWS costs | Historical costs = Cost Explorer; service info = documentation |
| Q533 | C | NFS protocols, store/retrieve objects in S3 | NFS-to-S3 bridge | AWS Storage Gateway file gateway | FSx for Lustre = HPC; Volume Gateway = iSCSI |
| Q534 | A, C | change IAM password services | IAM password management | AWS CLI + AWS Management Console | KMS = encryption keys; RAM = sharing; Secrets Manager = secrets |
| Q535 | A | customer task, shared responsibility | Customer responsibility | Patch guest OS on EC2 | Physical access = AWS; host OS = AWS |
| Q536 | B | firewall at subnet level | Subnet-level firewall | Network ACL | Security group = instance level; WAF = web layer |
| Q537 | A | automated video analysis, identify employees | Video analysis ML | Amazon Rekognition | Polly = text-to-speech; Cognito = identity |
| Q538 | B | web server on EC2, at least 1 year, no interruption | Year-long, no interruption | Partial Upfront Reserved Instances | All Upfront = most savings; No Upfront = less savings |
| Q539 | B, E | IAM best practices | IAM guidelines | Create individual IAM users + Use groups for permissions | Sharing keys = bad; inline policies = harder to manage |
| Q540 | B | scale resources up and down based on load | Cloud advantage | Stop guessing capacity | Going global = geography; economies of scale = cost |
| Q541 | B | PCI reports, validate security controls | PCI compliance | AWS Artifact | Support = technical help; TAM = Enterprise Support |
| Q542 | A | distribute traffic between EC2 instances | Traffic distribution | Application Load Balancer | WAF = web security; CloudHSM = encryption; Direct Connect = network |
| Q543 | A, C | AWS Cloud global infrastructure components | Infrastructure components | Availability Zones + AWS Regions | ElastiCache = service; S3 = service; VPC = logical network |
| Q544 | A, D | AWS responsibilities | Shared responsibility | Network infrastructure and virtualization + Physical security | Data security, guest OS, credentials = customer |
| Q545 | B | encrypt databases and backups, who manages | Encryption management | The company (customer) | AWS manages infrastructure; customer manages encryption settings |
| Q546 | B | custom conditions to filter inbound web traffic | Web traffic filtering | AWS WAF | GuardDuty = threats; Macie = data; Shield = DDoS |
| Q547 | B | consistent bandwidth, better than public internet | Consistent private connection | AWS Direct Connect | VPN = encrypted but variable; CloudFront = CDN |
| Q548 | B | temporary, variable, cannot stop before finishing | Short-burst, non-interruptible | On-Demand Instances | Spot = can be interrupted; Savings Plan = long-term |
| Q549 | A | employees working from home, Windows/Linux desktops | Virtual desktop | Amazon WorkSpaces | Cloud9 = IDE; Outposts = on-premises; Lightsail = simple apps |
| Q550 | B | SQL syntax, direct query of S3 objects | SQL queries on S3 | Amazon Athena | Glue = ETL; Lambda = functions; Kinesis = streaming |
| Q551 | C | Amazon RDS highly available | RDS high availability | Multi-AZ deployment | Read replicas = read scaling; Reserved = pricing |
| Q552 | B | serverless compute for containers | Serverless containers | AWS Fargate | SQS = messaging; Beanstalk = PaaS; SageMaker = ML |
| Q553 | A | one bill for multiple accounts | Consolidated billing | AWS Organizations | Trusted Advisor = recommendations; Budgets = alerts |
| Q554 | D | firewall, one EC2 instance only, not others in same subnet | Instance-specific firewall | Security group | Network ACL = subnet level; WAF = web layer |
| Q555 | B | web servers, most customers use during certain hours | Cost-effective for variable traffic | Auto Scaling group | Multiple AZs = HA; placement group = performance |
| Q556 | B | always free regardless of support plan | Always-free benefit | AWS Developer Forums | Developer Support = paid; TAM = Enterprise; programmatic case = Business+ |
| Q557 | A | 3+ years, continuous, discount | Long-term EC2 | Reserved Instances | Spot = interruptible; On-Demand = most expensive |
| Q558 | C | audit recent account activity, who initiated events | Account activity audit | AWS CloudTrail | Config = configuration; Rekognition = images |
| Q559 | A, C | reliability pillar design principles | Reliability design | Automatically recover from failure + Stop guessing capacity | Grant everyone quota access = wrong; single AZ = bad |
| Q560 | D | static website, least operational overhead | Static website hosting | Amazon S3 | EC2 = requires management; Beanstalk = PaaS; Lightsail = simple apps |
| Q561 | D | Cost Explorer recommendation | Cost Explorer function | Terminate idle instance | Database engine change = not Cost Explorer; OS deployment = not Cost Explorer |
| Q562 | B | multiple AZs in single region | AZ deployment benefit | Resilient architecture, highly available | Improved global performance = multiple regions; shutting AZ = not possible |
| Q563 | B | RSS feeds for AWS service updates | Service status | AWS Health Dashboard | SNS = notifications; Config = compliance; CodeCommit = code |
| Q564 | C | Reserved Instances, most cost savings | RI term commitment | 3 years | 1 year = less discount; 5 years = not available |
| Q565 | B | big data analytics, parallel, can tolerate downtime | Interruptible analytics | Spot Instances | On-Demand = more expensive; Reserved = commitment |
| Q566 | B | EC2 instances, 3 hours/week, cannot be interrupted | Short, non-interruptible | On-Demand Instances | Spot = interruptible; Convertible Reserved = long commitment |
| Q567 | C | API calls to AWS Support, most cost-effective | Support with API access | AWS Business Support | Basic = no API; Developer = no API |
| Q568 | D | pay for services on as-needed basis | Cloud computing advantage | Trade fixed expense for variable expense | Stop spending on data centers = also true but less specific to payment model |
| Q569 | C | predictable compute workload, 3 years, critical | Long-term, critical | Savings Plans | Spot = interruptible; On-Demand = most expensive |
| Q570 | D | estimate cost for AWS architecture before migration | Pre-deployment cost estimate | AWS Pricing Calculator | Detective = security; Budgets = alerts; Resource Explorer = search |
| Q571 | C | centrally manage employee access to multiple accounts | Centralized multi-account access | AWS IAM Identity Center | Access Analyzer = external sharing; Secrets Manager = credentials |
| Q572 | A | monthly allocation alert, research grant | Budget alert | AWS Budgets | Cost Explorer = visualization; Cost allocation tags = tagging |
| Q573 | B, D | optimize existing EC2 resources | EC2 optimization | AWS Cost Explorer + AWS Compute Optimizer | Elastic Beanstalk = PaaS; Detective = security; Billing Conductor = billing |
| Q574 | B | multi-account AWS environment setup | Multi-account governance | AWS Control Tower | CloudFormation = IaC; Config = compliance; VPC = networking |
| Q575 | C | full set of Trusted Advisor checks | Trusted Advisor requirement | AWS Trusted Advisor with AWS Business Support | Developer Support = 7 checks only |
| Q576 | C | track migration progress | Migration tracking | AWS Migration Hub | CloudWatch = monitoring; DataSync = migration; Application Migration = migration |
| Q577 | C | accelerate cloud adoption, paid engagements | Cloud adoption services | AWS Professional Services | Enterprise Support = technical support; Solutions Architects = design |
| Q578 | C | 1+ year, application must run continuously | Long-term continuous | Reserved Instances | Dedicated = expensive; Spot = interruptible |
| Q579 | A, C | AWS CDK programming languages | CDK languages | Python + TypeScript | Swift = Apple; Ruby = not CDK; PHP = not CDK |
| Q580 | A | provision AWS infrastructure programmatically | Programmatic IaC | AWS CDK | CodeGuru = code review; Config = compliance; CodeCommit = code storage |
| Q581 | C | own logically isolated section of AWS Cloud | Network isolation | Amazon VPC | VPN = encrypted connection; AZs = physical locations |
| Q582 | A, C | IAM controls | IAM capabilities | Control access to APIs + Protect with MFA | Threat detection = GuardDuty; data center access = not IAM |
| Q583 | A | why CloudFormation templates used | CloudFormation purpose | Reduce provisioning time with automation | Transfer infrastructure = not possible; on-premises reuse = not applicable |
| Q584 | D | who manages root user access keys | Root key management | The AWS account owner | IAM users and roles cannot manage root keys |
| Q585 | B | shares responsibility with AWS | Shared responsibility | Customers | Third-party vendors = not in model; internet providers = infrastructure |
| Q586 | B | event history of AWS resources created | Resource creation history | AWS CloudTrail | CloudWatch = metrics; Aurora = database; EventBridge = event routing |
| Q587 | B | run relational databases, install, regular updates | Managed relational DB | Amazon RDS | S3 = object storage; EBS = block storage; DynamoDB = NoSQL |
| Q588 | C | fully managed graph database, highly connected | Graph database | Amazon Neptune | DynamoDB = NoSQL; RDS = relational; Aurora = relational |
| Q589 | C | DDoS protection, real-time visibility | Advanced DDoS protection | AWS Shield Advanced | Shield Standard = free; Firewall Manager = rule management |
| Q590 | B | container services, 4-hour jobs, no server provisioning | Serverless containers | AWS Fargate | Lambda = 15 min limit; EC2 = requires management |
| Q591 | B | create copies of resources across regions | Cross-region resource copying | AWS CloudFormation | ElastiCache = caching; CloudTrail = logging |
| Q592 | C | AWS responsibility | Shared responsibility | Perform automated backups of RDS | Guest OS patches, cost optimization = customer |
| Q593 | C | one-time backup of EBS volume | EBS backup | Create an EBS snapshot | Copying contents = complex; Direct Connect = network |
| Q594 | C | no AWS experience, build web application | Beginner web development | Amazon Lightsail | SageMaker = ML; Lambda = functions; ECS = containers |
| Q595 | B | third-party SaaS access, portal for end users | SSO portal for SaaS | AWS IAM Identity Center | Cognito = mobile/web users; IAM = AWS users; Directory Service = AD |
| Q596 | D | NoSQL database workloads | NoSQL service | Amazon DynamoDB | RDS = relational; S3 = object storage; Redshift = analytics |
| Q597 | B | website, worldwide, low-latency for global users | CDN for websites | Amazon CloudFront | CloudFormation = IaC; ElastiCache = caching; DynamoDB = database |
| Q598 | B | conversational chatbot for website | Chatbot service | Amazon Lex | Textract = document extraction; Glue = ETL |
| Q599 | D | monitor disk write spikes on EC2 | Performance monitoring | Amazon CloudWatch | CloudTrail = API logs; Health Dashboard = service status |
| Q600 | A | control on-premises factory equipment, least latency | On-premises low-latency compute | AWS Outposts | EC2 = cloud; Lambda = serverless cloud |
| Q601 | B | inventory data products, data catalog | CAF perspective | Governance | Operations = delivery; Platform = technology |
| Q602 | D | production workload, lowest cost support | Production support, lowest cost | AWS Business Support | Developer = not for production; Enterprise = more expensive |
| Q603 | C | primary use case for GuardDuty | GuardDuty purpose | Automatic monitoring for threats | DDoS = Shield; SQL injection = WAF; auto-provisioning = not security |
| Q604 | B | virtual firewall at EC2 instance level | Instance-level firewall | Security group | Network ACL = subnet; Route table = routing; NAT = translation |
| Q605 | D | interact with AWS CLI | CLI authentication | AWS access key | Username/password = Console; root password = dangerous |
| Q606 | A | block users in certain countries | Geographic blocking | AWS WAF | Control Tower = governance; Fraud Detector = fraud; Pinpoint = marketing |
| Q607 | B | 5MB audio files, rarely accessed, retrieve immediately | Infrequent but fast retrieval | S3 Standard-Infrequent Access | Glacier = slow retrieval; Standard = frequent access |
| Q608 | C | secure network connection, within 1 week | Quick VPN setup | AWS Site-to-Site VPN | Direct Connect = weeks/months; VPC = logical network; Edge = CDN |
| Q609 | C | Lambda, customer responsibility | Shared responsibility, Lambda | Code and libraries in Lambda functions | Hardware, networking, server software = AWS |
| Q610 | C, E | AWS responsibilities | AWS tasks | Secure physical AWS facilities + Infrastructure patching | IAM, security groups, app patches = customer |
| Q611 | A | review AWS SOC reports | Compliance documentation | AWS Artifact | Concierge = billing; Support = technical; Trusted Advisor = recommendations |
| Q612 | A | record and evaluate configuration changes, remediation | Configuration compliance | AWS Config | Secrets Manager = credentials; CloudTrail = API logs |
| Q613 | B | one-time migration, large dataset, millions of files | File data migration | AWS DataSync | DMS = database; Migration Hub = tracking; Application Migration = server |
| Q614 | A, C | CIDR block notation in AWS | CIDR notation services | Security groups + Network ACLs | AMI = EC2 image; Budgets = cost; EBS = storage |
| Q615 | B | accessibility app, text to speech | Text-to-speech | Amazon Polly | MQ = messaging; Neptune = graph; Timestream = time-series |
| Q616 | D | dedicated network, no public internet | Dedicated private connection | AWS Direct Connect | Transit Gateway = connectivity; VPN = internet-based |
| Q617 | C | dashboards and charts from business data | BI visualization | Amazon QuickSight | Macie = data; Aurora = database; CloudTrail = API logs |
| Q618 | D | reduce upfront costs, migration | Cloud advantage | Trade fixed expense for variable expense | Global in minutes = agility; economies of scale = cost reduction |
| Q619 | C | perform intended function, throughout lifecycle | Well-Architected pillar | Reliability | Operational excellence = processes; Performance = resource efficiency |
| Q620 | B | federated security credentials, temporary | Temporary federated credentials | AWS STS | GuardDuty = threats; Secrets Manager = credentials; ACM = SSL |
| Q621 | B | ELB benefit | ELB function | Balance traffic across multiple compute resources | ELB does NOT auto-scale (ASG does); ELB is regional |
| Q622 | C | convert video/audio to mobile format | Media transcoding | Amazon Elastic Transcoder | Comprehend = NLP; Rekognition = images; Polly = text-to-speech |
| Q623 | C | store RDS credentials, auto-rotate passwords | Automatic credential rotation | AWS Secrets Manager | S3 = object storage; Parameter Store = config but not auto-rotate; CloudTrail = audit |
| Q624 | C | set up infrastructure in minutes | Cloud advantage | Increase speed and agility | Economies of scale = cost; capacity guessing = planning |
| Q625 | D | managed NFS file system for compute resources | Managed NFS | Amazon EFS | EBS = block storage; Tape Gateway = tape backup; S3 Glacier = archival |
| Q626 | A | gather information about on-premises data center | Migration discovery | AWS Application Discovery Service | DataSync = file migration; Storage Gateway = hybrid; DMS = database |
| Q627 | B, D | customer responsibilities | Customer tasks | Encrypt data + Maintain IAM controls | Virtualization layer = AWS; RDS OS = AWS; Availability Zones = AWS |
| Q628 | B, D | handle seasonal workload increase, cost-effective | Cloud scalability for seasonal | Pay-as-you-go + Auto Scaling policies | Cross-Region = not necessary; CloudTrail = audit; centralized logging = monitoring |
| Q629 | B | standardized template for multiple environments | Environment templating | AWS CloudFormation | Cloud Map = service discovery; CloudFront = CDN; CloudTrail = audit |
| Q630 | C | private network connection, on-premises | Private dedicated connection | AWS Direct Connect | Config = compliance; VPC = logical network; Route 53 = DNS |
| Q631 | C | customer responsibility | Customer task | Patch guest OS with latest security patches | Disk shredding = AWS; packet collection prevention = AWS |
| Q632 | D | speech-to-text conversion | Speech-to-text | Amazon Transcribe | Polly = text-to-speech; Textract = documents; Rekognition = images/video |
| Q633 | C | graphical interface for managing AWS services | GUI management | AWS Management Console | Copilot = containers; CLI = command line; SDK = programming |
| Q634 | A | workload 1 year, cannot tolerate interruptions, most cost-effective | Year-long, no interruption | All Upfront Reserved Instances | Partial Upfront = less savings; Dedicated = expensive |
| Q635 | A | ensure ongoing optimization and security | Ongoing optimization | AWS Trusted Advisor | Health Dashboard = service status; Connect = contact center |
| Q636 | A | encrypt data at rest, integrates with other AWS services | Encryption integration | AWS KMS | ACM = SSL certs; IAM = access control; Security Hub = aggregation |
| Q637 | B | track monthly cost and usage of EC2 instances | Cost tracking | AWS Budgets | Cost Anomaly Detection = spikes; Compute Optimizer = rightsizing |
| Q638 | B | automatically acquire and release resources | Cloud concept | Elasticity | Availability = uptime; Durability = data; Reliability = recovery |
| Q639 | A | short time periods, can be interrupted, cost-effective | Interruptible short workloads | Spot Instances | On-Demand = no interruption; Reserved = long commitment |
| Q640 | D | DDoS Response Team (DRT) access | DRT access requirement | AWS Shield Advanced | Business Support = insufficient; WAF = web attacks |
| Q641 | C | historical spending patterns, future cost projections | Cost visualization | Cost Explorer | Cost and Usage = raw data; Budgets = alerts; CloudWatch = metrics |
| Q642 | B, C | advantages of migrating to AWS | Migration advantages | Increased global reach and agility + Ability to deploy globally | Security auditing still needed; IT staff still needed |
| Q643 | C | uses edge locations to cache content | CDN edge caching | Amazon CloudFront | Kinesis = streaming; SQS = queue; Route 53 = DNS |
| Q644 | C | securely access S3 from EC2 without internet | Private AWS service access | VPC endpoint | VPN = encrypted internet; NAT = internet through private subnet |
| Q645 | C | automate software deployment, EC2 and on-premises | Hybrid deployment automation | AWS CodeDeploy | CodeCommit = code storage; CodeBuild = build; CodePipeline = orchestration |
| Q646 | A, D | serverless AWS services | Serverless | AWS Fargate + Amazon S3 | EC2 = servers; EMR = managed cluster; Kafka = managed |
| Q647 | B | continuously improve processes to deliver value | Well-Architected pillar | Operational excellence | Performance efficiency = resource use; Reliability = recovery |
| Q648 | D | customer responsibility, shared responsibility | Customer task | Implement MFA for IAM user accounts | S3 patches, data centers, Lambda@Edge OS = AWS |
| Q649 | B | organize and search large numbers of images | Image analysis | Amazon Rekognition | Transcribe = audio; Aurora = database; QuickSight = BI |
| Q650 | B | always free of charge | Free service | AWS IAM | Athena, Secrets Manager, ElastiCache = have costs |
| Q651 | B | on-premises + cloud, same API calls | Hybrid with same APIs | AWS Outposts | Dedicated Hosts = physical servers in cloud; Wavelength = 5G |
| Q652 | C | On-Demand recommended use case | On-Demand use case | Unpredictable workload, no long-term commitment | Steady-state = Reserved; interruptible = Spot |
| Q653 | C | centralized gateway, multiple VPCs and on-premises | Network hub | AWS Transit Gateway | Gateway VPC endpoint = AWS services; PrivateLink = private services |
| Q654 | A | multiple resources deleted, identify user | Resource deletion investigation | AWS CloudTrail | Inspector = vulnerabilities; GuardDuty = threats |
| Q655 | C | PCI DSS compliance assistance | PCI compliance | AWS Attestation of Compliance (AOC) via Artifact | Physical inspections = not offered; professional services = not AWS |
| Q656 | B | when to create IAM user | IAM user creation | Creating AWS credentials for individuals | Applications use roles; mobile = Cognito or roles |
| Q657 | B | distribute traffic, single point of contact | Load distribution | Application Load Balancer | VPC endpoints = AWS services; NAT = internet; Internet gateway = internet |
| Q658 | D | total volume of S3 data | S3 capacity | Virtually unlimited | There is no set maximum for S3 storage |
| Q659 | A | reliability pillar design principle | Reliability design | Test recovery procedures | Experiment more = Performance; global in minutes = Performance |
| Q660 | D | S3 data stored, AWS task | AWS S3 responsibility | Protect infrastructure supporting S3 | Lifecycle, Versioning, bucket policies = customer |
| Q661 | D | convert existing server to run on AWS | Server migration | AWS Application Migration Service | DataSync = data; DMS = database; Discovery = pre-migration |
| Q662 | C | fully managed NoSQL | NoSQL service | Amazon DynamoDB | RDS = relational; Redshift = analytics; Aurora = relational |
| Q663 | A | improve application performance and availability, multiple regions | Global application performance | AWS Global Accelerator | DataZone = data governance; Cloud Map = service discovery |
| Q664 | C | SQL Server, day-to-day administration by AWS | Managed SQL Server | Amazon RDS | EC2 = self-managed; DynamoDB = NoSQL; Aurora = MySQL/PostgreSQL |
| Q665 | C | stateless network filtering for VPC | Stateless filtering | Network access control list (ACL) | PrivateLink = private services; Security group = stateful |
| Q666 | B | minimize variable costs | Cloud economic advantage | Economies of scale | High availability = architecture; Global reach = geography |
| Q667 | A, B | total cost of ownership for compute | Migration cost tools | AWS Pricing Calculator + Migration Evaluator | Support Center = technical; Application Discovery = discovery |
| Q668 | B | HPC workloads, data lakes | EC2 for HPC | Compute optimized instances | General purpose = balanced; Memory = RAM; Storage = I/O |
| Q669 | A, E | benefits of moving on-premises to AWS | Migration benefits | Reduce hardware tasks + Faster feature deployment | Staff elimination = false; auto security = false |
| Q670 | A, C | CAF, organizational transformation | CAF organization | Realign teams + Use agile methods | New products = Business; data platform = Technology; infrastructure = Technology |
| Q671 | B | isolated area, limited internet, local data processing | Offline edge computing | AWS Snowball Edge | S3 = cloud; Storage Gateway = hybrid needs internet |
| Q672 | A | graph queries, fraud pattern detection | Graph database | Amazon Neptune | DynamoDB = NoSQL; Timestream = time-series; Forecast = predictions |
| Q673 | A | acquire resources when needed, release when done | Cloud architecture concept | Elasticity | Availability = uptime; Reliability = recovery; Durability = data |
| Q674 | C | containerized app, auto container images from source code | Automated container deployment | AWS App Runner | Beanstalk = traditional apps; ECS = requires configuration |
| Q675 | C | track cost/usage, generate reports automatically | Automated cost reports | AWS Budgets | Detective = security; Pricing Calculator = estimates; Savings Plans = pricing |
| Q676 | C | real-time insights, strategy questions | CAF perspective | Business | Operations = delivery; People = workforce; Platform = technology |
| Q677 | B | critical production systems, 3 years, minimize cost | 3-year commitment | Reserved Instances | Spot = interruptible; On-Demand = no discount |
| Q678 | C | system remains functional during operational problems | Well-Architected concept | Durability | Consistency = database; Elasticity = scaling; Latency = speed |
| Q679 | D | recover automatically from service interruptions | Well-Architected pillar | Reliability | Security = protection; Performance = efficiency; Operational Excellence = processes |
| Q680 | B | multiple SQL databases, migrate, least overhead | Managed SQL databases | Amazon RDS | EC2 = self-managed; DynamoDB = NoSQL; OpenSearch = search |
| Q681 | D | build, train, deploy ML models | ML platform | Amazon SageMaker | Personalize = recommendations; Comprehend = NLP; Forecast = predictions |
| Q682 | B | rightsized EC2, historical workload usage | Rightsizing recommendations | AWS Compute Optimizer | Pricing Calculator = estimates; App Runner = containers |
| Q683 | B | explore and analyze data in S3 with programming language | SQL query on S3 | Amazon Athena | Kendra = document search; Comprehend = NLP; SageMaker = ML |
| Q684 | A | EC2, no interruption, most cost-effective | Non-interruptible EC2 | Standard Reserved Instances | Convertible = flexible but less discount; Spot = interruptible |
| Q685 | B | centralize and automate data protection | Centralized backup | AWS Backup | Artifact = compliance; Batch = batch jobs; Shield = DDoS |
| Q686 | C | gather usage and configuration data for migration | Pre-migration discovery | AWS Application Discovery Service | DMS = database migration; Transfer Family = SFTP |
| Q687 | A | performance efficiency, design principle | Performance efficiency principle | Using serverless architectures | Horizontal scaling = reliability; managed services = multiple pillars |
| Q688 | A | low latency globally | Cloud feature for global users | Global infrastructure | Pay-as-you-go = cost; managed services = operations |
| Q689 | B | Spot Instance workload type | Spot Instance use case | Workload that can be interrupted and control costs | Steady-state = Reserved; unpredictable = On-Demand |
| Q690 | B | multiple accounts, consolidated bill, security/compliance | Multi-account management | AWS Organizations | Cost and Usage = raw billing; Config = compliance; Security Hub = security |
| Q691 | B | On-Demand, most cost-effective use case | On-Demand optimal use | 1-month continuous quality assurance tests | Transcoding = Spot; web server 1 year = Reserved; database 3 years = Reserved |
| Q692 | D | cannot predict usage demand | Cloud benefit sought | Scalable and high performance | Easy to use = simplicity; cost-effective = pricing |
| Q693 | A | discover security vulnerabilities on EC2 | EC2 vulnerability scanning | Amazon Inspector | Macie = data; Shield Standard = DDoS; security groups = network |
| Q694 | C | Windows virtual desktops, remote employees | Virtual desktop service | Amazon WorkSpaces | Dedicated Hosts = physical; Global Accelerator = performance; CloudFront = CDN |
| Q695 | A | visualize and manage costs for specific period | Cost visualization | Cost Explorer | Consolidated billing = multi-account; Organizations = accounts; Budgets = alerts |
| Q696 | B | MySQL database engine support | MySQL managed service | Amazon RDS | DynamoDB = NoSQL; DocumentDB = MongoDB; ElastiCache = caching |
| Q697 | B | Standard RIs no longer needed, move to different family | Sell unused RIs | Amazon EC2 Reserved Instance Marketplace | AWS Support = not a marketplace; Savings Plans = not RI conversion |
| Q698 | C | strategic planning, IEM, real-time support | Strategic + event support | AWS Enterprise Support | Trusted Advisor = recommendations; APN = partners; Professional Services = consulting |
| Q699 | B | search for questions, retrieve specific answers | Intelligent search | Amazon Kendra | Connect = contact center; Lex = chatbot; Comprehend = NLP |
| Q700 | A | S3 single-digit milliseconds | Fastest S3 class | S3 Express One Zone | S3 Standard = milliseconds but not single-digit; Glacier = minutes/hours |
| Q701 | A, E | optimize costs, uninterruptible 24/7, 12 months | Year-long maximum savings | Standard Reserved Instance + All Upfront payment | Convertible = less discount; Spot = interruptible |
| Q702 | B | run code without provisioning servers | Serverless execution | AWS Lambda | Glue = ETL; CodeDeploy = deployment; CodeGuru = code review |
| Q703 | A | understand on-premises usage, not replicate yet | Pre-migration discovery | AWS Application Discovery Service | Application Migration = actual migration; Transfer Family = SFTP |
| Q704 | A | work remotely, Windows or Linux desktops | Virtual desktop | Amazon WorkSpaces | AppStream = stream specific apps; Cloud9 = IDE; Keyspaces = database |
| Q705 | B | test new application | Cloud principle | Scale up/down without long-term commitments | Long-term commitments = Reserved; total control = on-premises |
| Q706 | A | monitor ongoing costs of ecommerce website | Cost monitoring | AWS Cost Explorer | SDKs = development; Image Builder = AMI; CloudFormation = IaC |
| Q707 | A | improve performance of public applications, ALBs | Global application performance | AWS Global Accelerator | Connect = contact center; ElastiCache = caching; CloudWatch = monitoring |
| Q708 | B | on-premises app, < 5 minutes, few times/day | Short infrequent functions | AWS Lambda | ECS = containers; EKS = Kubernetes; EC2 = always running |
| Q709 | A | strategy management capability, CAF | CAF capability | Business perspective | People = workforce; Governance = risk; Operations = delivery |
| Q710 | D | consolidate call centers, voice and chat | Cloud contact center | Amazon Connect | SNS = notifications; Support Center = AWS support; Cognito = identity |
| Q711 | C | uninterruptible, pay by second | Flexible, uninterruptible compute | On-Demand Instances | Reserved = commitment; Spot = interruptible; Dedicated = physical |
| Q712 | A | migrate EC2 from one region to another | EC2 region migration | AWS Application Migration Service | DMS = database; DataSync = file; Migration Hub = tracking |
| Q713 | A | block SQL injection attacks | Web attack prevention | AWS WAF | NACLs = IP/port; Security groups = instance; Trusted Advisor = recommendations |
| Q714 | D | EC2 on AWS, keep on-premises for compliance | Hybrid on-premises compliance | AWS Outposts | Dedicated Instances = isolated but in cloud; CloudFront = CDN |
| Q715 | B | connect AWS services and VPCs, no public internet | Private AWS connectivity | AWS PrivateLink | Inspector = vulnerabilities; Connect = contact center; Internet Gateway = internet |
| Q716 | C | manage permissions using policies | IAM service | AWS IAM | Inspector = vulnerabilities; Detective = investigation; GuardDuty = threats |
| Q717 | B | workload in AWS, some on-premises for compliance | Hybrid deployment | AWS Outposts | Config = compliance; Lightsail = simple apps; Connect = contact center |
| Q718 | B | relational database, automated backups, snapshots | Managed relational DB with backups | Amazon RDS | DocumentDB = MongoDB; EBS = block storage; S3 = object storage |
| Q719 | B | additional servers needed for new business line, quickly | Fast infrastructure provisioning | Increase speed and agility | Economies of scale = cost; going global = geography |
| Q720 (truncated, same as Q719 continued) | B | — | — | Increase speed and agility | — |

---

# PART 2: Service-Based Summary

## AWS IAM (Identity and Access Management)
- **One-line definition:** Manage who can access what AWS resources.
- **Keywords:** users, groups, roles, policies, MFA, access keys, least privilege, credential report, Access Analyzer
- **Exam Rules:**
  - IAM is free, global service.
  - Root user = first sign-in identity; should NOT be used for daily tasks.
  - IAM User = long-term credentials for a person.
  - IAM Role = temporary credentials for services or cross-account access.
  - IAM Policy = JSON document defining permissions.
  - IAM Group = collection of users; cannot contain other groups.
  - Least privilege principle = grant only what is needed.
  - IAM Credential Report = lists all users + status of password, access keys, MFA.
  - IAM Access Analyzer = identifies resources shared externally.
- **Traps:**
  - Security groups ≠ IAM; Security groups are network firewalls.
  - Roles for EC2 = best practice; never hardcode access keys in code.
  - MFA can be applied to all IAM users, not just root.
  - IAM Access Analyzer is about external sharing, NOT credential status.
- **Questions covered:** Q4, Q5, Q29, Q32, Q39, Q54, Q94, Q98, Q106, Q108, Q149, Q160, Q177, Q216, Q297, Q343, Q428, Q433, Q434, Q482, Q539, Q571, Q582, Q584, Q650, Q656

---

## Amazon EC2 (Elastic Compute Cloud)
- **One-line definition:** Virtual servers in the AWS Cloud.
- **Keywords:** instance types, AMI, security group, EBS, user data, purchasing options, auto scaling
- **Exam Rules:**
  - EC2 = IaaS; customer manages OS, patches, applications.
  - Instance types: General Purpose, Compute Optimized, Memory Optimized, Storage Optimized, Accelerated Computing (GPU).
  - On-Demand = pay by second, no commitment, most flexible.
  - Reserved Instances (1 or 3 year) = up to 72% discount; Standard or Convertible.
  - Spot Instances = up to 90% discount; CAN BE INTERRUPTED.
  - Savings Plans = flexible commitment by dollar/hour.
  - Dedicated Hosts = physical server, for BYOL licensing or compliance.
  - Dedicated Instances = hardware dedicated to one account, no license control.
  - Capacity Reservations = reserve capacity, no billing discount.
- **Traps:**
  - Spot Instances = cheapest but interruptible; never use for critical/uninterruptible workloads.
  - Reserved Instances can be sold on the RI Marketplace.
  - Customer patches EC2 guest OS; AWS patches the physical infrastructure.
  - GPU = Accelerated Computing instances (not Compute Optimized).
- **Questions covered:** Q8, Q16, Q20, Q33, Q57, Q67, Q88, Q118, Q121, Q129, Q138, Q144, Q147, Q162, Q209, Q213, Q222, Q230, Q233, Q235, Q245, Q250, Q254, Q266, Q272, Q281, Q290, Q362, Q429, Q431, Q462, Q463, Q524, Q538, Q548, Q557, Q564, Q565, Q566, Q578, Q634, Q639, Q684, Q691

---

## Amazon S3 (Simple Storage Service)
- **One-line definition:** Unlimited, durable object storage.
- **Keywords:** buckets, objects, keys, durability 99.999999999%, storage classes, versioning, lifecycle, replication
- **Exam Rules:**
  - S3 = object storage; NOT file system (EFS) or block storage (EBS).
  - Buckets = region-scoped; names globally unique.
  - Max object size = 5TB; use multi-part upload for >5GB.
  - S3 Standard = frequent access, 99.99% availability.
  - S3 Standard-IA = infrequent, fast retrieval.
  - S3 One Zone-IA = cheaper but single AZ, risk of loss.
  - S3 Intelligent-Tiering = unknown patterns, auto moves objects.
  - S3 Glacier Instant Retrieval = milliseconds, quarterly access.
  - S3 Glacier Flexible Retrieval = 1-5 min (expedited), 3-5 hrs, 5-12 hrs.
  - S3 Glacier Deep Archive = 12-48 hrs, cheapest long-term.
  - S3 Express One Zone = single-digit millisecond, highest performance.
  - S3 Transfer Acceleration = faster uploads using edge locations.
  - S3 Versioning = protects against accidental deletion/overwriting.
  - S3 Lifecycle = automate movement between storage classes.
  - S3 Replication = CRR (cross-region) or SRR (same-region).
  - S3 Bucket Policy = resource-based access control.
  - Access Analyzer for S3 = review ACLs and policies.
  - Static website hosting = enable and allow public access.
  - Inbound data transfer = FREE; outbound = has cost.
- **Traps:**
  - S3 Intelligent-Tiering ≠ cheapest; it has monitoring fee.
  - S3 One Zone-IA = data lost if AZ is destroyed.
  - S3 Glacier ≠ instant retrieval by default (Glacier Instant Retrieval is the instant option).
  - S3 is NOT a file system; cannot be mounted natively without Storage Gateway.
- **Questions covered:** Q1, Q17, Q18, Q49, Q58, Q83, Q87, Q143, Q153, Q168, Q179, Q183, Q201, Q219, Q251, Q274, Q294, Q313, Q338, Q349, Q368, Q450, Q453, Q456, Q523, Q529, Q533, Q560, Q607, Q644, Q646, Q658, Q660

---

## Amazon RDS (Relational Database Service)
- **One-line definition:** Managed relational database service.
- **Keywords:** SQL, MySQL, PostgreSQL, Aurora, MariaDB, Oracle, SQL Server, Multi-AZ, Read Replicas, automated backups
- **Exam Rules:**
  - RDS = managed service; AWS patches OS, hardware; customer manages data, access, schema.
  - Multi-AZ = high availability, automatic failover, NOT performance.
  - Read Replicas = improve read performance, NOT HA by itself.
  - RDS = cannot SSH into instances.
  - Supports: MySQL, PostgreSQL, MariaDB, Oracle, SQL Server, IBM DB2, Aurora.
  - Aurora = AWS proprietary; 5x MySQL performance, 3x PostgreSQL performance.
  - Aurora Serverless = auto-scaling, pay-per-second, for infrequent/unpredictable workloads.
- **Traps:**
  - Multi-AZ ≠ Read Replicas; Multi-AZ = HA; Read Replicas = performance.
  - RDS is NOT for NoSQL; use DynamoDB for NoSQL.
  - AWS patches RDS OS; customer configures access and encryption.
  - Aurora = relational but much higher performance than standard RDS.
- **Questions covered:** Q63, Q161, Q162, Q190, Q200, Q227, Q240, Q409, Q411, Q503, Q525, Q551, Q587, Q664, Q680, Q696, Q718

---

## Amazon DynamoDB
- **One-line definition:** Managed NoSQL (key-value) database.
- **Keywords:** NoSQL, key-value, serverless, millions of requests/second, low latency, DAX, global tables
- **Exam Rules:**
  - DynamoDB = NoSQL; fully managed, auto-scales.
  - Single-digit millisecond latency.
  - DynamoDB = serverless; no servers to manage.
  - DAX = DynamoDB Accelerator; microsecond latency; ONLY for DynamoDB.
  - Global Tables = multi-region, active-active replication.
  - Standard and Infrequent Access (IA) table classes.
  - AWS manages OS, infrastructure; customer manages data and access permissions.
- **Traps:**
  - DAX ≠ ElastiCache; DAX only works with DynamoDB.
  - DynamoDB ≠ relational; cannot use JOIN queries.
  - Customer manages access permissions; AWS manages everything else.
- **Questions covered:** Q5, Q44, Q55, Q56, Q66, Q182, Q241, Q438, Q518, Q596, Q662

---

## AWS Lambda
- **One-line definition:** Run code without managing servers (serverless, FaaS).
- **Keywords:** serverless, function, event-driven, 15-minute limit, pay per invocation, per duration
- **Exam Rules:**
  - Lambda = serverless; no EC2 to manage.
  - Max execution time = 15 minutes.
  - Customer manages: code, IAM permissions, environment variables.
  - AWS manages: hardware, OS, runtime, infrastructure.
  - Lambda billing = per request + per duration (GB-seconds).
  - Free tier = 1M requests/month + 400,000 GB-seconds.
- **Traps:**
  - Lambda ≠ for long-running jobs; use Batch or EC2 for >15 min.
  - Lambda has limited disk space; use EBS/EFS for large storage.
  - AWS manages runtime for Lambda (unlike EC2 where customer manages).
- **Questions covered:** Q42, Q118, Q434, Q464, Q608, Q702, Q708

---

## Amazon CloudFront
- **One-line definition:** CDN that delivers content globally with low latency using edge locations.
- **Keywords:** CDN, edge locations, cache, TTL, static content, DDoS protection, OAC, custom origin
- **Exam Rules:**
  - CloudFront = Content Delivery Network; caches content at edge locations.
  - Works with S3, ALB, EC2, custom HTTP origins.
  - Origin Access Control (OAC) = restricts S3 access to CloudFront only.
  - Integrates with AWS Shield and WAF for DDoS protection.
  - 400+ edge locations globally.
- **Traps:**
  - CloudFront ≠ S3 Transfer Acceleration; CloudFront caches content; Transfer Acceleration speeds up S3 uploads.
  - CloudFront ≠ Global Accelerator; CloudFront = content caching; Global Accelerator = TCP/UDP routing, no caching.
  - CloudFront is regional in the sense that origins are regional but edge locations are global.
- **Questions covered:** Q49, Q85, Q194, Q269, Q321, Q365, Q426, Q597, Q643

---

## Amazon Route 53
- **One-line definition:** Managed DNS service with routing policies.
- **Keywords:** DNS, domain, routing policies, A record, CNAME, alias, latency, failover, geolocation, weighted
- **Exam Rules:**
  - Route 53 = managed DNS, global service.
  - Routing policies: Simple, Weighted, Latency, Failover, Geolocation.
  - Alias records = point to AWS resources (ELB, CloudFront, S3).
  - Route 53 enables multi-region failover and disaster recovery.
- **Traps:**
  - Route 53 ≠ load balancer; it's DNS routing.
  - Route 53 supports domain registration AND DNS hosting.
- **Questions covered:** Q242, Q476, Q496, Q528

---

## Amazon VPC (Virtual Private Cloud)
- **One-line definition:** Private, isolated virtual network in AWS.
- **Keywords:** subnets, internet gateway, NAT gateway, route tables, VPC peering, VPC endpoints, security groups, NACLs
- **Exam Rules:**
  - VPC = regional resource; subnets = AZ-scoped.
  - Public subnet = has route to internet gateway.
  - Private subnet = no direct internet access; use NAT gateway.
  - Internet Gateway = enables VPC-to-internet communication.
  - NAT Gateway = allows private subnets to access internet; blocks inbound.
  - VPC Peering = connect two VPCs; non-transitive.
  - VPC Endpoints = connect to AWS services without internet.
  - VPC Flow Logs = capture IP traffic info for monitoring.
  - Security Groups = instance-level, stateful, allow-only rules.
  - NACLs = subnet-level, stateless, allow and deny rules, evaluated in order.
  - Transit Gateway = hub for connecting many VPCs and on-premises.
- **Traps:**
  - Security Groups = stateful (return traffic automatically allowed).
  - NACLs = stateless (return traffic needs explicit rule).
  - VPC Peering ≠ transitive; must establish connection per pair.
  - NAT Gateway = outbound only from private subnets, NOT inbound.
- **Questions covered:** Q24, Q59, Q95, Q119, Q172, Q199, Q291, Q310, Q327, Q340, Q352, Q414, Q443, Q516, Q581, Q614, Q644, Q665

---

## Amazon CloudWatch
- **One-line definition:** Monitoring and observability service for AWS resources.
- **Keywords:** metrics, alarms, logs, dashboards, CPU utilization, custom metrics, CloudWatch Events/EventBridge
- **Exam Rules:**
  - CloudWatch = monitors AWS services and applications in real time.
  - Default EC2 metrics = every 5 minutes; Detailed Monitoring = every 1 minute.
  - EC2 does NOT report RAM metrics by default; needs custom agent.
  - CloudWatch Alarms = trigger Auto Scaling, EC2 actions, SNS notifications.
  - CloudWatch Logs = collect logs from EC2, Lambda, ECS, etc.
  - CloudWatch Agent = needed on EC2 to push custom logs.
  - EventBridge (formerly CloudWatch Events) = react to events, schedule tasks.
- **Traps:**
  - CloudWatch ≠ CloudTrail; CloudWatch = metrics/logs; CloudTrail = API audit.
  - Billing metrics only available in us-east-1.
- **Questions covered:** Q27, Q60, Q314, Q373, Q378, Q495, Q513, Q599, Q637

---

## AWS CloudTrail
- **One-line definition:** Records all API calls made to AWS for audit and governance.
- **Keywords:** API calls, audit, who did what, governance, compliance, event history
- **Exam Rules:**
  - CloudTrail = enabled by default in all accounts.
  - Records: who made the call, when, from where, what was changed.
  - Logs sent to S3 or CloudWatch Logs.
  - CloudTrail Insights = detects unusual API activity.
  - Covers all regions by default (trail can be single or multi-region).
  - If a resource is deleted, first check CloudTrail.
- **Traps:**
  - CloudTrail ≠ CloudWatch; CloudTrail = API audit; CloudWatch = metrics.
  - CloudTrail does NOT monitor application performance.
- **Questions covered:** Q41, Q60, Q111, Q155, Q232, Q244, Q302, Q435, Q504, Q505, Q558, Q586, Q612, Q654

---

## AWS Organizations
- **One-line definition:** Manage multiple AWS accounts centrally.
- **Keywords:** consolidated billing, service control policies (SCP), master account, organizational units (OU)
- **Exam Rules:**
  - AWS Organizations = free service.
  - Consolidated billing = one bill for all accounts; volume discounts.
  - SCPs = restrict permissions across accounts (even root user).
  - SCPs require explicit Allow; they don't grant permissions by default.
  - Cannot restrict the master/management account with SCPs.
  - AWS Control Tower = automated multi-account setup with best practices.
- **Traps:**
  - Organizations does NOT set spending limits; use Budgets for that.
  - SCP does not affect service-linked roles.
  - Consolidated billing ≠ security; it's billing aggregation.
- **Questions covered:** Q44, Q82, Q107, Q122, Q131, Q225, Q247, Q260, Q405, Q553, Q574, Q690

---

## AWS Budgets
- **One-line definition:** Set custom cost/usage budgets and receive alerts when thresholds exceeded.
- **Keywords:** spending limits, budget alerts, cost threshold, notification, SNS
- **Exam Rules:**
  - AWS Budgets = for setting spending limits and alerts.
  - 4 budget types: Cost, Usage, Reservation, Savings Plans.
  - Up to 5 SNS notifications per budget.
  - Budgets ≠ Cost Explorer; Budgets = forward-looking alerts; Cost Explorer = historical analysis.
- **Traps:**
  - Billing Alarms (CloudWatch) = simpler; Budgets = more advanced with filtering.
  - Budgets do NOT show you cost breakdowns; they only alert.
- **Questions covered:** Q27, Q104, Q141, Q264, Q406, Q572, Q637

---

## AWS Cost Explorer
- **One-line definition:** Visualize, understand, and manage AWS costs and usage over time.
- **Keywords:** cost analysis, historical costs, forecast, rightsizing recommendations, savings plan recommendations
- **Exam Rules:**
  - Cost Explorer = analyze historical spending + forecast.
  - Can provide rightsizing recommendations for EC2.
  - Granularity: monthly, hourly, resource-level.
  - Free to access; some features like hourly granularity cost extra.
- **Traps:**
  - Cost Explorer ≠ AWS Budgets; Explorer = analysis; Budgets = alerts.
  - Cost Explorer cannot set spending limits.
- **Questions covered:** Q13, Q48, Q91, Q331, Q396, Q561, Q573, Q641, Q695, Q706

---

## AWS Trusted Advisor
- **One-line definition:** Automated best practice recommendations across cost, security, fault tolerance, performance, and service limits.
- **Keywords:** best practices, 5/6 categories, business/enterprise for full checks, 7 core checks free
- **Exam Rules:**
  - Trusted Advisor = no software to install; web-based.
  - All plans get 7 core checks for free.
  - Full checks require Business or Enterprise Support.
  - Categories: Cost optimization, Performance, Security, Fault tolerance, Service limits, Operational Excellence (new).
  - Programmatic access via AWS Support API = Business or Enterprise.
- **Traps:**
  - Trusted Advisor ≠ Inspector; Trusted Advisor = general best practices; Inspector = vulnerability scans.
  - Trusted Advisor ≠ Config; Config = configuration compliance; Trusted Advisor = recommendations.
- **Questions covered:** Q10, Q65, Q126, Q273, Q412, Q575, Q635

---

## AWS Support Plans
- **One-line definition:** Four tiers of AWS technical support with increasing capabilities.
- **Exam Rules:**
  - Basic: Free, 7 core Trusted Advisor checks, AWS Health Dashboard.
  - Developer: Business hours email support, general/system impaired response times.
  - Business: 24/7 phone/email/chat, full Trusted Advisor, API access, IEM (additional fee).
  - Enterprise On-Ramp: Pool of TAMs, concierge, 30-min for business-critical.
  - Enterprise: Designated TAM, concierge, 15-min for business-critical, IEM included.
  - TAM = Technical Account Manager; only Enterprise On-Ramp and Enterprise.
  - Concierge = billing/account help; Enterprise On-Ramp and Enterprise.
- **Traps:**
  - Business Support = full Trusted Advisor, but no TAM.
  - IEM (Infrastructure Event Management) = included in Enterprise, additional fee for Business.
  - Concierge = billing questions ONLY, not technical support.
- **Questions covered:** Q71, Q135, Q236, Q246, Q265, Q407, Q520, Q556, Q567, Q602, Q698

---

## AWS Well-Architected Framework
- **One-line definition:** Six pillars of best practices for cloud architecture.
- **Six Pillars:**
  1. **Operational Excellence** = run and monitor systems, improve processes; design principles: perform operations as code, make small reversible changes, learn from failures.
  2. **Security** = protect information and systems; design principles: least privilege, enable traceability, automate security.
  3. **Reliability** = recover from failures, meet demand; design principles: automatically recover, stop guessing capacity, scale horizontally.
  4. **Performance Efficiency** = use resources efficiently; design principles: use serverless, go global in minutes, experiment more.
  5. **Cost Optimization** = deliver value at lowest price; design principles: pay only for what you use, measure efficiency, use managed services.
  6. **Sustainability** = minimize environmental impact; design principles: maximize utilization, use managed services, reduce downstream impact.
- **Traps:**
  - Pillars are synergistic, not trade-offs.
  - High availability, scalability, agility = NOT pillars.
  - Loose coupling = design principle (Operational Excellence/Reliability).
  - "Go global in minutes" = Performance Efficiency pillar.
- **Questions covered:** Q23, Q25, Q30, Q93, Q154, Q164, Q185, Q261, Q268, Q277, Q285, Q337, Q354, Q356, Q386, Q404, Q424, Q619, Q647, Q659, Q679, Q687

---

## AWS Cloud Adoption Framework (AWS CAF)
- **One-line definition:** Guidance framework for cloud transformation with 6 perspectives.
- **Six Perspectives:**
  - **Business:** strategy, data monetization, business insights → people focused on outcomes.
  - **People:** culture, organizational alignment, organization design, cloud fluency → bridge between tech and business.
  - **Governance:** program management, portfolio management, risk management, cloud financial management, benefits management → orchestrate cloud initiatives.
  - **Platform:** data architecture, data engineering, CI/CD, platform engineering → build cloud platform.
  - **Security:** identity and access, infrastructure protection, data protection, threat detection, incident response → protect data.
  - **Operations:** event management, configuration management, patch management, performance management → cloud service delivery.
- **Four Phases:** Envision → Align → Launch → Scale.
- **Traps:**
  - CAF perspectives ≠ Well-Architected pillars.
  - People perspective = bridge; not just HR.
  - Governance ≠ Security; Governance = risk, financial, portfolio; Security = identity, protection.
- **Questions covered:** Q6, Q45, Q101, Q114, Q127, Q134, Q137, Q142, Q145, Q178, Q257, Q258, Q292, Q315, Q325, Q335, Q344, Q379, Q381, Q382, Q383, Q387, Q422, Q439, Q507, Q601, Q670, Q676, Q709

---

## AWS KMS (Key Management Service)
- **One-line definition:** Manage encryption keys for data at rest and in transit.
- **Keywords:** encryption keys, EBS encryption, S3 SSE-KMS, RDS encryption, CloudTrail logs
- **Exam Rules:**
  - KMS = AWS manages software; customer manages keys.
  - Customer Managed Keys = customer creates and controls.
  - AWS Managed Keys = AWS creates and manages for you.
  - AWS Owned Keys = used by AWS services across accounts.
  - KMS integrates with most AWS services for encryption.
- **Traps:**
  - KMS ≠ CloudHSM; KMS = software-based; CloudHSM = hardware-based, customer manages everything.
  - KMS ≠ Secrets Manager; KMS = encryption keys; Secrets Manager = credentials/secrets.
- **Questions covered:** Q74, Q219, Q418, Q449, Q636

---

## AWS Secrets Manager
- **One-line definition:** Store, manage, and automatically rotate secrets/credentials.
- **Keywords:** credentials rotation, RDS passwords, automatic rotation, Lambda rotation, KMS encryption
- **Exam Rules:**
  - Secrets Manager = auto-rotation of secrets.
  - Integrates with RDS, Aurora, etc.
  - Secrets encrypted using KMS.
  - More expensive than Parameter Store.
- **Traps:**
  - Parameter Store = configuration and secrets, NO auto-rotation.
  - Secrets Manager = best for database passwords needing auto-rotation.
  - CloudHSM ≠ Secrets Manager.
- **Questions covered:** Q72, Q120, Q158, Q217, Q423, Q526, Q623

---

## Amazon SQS (Simple Queue Service)
- **One-line definition:** Managed message queue service for decoupling applications.
- **Keywords:** queue, decouple, consumers, producers, FIFO, retention 4-14 days, delete after reading
- **Exam Rules:**
  - SQS = pull-based (consumers poll queue).
  - Standard Queue = at-least-once delivery, best-effort ordering.
  - FIFO Queue = exactly-once processing, strict ordering.
  - Messages retained up to 14 days.
  - Messages deleted after read.
  - No limit on number of messages.
- **Traps:**
  - SQS ≠ SNS; SQS = queue (one consumer per message); SNS = pub/sub (all subscribers get message).
  - SQS FIFO ≠ Kinesis; SQS FIFO = ordered queue; Kinesis = real-time streaming.
- **Questions covered:** Q81, Q140, Q188, Q376

---

## Amazon SNS (Simple Notification Service)
- **One-line definition:** Pub/sub messaging service for broadcasting notifications.
- **Keywords:** topic, subscribers, pub/sub, email, SMS, Lambda, SQS, HTTP endpoints
- **Exam Rules:**
  - SNS = push-based (sends to all subscribers).
  - One message → many subscribers.
  - No message retention; if subscriber is offline, message is lost.
  - Integrates with SQS (SNS → SQS = fan-out pattern).
- **Traps:**
  - SNS ≠ SES; SNS = multi-protocol notifications; SES = email-only.
  - SNS ≠ SQS; SNS = push to all; SQS = pull, one consumer.
- **Questions covered:** Q31, Q376, Q495

---

## Amazon EventBridge
- **One-line definition:** Serverless event bus for reacting to AWS service events and scheduling.
- **Keywords:** event rules, cron jobs, schedule, react to events, triggers, CloudWatch Events replacement
- **Exam Rules:**
  - EventBridge = formerly CloudWatch Events.
  - Schedule tasks like Lambda functions on a cron schedule.
  - React to events from AWS services.
  - Schema Registry = model event schemas.
  - Archive and replay events.
- **Questions covered:** Q502

---

## Elastic Load Balancing (ELB)
- **One-line definition:** Distribute incoming traffic across multiple targets.
- **Keywords:** ALB (HTTP/HTTPS/Layer 7), NLB (TCP/UDP/Layer 4), GLB (Layer 3/security), health checks
- **Exam Rules:**
  - ALB = Application Load Balancer; Layer 7; HTTP/HTTPS; ideal for web apps; supports WAF.
  - NLB = Network Load Balancer; Layer 4; TCP/UDP; ultra-high performance; static IP.
  - GLB = Gateway Load Balancer; Layer 3; route to security appliances (firewalls).
  - Classic LB = retired in 2023.
  - ELB distributes traffic; Auto Scaling adds/removes instances.
- **Traps:**
  - ELB does NOT auto-scale; Auto Scaling does.
  - ELB is regional; not global (use Global Accelerator for global).
- **Questions covered:** Q442, Q542, Q621, Q657

---

## Amazon EC2 Auto Scaling
- **One-line definition:** Automatically adjust the number of EC2 instances based on demand.
- **Keywords:** scale out, scale in, min/max/desired capacity, CloudWatch alarms, health checks
- **Exam Rules:**
  - Scaling strategies: Manual, Simple/Step, Target Tracking, Scheduled, Predictive.
  - Auto Scaling = scale in/out (horizontal); NOT scale up/down (vertical).
  - Integrates with ELB for distributing traffic to scaled instances.
  - Automatically replaces unhealthy instances.
- **Questions covered:** Q157, Q209, Q363, Q432, Q465, Q555

---

## Amazon EBS (Elastic Block Store)
- **One-line definition:** Persistent block storage for EC2 instances.
- **Keywords:** volume, snapshot, IOPS, network drive, AZ-bound, persistent
- **Exam Rules:**
  - EBS = attached to ONE EC2 instance at a time (at CCP level).
  - Bound to specific AZ; use snapshot to move across AZs.
  - Snapshot = backup of EBS volume; stored in S3.
  - Delete on termination = configurable; root volume deleted by default.
  - EBS Snapshot Archive = 75% cheaper; 24-72 hr restore time.
  - Recycle Bin = recover deleted snapshots.
- **Traps:**
  - EBS ≠ EFS; EBS = one EC2, one AZ; EFS = many EC2, multi-AZ.
  - EBS ≠ Instance Store; EBS = persistent; Instance Store = ephemeral.
  - Customer enables EBS encryption; KMS manages keys.
- **Questions covered:** Q231, Q593

---

## Amazon EFS (Elastic File System)
- **One-line definition:** Managed NFS file system accessible from multiple EC2 instances simultaneously.
- **Keywords:** NFS, shared file system, Linux, multi-AZ, scalable, pay per use
- **Exam Rules:**
  - EFS = works with Linux EC2 instances; NOT Windows.
  - Multi-AZ; highly available.
  - EFS-IA = Infrequent Access storage class (92% lower cost); move files via Lifecycle Policy.
  - More expensive than EBS (3x gp2 price).
  - No capacity planning needed; pay per use.
- **Traps:**
  - EFS ≠ EBS; EFS = shared; EBS = single instance.
  - EFS = Linux only; for Windows use FSx for Windows File Server.
- **Questions covered:** Q473, Q625

---

## Amazon FSx
- **One-line definition:** Managed third-party file systems on AWS.
- **Keywords:** FSx for Windows (SMB, NTFS, Active Directory), FSx for Lustre (HPC, Linux), FSx for NetApp ONTAP
- **Exam Rules:**
  - FSx for Windows = fully managed Windows file server; SMB protocol; integrates with Active Directory.
  - FSx for Lustre = HPC (High Performance Computing); Linux; scales to 100s GB/s; integrates with S3.
  - FSx File Gateway = access FSx Windows shares from on-premises without new infrastructure.
- **Traps:**
  - FSx for Windows ≠ EFS; FSx for Windows = SMB; EFS = NFS/Linux.
  - FSx for Lustre ≠ FSx for Windows; Lustre = Linux/HPC.
  - For NFS workloads migrating to S3 → S3 File Gateway; for SMB Windows → FSx File Gateway.
- **Questions covered:** Q109, Q110, Q196, Q312, Q317

---

## AWS Storage Gateway
- **One-line definition:** Hybrid storage bridge between on-premises and AWS Cloud.
- **Keywords:** hybrid storage, File Gateway (NFS/SMB to S3), Volume Gateway (iSCSI), Tape Gateway (VTL)
- **Exam Rules:**
  - File Gateway = store files in S3 using NFS/SMB protocols; locally cached.
  - Volume Gateway = expose iSCSI block storage backed by S3.
  - Tape Gateway = replace physical tape libraries with virtual tapes in S3/Glacier.
  - Use when: extending on-premises storage to cloud, disaster recovery, tiered storage.
- **Traps:**
  - Storage Gateway ≠ DataSync; Gateway = ongoing hybrid access; DataSync = migration/transfer.
  - Storage Gateway ≠ Snowball; Snowball = offline large migration; Gateway = online hybrid.
- **Questions covered:** Q3, Q90, Q103, Q205, Q255, Q364, Q533

---

## AWS Backup
- **One-line definition:** Centralized, managed backup service across AWS services.
- **Keywords:** centralize, automate, PITR, cross-region backup, cross-account
- **Exam Rules:**
  - AWS Backup = managed backup for EC2, RDS, EFS, DynamoDB, EBS, Aurora, FSx, Storage Gateway.
  - Supports PITR (Point-in-time Recovery).
  - Cross-region and cross-account backups using AWS Organizations.
- **Questions covered:** Q400, Q685

---

## AWS WAF (Web Application Firewall)
- **One-line definition:** Filter web requests to protect applications from common web exploits.
- **Keywords:** Layer 7, SQL injection, cross-site scripting (XSS), Web ACL, IP addresses, geo-block, rate-based rules
- **Exam Rules:**
  - WAF = Layer 7; protects HTTP/HTTPS traffic.
  - Deploy on: ALB, API Gateway, CloudFront.
  - Define Web ACLs with rules for IP, headers, URI, body.
  - Geo-match = block/allow countries.
  - Rate-based rules = DDoS protection at application layer.
- **Traps:**
  - WAF ≠ Shield; WAF = filter web requests; Shield = DDoS protection.
  - WAF ≠ NACLs; WAF = Layer 7; NACLs = Layer 3/4.
- **Questions covered:** Q35, Q115, Q124, Q280, Q425, Q468, Q546, Q606, Q713

---

## AWS Shield
- **One-line definition:** DDoS protection service.
- **Keywords:** DDoS, always-on, automatic mitigation, Shield Standard (free), Shield Advanced ($3,000/month)
- **Exam Rules:**
  - Shield Standard = free for all; protects against Layer 3/4 DDoS attacks.
  - Shield Advanced = $3,000/month; protects EC2, ELB, CloudFront, Global Accelerator, Route 53; includes DRT access.
  - DRT = DDoS Response Team; requires Shield Advanced.
- **Traps:**
  - Shield ≠ WAF; Shield = DDoS; WAF = web application attacks.
  - Shield Standard does NOT include DRT access.
- **Questions covered:** Q211, Q223, Q490, Q589, Q640

---

## Amazon GuardDuty
- **One-line definition:** Intelligent threat detection using ML to protect AWS accounts.
- **Keywords:** threat detection, ML, VPC Flow Logs, CloudTrail, DNS logs, malicious behavior, one-click enable
- **Exam Rules:**
  - GuardDuty = threat detection; one-click enable; 30-day free trial.
  - Analyzes: VPC Flow Logs, CloudTrail Events, DNS Logs.
  - Optional: EKS, RDS, EBS, Lambda, S3 Data Events.
  - Findings trigger EventBridge → Lambda or SNS.
  - Detects CryptoCurrency attacks.
- **Traps:**
  - GuardDuty ≠ Inspector; GuardDuty = account-level threat detection; Inspector = EC2/container vulnerability scanning.
  - GuardDuty ≠ Macie; Macie = PII in S3; GuardDuty = threats to accounts.
- **Questions covered:** Q506, Q519, Q603

---

## Amazon Macie
- **One-line definition:** Discovers and protects sensitive data (PII) in Amazon S3.
- **Keywords:** PII, sensitive data, S3 buckets, ML, pattern matching, data classification
- **Exam Rules:**
  - Macie = fully managed; uses ML and pattern matching.
  - Specifically for S3 data; finds PII.
  - Alerts via EventBridge.
- **Traps:**
  - Macie ≠ Inspector; Macie = data classification; Inspector = EC2 vulnerabilities.
  - Macie ≠ GuardDuty; Macie = sensitive data; GuardDuty = threats.
- **Questions covered:** Q58, Q159, Q229, Q286, Q416

---

## Amazon Inspector
- **One-line definition:** Automated security assessment for EC2, containers, and Lambda.
- **Keywords:** EC2 vulnerabilities, container images ECR, Lambda, SSM agent, CVE database, risk score
- **Exam Rules:**
  - Inspector = automated vulnerability scans.
  - Targets: EC2 instances (via SSM), Container images (ECR), Lambda functions.
  - Continuous scanning; reports to Security Hub.
  - NOT for general AWS account best practices (that's Trusted Advisor).
- **Traps:**
  - Inspector ≠ Trusted Advisor; Inspector = specific vulnerability scanning; Trusted Advisor = general recommendations.
  - Inspector ≠ GuardDuty; Inspector = finds vulnerabilities; GuardDuty = detects threats.
- **Questions covered:** Q2, Q117, Q175, Q693

---

## AWS Config
- **One-line definition:** Record and evaluate configuration changes to AWS resources for compliance.
- **Keywords:** configuration history, compliance, audit, SNS alerts, Athena analysis, per-region
- **Exam Rules:**
  - Config = tracks configuration changes over time.
  - Can set rules and trigger alerts for non-compliant resources.
  - Stores config data in S3; analyzed with Athena.
  - Per-region service but can aggregate across regions and accounts.
  - Config rules = detect unrestricted SSH, public S3 buckets, etc.
- **Traps:**
  - Config ≠ CloudTrail; Config = configuration state; CloudTrail = API activity.
  - Config ≠ Inspector; Config = resource compliance; Inspector = vulnerability scanning.
- **Questions covered:** Q221, Q470, Q612

---

## AWS Systems Manager (SSM)
- **One-line definition:** Manage EC2 and on-premises systems at scale.
- **Keywords:** SSM agent, Session Manager, Parameter Store, Run Command, patch management, hybrid
- **Exam Rules:**
  - Session Manager = SSH alternative; no port 22 needed; works without keys.
  - Parameter Store = secure storage for configuration and secrets; serverless; no auto-rotation.
  - SSM = hybrid service; works on EC2 and on-premises.
  - SSM Agent = installed on instances to enable SSM features.
- **Traps:**
  - Parameter Store ≠ Secrets Manager; Parameter Store = simpler, cheaper; Secrets Manager = auto-rotation.
  - Session Manager ≠ EC2 Instance Connect; Session Manager = no port 22 at all; Instance Connect = requires port 22.
- **Questions covered:** Q120, Q346

---

## Amazon ECS (Elastic Container Service)
- **One-line definition:** Run Docker containers on AWS.
- **Keywords:** containers, Docker, EC2 launch type, Fargate, task, cluster
- **Exam Rules:**
  - ECS = container orchestration; manages starting/stopping containers.
  - EC2 Launch Type = you provision EC2 instances.
  - Fargate Launch Type = serverless containers (no EC2 management).
  - ECR = Elastic Container Registry; store Docker images.
- **Questions covered:** Q492

---

## AWS Fargate
- **One-line definition:** Serverless container execution; no EC2 instances to manage.
- **Keywords:** serverless containers, Docker, no EC2 provisioning, ECS/EKS, CPU/RAM billing
- **Exam Rules:**
  - Fargate = serverless; AWS manages servers.
  - Used with ECS or EKS.
  - Billing = per vCPU and memory allocated.
  - Lambda limit = 15 min; Fargate = no time limit.
- **Traps:**
  - Fargate ≠ Lambda; Fargate = containers; Lambda = functions.
  - Lambda = 15-min limit; Fargate = no limit.
- **Questions covered:** Q7, Q440, Q552, Q590

---

## Amazon EKS (Elastic Kubernetes Service)
- **One-line definition:** Managed Kubernetes clusters on AWS.
- **Keywords:** Kubernetes, containers, cloud-agnostic, EC2 or Fargate nodes
- **Exam Rules:**
  - EKS = managed Kubernetes; open-source, cloud-agnostic.
  - Can run on EC2 or Fargate.
  - Kubernetes = container management and deployment system.
- **Questions covered:** (covered in Fargate/container questions)

---

## Amazon Athena
- **One-line definition:** Serverless SQL query service for data in Amazon S3.
- **Keywords:** serverless, S3 queries, SQL, pay per scan, CSV/JSON/ORC/Parquet
- **Exam Rules:**
  - Athena = analyze data in S3 using SQL; serverless; no infrastructure.
  - Pay per TB scanned.
  - Use with QuickSight for dashboards.
  - Keyword: "analyze data in S3 using serverless SQL → Athena"
- **Traps:**
  - Athena ≠ Redshift; Athena = serverless queries on S3; Redshift = data warehouse.
  - Athena ≠ RDS; Athena = S3 data; RDS = relational database.
- **Questions covered:** Q43, Q318, Q550, Q683

---

## AWS Glue
- **One-line definition:** Managed serverless ETL (Extract, Transform, Load) service.
- **Keywords:** ETL, data catalog, serverless, transform, prepare data, analytics
- **Exam Rules:**
  - Glue = fully managed ETL service.
  - Glue Data Catalog = central metadata repository; used by Athena, Redshift, EMR.
  - Glue = serverless.
- **Questions covered:** Q14, Q262, Q430

---

## Amazon Redshift
- **One-line definition:** Managed data warehouse for OLAP (analytics), not OLTP.
- **Keywords:** data warehouse, OLAP, SQL, columnar storage, petabyte scale, QuickSight, Redshift Serverless
- **Exam Rules:**
  - Redshift = OLAP; analytical queries on large datasets.
  - Columnar storage = better for analytics than row-based.
  - Redshift Serverless = auto-provisions capacity; no management.
  - Integrates with BI tools (QuickSight, Tableau).
- **Traps:**
  - Redshift ≠ RDS; Redshift = analytics/OLAP; RDS = transactional/OLTP.
  - Redshift ≠ Athena; Redshift = warehouse; Athena = serverless S3 queries.
- **Questions covered:** Q96, Q332, Q489

---

## Amazon QuickSight
- **One-line definition:** Serverless ML-powered BI service for interactive dashboards.
- **Keywords:** dashboards, visualizations, BI, ML insights, QuickSight Q (NLP), serverless
- **Exam Rules:**
  - QuickSight = create interactive dashboards.
  - Integrates with RDS, Aurora, Athena, Redshift, S3.
  - QuickSight Q = NLP-based query (ask questions in natural language).
- **Questions covered:** Q14, Q166, Q367, Q452, Q458, Q617

---

## AWS Snow Family
- **One-line definition:** Physical devices for large-scale data migration and edge computing.
- **Keywords:** Snowball Edge, Snowmobile, offline migration, edge computing, intermittent connectivity
- **Exam Rules:**
  - Snowball Edge Storage Optimized = 210TB storage, 104 vCPUs.
  - Snowball Edge Compute Optimized = 28TB storage, more compute.
  - Snowmobile = exabyte-scale (100PB per truck); for 10s of PB+ migrations.
  - Data transfer INTO S3 = free; device usage after included days = charged.
  - Snowball Edge = edge computing; run EC2/Lambda at edge without internet.
  - Use Snowball if data transfer over network would take >1 week.
- **Traps:**
  - Snowball Edge ≠ Snowmobile; Snowball = up to 210TB; Snowmobile = for petabytes to exabytes.
  - Snowball ≠ Storage Gateway; Snowball = offline large migration; Gateway = ongoing hybrid.
- **Questions covered:** Q1, Q151, Q191, Q270, Q276, Q355, Q671

---

## AWS Direct Connect
- **One-line definition:** Dedicated private physical connection from on-premises to AWS.
- **Keywords:** private, dedicated, physical connection, consistent bandwidth, NOT over internet, takes months to set up
- **Exam Rules:**
  - Direct Connect = private, dedicated line; bypasses public internet.
  - Takes at least 1 month to set up; requires ISP and colocation facility.
  - Provides consistent latency and bandwidth.
  - More expensive but more reliable than VPN.
- **Traps:**
  - Direct Connect ≠ VPN; Direct Connect = physical private line; VPN = encrypted over public internet.
  - Direct Connect takes months; VPN can be set up in minutes/days.
- **Questions covered:** Q21, Q73, Q326, Q357, Q466, Q547, Q616, Q630

---

## AWS VPN (Site-to-Site VPN)
- **One-line definition:** Encrypted VPN connection over public internet from on-premises to AWS.
- **Keywords:** VPN, encrypted, public internet, quick to set up, Customer Gateway, Virtual Private Gateway
- **Exam Rules:**
  - VPN = encrypted tunnel over public internet.
  - Can be set up quickly (within a week).
  - Customer Gateway (on-premises) + Virtual Private Gateway (AWS VPC).
  - AWS Client VPN = for individual users to connect from their devices.
- **Traps:**
  - VPN ≠ Direct Connect; VPN = internet-based; Direct Connect = dedicated physical.
  - VPN can have variable performance due to internet routing.
- **Questions covered:** Q608

---

## AWS Global Accelerator
- **One-line definition:** Improves global application performance by routing traffic through AWS network.
- **Keywords:** 2 Anycast IPs, TCP/UDP, no caching, edge locations, deterministic routing, static IP
- **Exam Rules:**
  - Global Accelerator = routes traffic via AWS private backbone; not cached.
  - Provides 2 static Anycast IP addresses.
  - Good for HTTP uses needing static IP or fast failover.
  - 60% performance improvement.
- **Traps:**
  - Global Accelerator ≠ CloudFront; CloudFront = caches content; Global Accelerator = routes packets.
  - Both use edge locations and integrate with Shield.
- **Questions covered:** Q80, Q86, Q208, Q321, Q663, Q707

---

## Amazon Cognito
- **One-line definition:** Identity service for web/mobile application users.
- **Keywords:** user pool, social login (Facebook/Google), mobile/web auth, millions of users
- **Exam Rules:**
  - Cognito = for external application users (NOT AWS IAM users).
  - Supports social identity providers (Facebook, Google, Twitter).
  - User pools = directory of users; identity pools = AWS credentials.
- **Traps:**
  - Cognito ≠ IAM Identity Center; Cognito = for your app's end users; IAM Identity Center = for workforce/AWS accounts.
  - Cognito ≠ IAM; IAM = AWS users; Cognito = app users.
- **Questions covered:** Q170, Q220, Q394, Q509

---

## AWS IAM Identity Center (formerly AWS SSO)
- **One-line definition:** Single sign-on for multiple AWS accounts and business applications.
- **Keywords:** SSO, multiple AWS accounts, SAML 2.0, workforce, portal, single login
- **Exam Rules:**
  - IAM Identity Center = one login for all AWS accounts in an Organization.
  - Supports SAML 2.0 applications.
  - Integrates with Active Directory (AD).
  - For workforce users accessing multiple AWS accounts.
- **Traps:**
  - IAM Identity Center ≠ Cognito; Identity Center = workforce/internal; Cognito = external app users.
  - IAM Identity Center ≠ AWS Organizations; Organizations = account management; Identity Center = access management.
- **Questions covered:** Q170, Q339, Q391, Q474, Q477, Q571, Q595

---

## AWS CloudFormation
- **One-line definition:** Infrastructure as Code; declaratively deploy AWS resources.
- **Keywords:** IaC, template, stack, YAML/JSON, declarative, repeatable, automated
- **Exam Rules:**
  - CloudFormation = free; you pay for resources created.
  - Templates define infrastructure; CloudFormation creates it in the right order.
  - Infrastructure Composer = visual tool for CloudFormation templates.
  - CDK = write IaC in programming languages; compiles to CloudFormation.
- **Traps:**
  - CloudFormation ≠ Elastic Beanstalk; CloudFormation = flexible IaC; Beanstalk = PaaS.
  - CDK ≠ CLI; CDK = programming languages for infrastructure code.
- **Questions covered:** Q19, Q78, Q100, Q187, Q305, Q353, Q487, Q517, Q583, Q591, Q629

---

## AWS Elastic Beanstalk
- **One-line definition:** Platform as a Service (PaaS) for deploying applications without managing infrastructure.
- **Keywords:** PaaS, web apps, auto provisioning, EC2/ASG/ELB/RDS managed, developer focus
- **Exam Rules:**
  - Beanstalk = free; pay for underlying resources.
  - Supports: Go, Java, .NET, Node.js, PHP, Python, Ruby, Docker.
  - Three models: Single Instance (dev), LB+ASG (production), ASG only (workers).
  - Health monitoring via CloudWatch.
- **Traps:**
  - Beanstalk ≠ CloudFormation; Beanstalk = PaaS (automated); CloudFormation = IaC (more control).
  - Beanstalk does manage infrastructure but hides complexity.
- **Questions covered:** Q17, Q193, Q323, Q366, Q397, Q451

---

## Amazon Lightsail
- **One-line definition:** Simple, low-cost cloud service for beginners with predictable pricing.
- **Keywords:** beginner, simple alternative, WordPress, LAMP, predictable pricing, bundled resources
- **Exam Rules:**
  - Lightsail = simplified alternative to EC2, RDS, ELB, Route 53.
  - Great for: simple web apps, WordPress sites, dev/test environments.
  - No auto-scaling; limited AWS integrations.
  - High availability but not auto-scaling.
- **Questions covered:** Q329, Q594

---

## Amazon Kinesis
- **One-line definition:** Real-time data streaming and analysis.
- **Keywords:** real-time streaming, Kinesis Data Streams, Kinesis Data Firehose, ingestion at scale
- **Exam Rules:**
  - Kinesis = exam keyword for "real-time data streaming."
  - Kinesis Data Streams = low-latency streaming ingestion.
  - Kinesis Data Firehose = load streaming data into S3, Redshift, OpenSearch.
- **Traps:**
  - Kinesis ≠ SQS; Kinesis = streaming analytics; SQS = decoupling applications.
- **Questions covered:** (appears as distractor; exam mostly tests keyword recognition)

---

## Amazon EMR (Elastic MapReduce)
- **One-line definition:** Managed Hadoop/big data cluster service.
- **Keywords:** Hadoop, big data, Spark, HBase, data processing, clusters, EC2 or Spot
- **Exam Rules:**
  - EMR = big data processing; Hadoop, Spark, etc.
  - Can use Spot Instances for cost savings.
  - Auto-scaling; takes care of provisioning.
- **Questions covered:** (appears mostly as distractor)

---

## Amazon Neptune
- **One-line definition:** Fully managed graph database.
- **Keywords:** graph database, social networks, fraud detection, knowledge graphs, highly connected datasets
- **Exam Rules:**
  - Neptune = graph database; for highly connected data.
  - Use cases: social networks, fraud detection, recommendation engines, knowledge graphs.
  - 3 AZ, up to 15 read replicas.
- **Questions covered:** Q308, Q484, Q588, Q672

---

## Amazon Timestream
- **One-line definition:** Managed serverless time-series database.
- **Keywords:** time-series, IoT, trillions of events per day, fast, serverless
- **Exam Rules:**
  - Timestream = for time-based data (IoT sensors, metrics, events).
  - 1000x faster and 1/10 cost of relational databases.
  - Built-in time series analytics functions.
- **Questions covered:** Q248

---

## Amazon ElastiCache
- **One-line definition:** Managed in-memory caching (Redis or Memcached).
- **Keywords:** Redis, Memcached, in-memory cache, low latency, reduce database load
- **Exam Rules:**
  - ElastiCache = cache frequently accessed data to reduce DB load.
  - Redis = more features (persistence, pub/sub, geospatial); ElastiCache with Redis.
  - DAX = in-memory cache for DynamoDB ONLY; not a general cache like ElastiCache.
- **Questions covered:** (mentioned in architecture discussions)

---

## Amazon SageMaker
- **One-line definition:** Fully managed platform to build, train, and deploy ML models.
- **Keywords:** machine learning, ML, data scientists, train models, deploy models
- **Exam Rules:**
  - SageMaker = end-to-end ML platform.
  - Covered by Savings Plans.
  - Not for specific use cases like recommendations (Personalize) or NLP (Comprehend).
- **Questions covered:** Q681

---

## Amazon Rekognition
- **One-line definition:** ML-powered image and video analysis.
- **Keywords:** image recognition, face detection, video analysis, labeling, celebrity recognition, content moderation
- **Exam Rules:**
  - Rekognition = analyze images and videos.
  - Face detection, comparison, search.
  - Content moderation, labeling.
- **Questions covered:** Q485, Q537, Q649

---

## Amazon Transcribe
- **One-line definition:** Convert speech to text (ASR - Automatic Speech Recognition).
- **Keywords:** speech to text, audio to text, subtitles, call transcription, PII redaction
- **Questions covered:** Q632

---

## Amazon Polly
- **One-line definition:** Convert text to lifelike speech (TTS - Text-to-Speech).
- **Keywords:** text to speech, lifelike, audio generation
- **Questions covered:** Q328, Q615

---

## Amazon Translate
- **One-line definition:** Neural machine translation service.
- **Keywords:** language translation, localization
- **Questions covered:** (mentioned in notes)

---

## Amazon Comprehend
- **One-line definition:** NLP service to find insights and relationships in text.
- **Keywords:** NLP, sentiment analysis, entity extraction, text classification, language detection
- **Questions covered:** Q333

---

## Amazon Lex
- **One-line definition:** Build conversational chatbots with speech and text.
- **Keywords:** chatbot, conversational AI, Alexa technology, ASR + NLP
- **Questions covered:** Q598

---

## Amazon Kendra
- **One-line definition:** ML-powered intelligent document search service.
- **Keywords:** document search, ML search, extract answers, knowledge base, FAQ
- **Questions covered:** Q320, Q699

---

## Amazon Personalize
- **One-line definition:** Real-time personalized recommendations using ML.
- **Keywords:** recommendations, personalization, retail, media, same technology as Amazon.com
- **Questions covered:** Q113

---

## Amazon Textract
- **One-line definition:** Extract text and data from documents using ML.
- **Keywords:** document analysis, OCR, forms, tables, invoices, ID documents
- **Questions covered:** (mentioned in notes)

---

## Amazon Connect
- **One-line definition:** Cloud-based contact center service with AI features.
- **Keywords:** contact center, voice calls, chat, call center, AI, Lex integration
- **Questions covered:** Q460, Q488, Q710

---

## AWS CodeDeploy
- **One-line definition:** Automate application deployments to EC2 and on-premises.
- **Keywords:** deploy, hybrid, EC2, on-premises, automated deployment, CodeDeploy agent
- **Questions covered:** Q421, Q645

---

## AWS CodeCommit
- **One-line definition:** Managed private Git repository hosting.
- **Keywords:** Git, source control, version control, private repository
- **Questions covered:** (mentioned in notes/CI-CD discussions)

---

## AWS CodeBuild
- **One-line definition:** Managed build and test service in the cloud.
- **Keywords:** compile, build, test, artifacts, serverless build
- **Questions covered:** (mentioned in CI/CD discussions)

---

## AWS CodePipeline
- **One-line definition:** Orchestrate CI/CD pipeline (Code → Build → Test → Deploy).
- **Keywords:** CI/CD, orchestration, pipeline, continuous delivery
- **Questions covered:** (mentioned in CI/CD discussions)

---

## AWS CodeStar
- **One-line definition:** Quickly set up CI/CD pipelines and development workflows.
- **Keywords:** CI/CD quick start, integrate CodeCommit, CodeBuild, CodeDeploy
- **Questions covered:** Q306

---

## AWS CDK (Cloud Development Kit)
- **One-line definition:** Define cloud infrastructure using programming languages.
- **Keywords:** TypeScript, Python, Java, .NET, programming language IaC, compiles to CloudFormation
- **Questions covered:** Q51, Q212, Q253, Q579, Q580

---

## AWS Migration Services
- **AWS Application Discovery Service:** Gather on-premises data (hostname, IP, configuration) before migration.
- **AWS Application Migration Service (MGN):** Lift-and-shift (rehost) server migration; converts physical/virtual to AWS.
- **AWS DMS (Database Migration Service):** Migrate databases homogeneous or heterogeneous; source stays available.
- **AWS DataSync:** Move large amounts of data (files) from on-premises to AWS over network; scheduled, incremental.
- **AWS Migration Hub:** Central tracking dashboard for all migration activities.
- **Migration Evaluator:** Build data-driven business case; analyze on-premises footprint, project costs.
- **AWS Schema Conversion Tool:** Convert database schema from one engine to another (use with DMS).
- **Questions covered:** Q151, Q176, Q178, Q227, Q259, Q263, Q304, Q316, Q345, Q375, Q389, Q395, Q478, Q576, Q613, Q626, Q661, Q686, Q703, Q712

---

## AWS Outposts
- **One-line definition:** AWS infrastructure deployed in customer's on-premises data center.
- **Keywords:** hybrid, on-premises, same AWS APIs, compliance, data residency, physical security = customer
- **Exam Rules:**
  - Outposts = AWS manages the rack; customer is responsible for physical security.
  - Run EC2, EBS, S3, EKS, ECS, RDS, EMR on Outposts.
  - Use when: data must remain on-premises, low latency to on-premises, compliance.
- **Traps:**
  - Outposts ≠ Local Zones; Outposts = on-premises; Local Zones = AWS-managed at edge locations.
  - Customer is responsible for physical security of Outposts racks.
- **Questions covered:** Q62, Q307, Q360, Q600, Q651, Q714, Q717

---

## AWS Local Zones
- **One-line definition:** AWS infrastructure placed closer to users in specific cities.
- **Keywords:** latency-sensitive, extension of Region, city-level, EC2/RDS/ECS/EBS/ElastiCache
- **Exam Rules:**
  - Local Zones = extend VPC to more locations; latency-sensitive apps.
  - Example: US East (N. Virginia) Region → Boston, Chicago, Dallas Local Zones.
- **Questions covered:** (distractor in Outposts questions)

---

## AWS WaveLength
- **One-line definition:** Deploy AWS services at edge of 5G networks.
- **Keywords:** 5G, ultra-low latency, telecommunications, smart cities, connected vehicles, AR/VR
- **Questions covered:** (appears as distractor)

---

## Amazon WorkSpaces
- **One-line definition:** Managed Windows/Linux virtual desktops in the cloud (DaaS).
- **Keywords:** virtual desktop, remote employees, DaaS, Windows/Linux, KMS integration
- **Exam Rules:**
  - WorkSpaces = full virtual desktop (vs. AppStream 2.0 = streams specific apps).
  - Pay-as-you-go or monthly rates.
  - AWS manages infrastructure; customer manages user accounts and MFA.
- **Questions covered:** Q309, Q346, Q549, Q694, Q704

---

## Amazon AppStream 2.0
- **One-line definition:** Stream specific desktop applications to a web browser.
- **Keywords:** stream apps to browser, lightweight clients, no VDI needed, web browser delivery
- **Exam Rules:**
  - AppStream = stream specific apps (not full desktop) to web browser.
  - Works with any device with a browser.
  - WorkSpaces = full virtual desktop; AppStream = stream specific apps.
- **Questions covered:** Q152

---

## AWS Artifact
- **One-line definition:** On-demand access to AWS compliance reports and agreements.
- **Keywords:** compliance reports, SOC, PCI, ISO, BAA, HIPAA, on-demand, auditor
- **Exam Rules:**
  - Artifact Reports = download security/compliance reports (ISO, SOC, PCI).
  - Artifact Agreements = review and accept BAA, HIPAA agreements.
  - Use for: internal audit, compliance requirements, external auditors.
- **Traps:**
  - Artifact ≠ Config; Artifact = pre-made compliance documents; Config = tracks your own resource compliance.
  - Artifact ≠ Inspector; Artifact = download reports; Inspector = scan vulnerabilities.
- **Questions covered:** Q37, Q84, Q174, Q218, Q287, Q479, Q541, Q611, Q655

---

## AWS Pricing Tools
- **AWS Pricing Calculator:** Estimate costs for new solutions BEFORE deployment.
- **AWS Budgets:** Set spending limits and get alerts when exceeded.
- **AWS Cost Explorer:** Analyze historical costs and forecast future spending.
- **AWS Cost and Usage Report:** Most comprehensive billing data; integrates with Athena/Redshift/QuickSight.
- **Billing Dashboard:** High-level overview of current costs.
- **Cost Allocation Tags:** Tag resources to track costs by department, project, etc.
- **Consolidated Billing:** One bill for all accounts in AWS Organizations; volume discounts.
- **Compute Optimizer:** Recommends right-sized EC2 based on CloudWatch metrics (free).
- **Cost Anomaly Detection:** ML-based detection of unusual spending patterns.
- **Savings Plans:** Commit to $/hour for 1 or 3 years; up to 72% savings.

---

## AWS Security Hub
- **One-line definition:** Central security dashboard aggregating findings from multiple security services.
- **Keywords:** aggregate, standardized findings, security posture, CSPM, multiple accounts
- **Exam Rules:**
  - Security Hub aggregates from: Config, GuardDuty, Inspector, Macie, IAM Access Analyzer, Firewall Manager.
  - Requires AWS Config to be enabled.
  - CSPM = Cloud Security Posture Management.
- **Questions covered:** Q53, Q284

---

## Amazon Detective
- **One-line definition:** Analyze, investigate, and identify root cause of security issues.
- **Keywords:** root cause analysis, investigation, ML, graphs, VPC Flow Logs + CloudTrail + GuardDuty
- **Exam Rules:**
  - Detective = INVESTIGATES security issues (after GuardDuty/Macie/Security Hub find them).
  - Automatically collects data from VPC Flow Logs, CloudTrail, GuardDuty.
  - Produces visualizations for root cause analysis.
- **Traps:**
  - Detective ≠ GuardDuty; GuardDuty = detects threats; Detective = investigates them.
- **Questions covered:** Q393

---

## AWS Firewall Manager
- **One-line definition:** Centrally manage security rules across multiple AWS accounts in an Organization.
- **Keywords:** centralize, WAF rules, Shield Advanced, security groups, organization-wide
- **Exam Rules:**
  - Firewall Manager = manage WAF rules, Shield Advanced, Network Firewall, VPC Security Groups across all accounts.
  - Rules applied to new resources automatically (good for compliance).
  - Requires AWS Organizations.
- **Questions covered:** Q197

---

## AWS Network Firewall
- **One-line definition:** Managed network firewall for protecting entire VPCs.
- **Keywords:** Layer 3-7, VPC protection, stateful, stateless, intrusion prevention
- **Exam Rules:**
  - Network Firewall = entire VPC-level protection; Layer 3-7.
  - WAF = web app protection; Network Firewall = full VPC protection.
- **Questions covered:** (mentioned in security discussions)

---

## Amazon API Gateway
- **One-line definition:** Fully managed service to create, publish, maintain, monitor APIs.
- **Keywords:** REST API, WebSocket, serverless API, rate limiting, authentication
- **Exam Rules:**
  - API Gateway + Lambda = serverless backend architecture.
  - Supports REST and WebSocket APIs.
  - Supports security, throttling, API keys.
- **Questions covered:** (appears in serverless architecture discussions)

---

## AWS Step Functions
- **One-line definition:** Serverless visual workflow to orchestrate Lambda functions and services.
- **Keywords:** workflow, orchestration, state machine, parallel, conditions
- **Questions covered:** Q140

---

## AWS Batch
- **One-line definition:** Fully managed batch processing for any scale.
- **Keywords:** batch jobs, start and end, EC2 or Spot, 100,000s of jobs, Docker
- **Exam Rules:**
  - Batch = for batch jobs with definite start/end; no time limit (unlike Lambda).
  - Uses EC2 or Spot Instances.
  - Jobs defined as Docker images; run on ECS.
- **Questions covered:** Q207

---

## Amazon Managed Blockchain
- **One-line definition:** Create and manage blockchain networks.
- **Keywords:** blockchain, Hyperledger Fabric, Ethereum, decentralized transactions
- **Questions covered:** (mentioned in notes)

---

## AWS STS (Security Token Service)
- **One-line definition:** Create temporary, limited-privilege credentials for AWS access.
- **Keywords:** temporary credentials, federated identity, cross-account, IAM role assumption
- **Exam Rules:**
  - STS = generates temporary security credentials.
  - Used for: federated users, cross-account access, EC2 role assumption.
  - Credentials have configurable expiration.
- **Questions covered:** Q52, Q279, Q620

---

## AWS CloudHSM
- **One-line definition:** Hardware Security Module for managing your own encryption keys on dedicated hardware.
- **Keywords:** hardware, HSM, FIPS 140-2 Level 3, customer manages keys, dedicated hardware
- **Exam Rules:**
  - CloudHSM = AWS provisions hardware; customer manages keys.
  - KMS = AWS manages software; customer controls keys.
  - FIPS 140-2 Level 3 compliant.
- **Traps:**
  - CloudHSM ≠ KMS; CloudHSM = hardware; KMS = software-based.
- **Questions covered:** Q418, Q449

---

## AWS Compute Optimizer
- **One-line definition:** ML-based recommendations to right-size AWS resources.
- **Keywords:** rightsizing, EC2, EBS, Lambda, Auto Scaling, CloudWatch metrics, up to 25% lower costs
- **Exam Rules:**
  - Compute Optimizer = analyzes CloudWatch metrics to recommend right-sized resources.
  - Supports: EC2, EC2 Auto Scaling Groups, EBS volumes, Lambda.
  - Recommendations exportable to S3.
- **Questions covered:** Q9, Q399, Q682

---

## AWS Trusted Advisor vs. Compute Optimizer
- Trusted Advisor = general best practices (security, cost, performance, fault tolerance, service limits).
- Compute Optimizer = specific rightsizing recommendations based on actual usage data.

---

## AWS Migration Strategies: The 7Rs
| Strategy | Description | Effort |
|---|---|---|
| Retire | Turn off unneeded apps | Lowest |
| Retain | Keep on-premises for now | None |
| Relocate | Move to cloud version (e.g., VMware to VMware Cloud on AWS) | Low |
| Rehost (Lift and Shift) | Migrate as-is to EC2; no changes | Low-Medium |
| Replatform (Lift and Reshape) | Minor optimizations (e.g., move to RDS) | Medium |
| Repurchase (Drop and Shop) | Move to SaaS (e.g., Salesforce) | Medium-High |
| Refactor (Re-architect) | Redesign using cloud-native features; microservices | Highest |

---

# PART 3: High-Yield Keywords

| Keyword in Question | Choose This | Why |
|---|---|---|
| static content + global users + low latency | CloudFront | CDN edge caching |
| object storage + unlimited scale + durable | S3 | Object storage service |
| relational database + managed + no OS patching | RDS | Managed SQL database |
| NoSQL + key-value + serverless + millisecond | DynamoDB | Managed NoSQL |
| serverless code + event-driven + no servers | Lambda | FaaS |
| audit API calls + who did what + event history | CloudTrail | Records all API activity |
| metrics + alarms + monitoring + CPU utilization | CloudWatch | Monitoring and alerting |
| DNS + domain routing + failover routing | Route 53 | Managed DNS |
| block SQL injection + XSS + Layer 7 web attacks | AWS WAF | Web Application Firewall |
| DDoS protection + always-on | AWS Shield | DDoS protection |
| encryption keys + data at rest | AWS KMS | Key management |
| secrets rotation + database credentials auto-rotate | Secrets Manager | Secret storage with rotation |
| cost alert + spending limit + budget notification | AWS Budgets | Budget notifications |
| cost analysis + historical spending + forecast | Cost Explorer | Cost visualization |
| best practice recommendations + 5 categories | Trusted Advisor | AWS best practice checks |
| compliance reports + SOC + PCI + ISO + auditor | AWS Artifact | On-demand compliance docs |
| threat detection + ML + VPC Flow Logs + CloudTrail | Amazon GuardDuty | Threat detection |
| EC2 vulnerabilities + container images + Lambda scanning | Amazon Inspector | Vulnerability scanning |
| PII + sensitive data + S3 + data classification | Amazon Macie | Data classification |
| configuration compliance + track changes + audit | AWS Config | Configuration compliance |
| multi-account management + SCP + consolidated billing | AWS Organizations | Multi-account governance |
| single sign-on + multiple AWS accounts + SAML | IAM Identity Center | SSO for workforce |
| mobile/web app users + social login | Amazon Cognito | App identity |
| temporary credentials + federated access | AWS STS | Temporary security tokens |
| IaC + YAML/JSON + declarative | CloudFormation | Infrastructure as Code |
| IaC + programming languages (Python, TypeScript) | AWS CDK | Code-based IaC |
| PaaS + deploy app without managing servers + web app | Elastic Beanstalk | Managed application platform |
| containers + serverless + no EC2 provisioning | AWS Fargate | Serverless containers |
| containers + Docker + managed orchestration + EC2 | Amazon ECS | Container orchestration |
| Kubernetes + managed | Amazon EKS | Managed Kubernetes |
| SQL queries + S3 + serverless + pay per scan | Amazon Athena | Serverless S3 queries |
| ETL + transform data + managed + serverless | AWS Glue | Managed ETL |
| data warehouse + OLAP + petabyte + columnar | Amazon Redshift | Data warehouse |
| BI dashboards + visualizations + ML insights | Amazon QuickSight | Business intelligence |
| real-time streaming + millions of records | Amazon Kinesis | Real-time data streaming |
| big data + Hadoop + Spark + clusters | Amazon EMR | Big data processing |
| graph database + fraud detection + social networks | Amazon Neptune | Graph database |
| time-series data + IoT + trillions of events | Amazon Timestream | Time-series database |
| in-memory cache + Redis + reduce DB load | Amazon ElastiCache | Caching service |
| hybrid storage + on-premises + locally cached + NFS | AWS Storage Gateway | Hybrid storage bridge |
| offline large data migration + no internet | AWS Snow Family | Physical data migration |
| >50 petabytes migration | AWS Snowmobile | Exabyte-scale migration |
| edge computing + intermittent connectivity + offline | AWS Snowball Edge | Edge compute and storage |
| dedicated private connection + on-premises + physical | AWS Direct Connect | Private dedicated network |
| encrypted VPN + public internet + on-premises + quick | AWS Site-to-Site VPN | VPN connection |
| global application performance + no caching + static IP | AWS Global Accelerator | Global routing optimization |
| CDN + edge caching + global users | Amazon CloudFront | Content Delivery Network |
| S3 fast uploads from anywhere + edge locations | S3 Transfer Acceleration | Accelerated S3 uploads |
| connect VPCs + on-premises + hub + thousands | AWS Transit Gateway | Network hub |
| private subnet + internet access + outbound only | NAT Gateway | Private subnet internet |
| internet access to VPC + inbound | Internet Gateway | VPC internet gateway |
| access AWS services without internet from VPC | VPC Endpoint | Private AWS service access |
| private connectivity to AWS services + 3rd party VPCs | AWS PrivateLink | Private service connectivity |
| connect two VPCs privately | VPC Peering | VPC-to-VPC connection |
| on-premises with same AWS APIs + compliance | AWS Outposts | AWS on-premises |
| 5G edge + ultra-low latency | AWS WaveLength | 5G edge computing |
| latency-sensitive + city-level + AWS resources closer | AWS Local Zones | City-level extension |
| virtual desktop + remote employees + Windows/Linux | Amazon WorkSpaces | Cloud virtual desktop |
| stream apps to browser + lightweight clients | Amazon AppStream 2.0 | Application streaming |
| speech to text + ASR + transcription | Amazon Transcribe | Speech recognition |
| text to speech + lifelike + audio | Amazon Polly | Text-to-speech |
| image/video analysis + face detection + labeling | Amazon Rekognition | Image/video ML |
| NLP + text analysis + sentiment + entity | Amazon Comprehend | Natural language processing |
| build chatbots + conversational AI + chatbot | Amazon Lex | Chatbot service |
| document search + intelligent + ML powered | Amazon Kendra | Intelligent document search |
| product recommendations + real-time + personalization | Amazon Personalize | ML recommendations |
| extract text from documents + OCR + invoices | Amazon Textract | Document text extraction |
| language translation + localize content | Amazon Translate | Language translation |
| ML platform + build train deploy models | Amazon SageMaker | Full ML platform |
| contact center + voice + chat + AI | Amazon Connect | Cloud contact center |
| blockchain + decentralized | Amazon Managed Blockchain | Blockchain service |
| message queue + decouple apps + consumers poll | Amazon SQS | Queuing service |
| pub/sub + notify all subscribers + topic | Amazon SNS | Notification service |
| event bus + react to events + schedule cron | Amazon EventBridge | Event routing |
| distribute traffic + multiple EC2 + HTTP | Application Load Balancer | Layer 7 load balancing |
| TCP/UDP + ultra-high performance + static IP | Network Load Balancer | Layer 4 load balancing |
| security appliances + 3rd party firewall routing | Gateway Load Balancer | Layer 3 security routing |
| auto add/remove EC2 based on demand | EC2 Auto Scaling | Horizontal scaling |
| rightsize EC2 + reduce costs + ML recommendations | AWS Compute Optimizer | Rightsizing |
| card that combines NLP with BI dashboards | Amazon QuickSight Q | NLP-powered BI |
| central hub for migration tracking | AWS Migration Hub | Migration visibility |
| discover on-premises servers + pre-migration | AWS Application Discovery Service | Pre-migration discovery |
| lift and shift servers to AWS | AWS Application Migration Service | Server migration |
| database migration + source remains available | AWS DMS | Database migration |
| file data migration + network + scheduled | AWS DataSync | File data migration |
| pre-migration cost estimate | AWS Pricing Calculator | Cost estimation |
| data-driven business case + on-premises footprint | Migration Evaluator | Migration business case |
| carbon footprint + sustainability + track emissions | AWS Customer Carbon Footprint Tool | Sustainability tracking |
| log network traffic + VPC + subnet | VPC Flow Logs | Network traffic logs |
| security aggregation + CSPM + multiple accounts | AWS Security Hub | Security posture management |
| investigate security incidents + root cause | Amazon Detective | Security investigation |
| manage WAF + Shield + security groups + organization-wide | AWS Firewall Manager | Cross-account security |
| hardware key management + FIPS 140-2 + customer manages | AWS CloudHSM | Hardware key security |
| compliance, configuration, and remediation | AWS Config | Configuration compliance |
| centrally manage and automate backup | AWS Backup | Centralized backup |
| managed Windows file server + SMB | Amazon FSx for Windows File Server | Windows file system |
| HPC + Linux + high performance + Lustre | Amazon FSx for Lustre | HPC file system |
| NFS file system + Linux + multi-EC2 | Amazon EFS | Shared Linux file system |
| block storage + single EC2 + persistent | Amazon EBS | Block storage |
| ephemeral storage + lost when EC2 stops | EC2 Instance Store | Temporary storage |
| pre-defined products + governance + authorized | AWS Service Catalog | IT product governance |
| share resources between AWS accounts | AWS Resource Access Manager (RAM) | Resource sharing |
| Windows Active Directory + on-premises + trust | AWS Directory Services | Active Directory |
| manage multiple accounts + guardrails + automated | AWS Control Tower | Multi-account setup |
| marketing communications + SMS + email + segments | Amazon Pinpoint | Marketing communications |
| IoT devices + connect to cloud | AWS IoT Core | IoT connectivity |
| data sync for mobile/web + offline + GraphQL | AWS AppSync | Mobile data sync |
| full stack web/mobile development tools | AWS Amplify | Full-stack development |
| visually design serverless apps | AWS Application Composer (Infrastructure Composer) | Serverless visual design |
| test web/mobile apps on real devices | AWS Device Farm | App testing |
| disaster recovery + quick recovery + block-level replication | AWS Elastic Disaster Recovery | Disaster recovery |
| satellite communications + ground stations | AWS Ground Station | Satellite management |
| IoT on 5G + WaveLength zones + ultra-low latency | AWS WaveLength | 5G edge computing |

---

# PART 4: Common Traps and Comparisons

## 1. CloudTrail vs. CloudWatch

| Feature | CloudTrail | CloudWatch |
|---|---|---|
| Purpose | API audit logging | Metrics and monitoring |
| What it tracks | Who did what (API calls) | Performance metrics, logs |
| Use case | "Who deleted this resource?" | "Is CPU usage high?" |
| Default | Enabled by default | Some metrics enabled |
| Storage | S3, CloudWatch Logs | CloudWatch Logs |
| Keywords | audit, governance, compliance, API calls | metrics, alarms, dashboards, performance |

---

## 2. S3 vs. EBS vs. EFS

| Feature | S3 | EBS | EFS |
|---|---|---|---|
| Type | Object storage | Block storage | File system (NFS) |
| Access | Anywhere via HTTPS | One EC2 (at a time) | Many EC2 simultaneously |
| AZ scope | Regional/global | Single AZ | Multi-AZ |
| Use case | Images, backups, static websites | OS volume, databases | Shared files, CMS, home directories |
| Persistent | Yes | Yes (until deleted) | Yes |
| OS | N/A | Any | Linux only |
| Scalable | Unlimited | Up to 64TB | Unlimited, auto-scale |
| Keywords | object, bucket, unlimited, S3 | volume, block, EC2 | shared, NFS, Linux, multi-AZ |

---

## 3. RDS vs. DynamoDB

| Feature | RDS | DynamoDB |
|---|---|---|
| Type | Relational (SQL) | NoSQL (key-value) |
| Schema | Fixed schema | Flexible schema |
| Query | SQL | Key-value, document |
| Scale | Vertical + read replicas | Horizontal, serverless |
| Use case | Structured data, transactions | Large-scale, low-latency, flexible |
| Keywords | SQL, relational, structured, join | NoSQL, key-value, serverless, ms latency |

---

## 4. CloudFront vs. S3 Transfer Acceleration

| Feature | CloudFront | S3 Transfer Acceleration |
|---|---|---|
| Purpose | Cache content at edge for fast delivery | Speed up uploads/downloads to S3 |
| Direction | Download (to users) | Upload (to S3 bucket) |
| Caching | Yes (TTL-based) | No caching |
| Origin | S3, EC2, ALB, custom | Only S3 |
| Use case | Static websites, videos, APIs | Large file uploads from far locations |
| Keywords | CDN, global delivery, cache | fast uploads, S3 transfers, edge acceleration |

---

## 5. Security Group vs. NACL

| Feature | Security Group | Network ACL (NACL) |
|---|---|---|
| Level | Instance level | Subnet level |
| State | Stateful (return traffic automatic) | Stateless (return traffic needs rule) |
| Rules | Allow only | Allow AND Deny |
| Rule evaluation | All rules evaluated | Rules in order (lowest number first) |
| Default | All inbound denied; all outbound allowed | All traffic allowed |
| Keywords | instance firewall, stateful, allow only | subnet firewall, stateless, allow/deny |

---

## 6. IAM User vs. IAM Role vs. IAM Policy

| Feature | IAM User | IAM Role | IAM Policy |
|---|---|---|---|
| What | Identity for a person | Identity for services or cross-account | Permissions document |
| Credentials | Username/password, access keys | Temporary credentials (STS) | JSON document |
| Use case | Developers, employees | EC2 accessing S3, Lambda, cross-account | Define what actions are allowed |
| Permanence | Long-term | Temporary | Attached to user/group/role |
| Keywords | individual user, access keys | assume role, temporary, service | JSON, allow/deny, actions, resources |

---

## 7. KMS vs. Secrets Manager vs. Parameter Store

| Feature | AWS KMS | AWS Secrets Manager | SSM Parameter Store |
|---|---|---|---|
| Purpose | Encryption key management | Store and rotate secrets/credentials | Store configuration and secrets |
| Auto-rotation | No | Yes (via Lambda) | No |
| Cost | Per-key, per-request | Per secret/per rotation | Free (standard); paid (advanced) |
| Best for | Encrypting data at rest | Database passwords needing auto-rotation | App configuration, config + basic secrets |
| Keywords | encryption keys, KMS keys | auto-rotate, database credentials | config, parameter, no auto-rotation |

---

## 8. SNS vs. SQS vs. EventBridge

| Feature | SNS | SQS | EventBridge |
|---|---|---|---|
| Model | Pub/Sub (push) | Queue (pull) | Event bus (rule-based) |
| Delivery | All subscribers instantly | Pulled by one consumer | Routed to targets based on rules |
| Persistence | No (lost if subscriber offline) | Up to 14 days | Archive support |
| Use case | Broadcast notifications | Decouple applications | React to AWS service events, schedule |
| Keywords | pub/sub, topic, broadcast | queue, decouple, FIFO | events, rules, schedule, cron, react |

---

## 9. Auto Scaling vs. Load Balancer

| Feature | Auto Scaling | Load Balancer |
|---|---|---|
| Purpose | Change the NUMBER of EC2 instances | Distribute traffic across EC2 instances |
| Scaling type | Horizontal (scale out/in) | Does NOT scale |
| Health checks | Replaces unhealthy instances | Directs traffic away from unhealthy |
| Triggers | CloudWatch alarms, schedules | Incoming requests |
| Keywords | add/remove instances, scale in/out | distribute traffic, single endpoint |

---

## 10. Route 53 Routing Policies

| Policy | Description | Use case |
|---|---|---|
| Simple | Route to one resource, no health checks | Single resource |
| Weighted | Distribute % of traffic | A/B testing, blue/green |
| Latency | Route to lowest latency region | Global apps |
| Failover | Route to primary; failover to secondary | Disaster recovery |
| Geolocation | Route based on user's location | Compliance, localization |
| Geoproximity | Route based on geographic distance | Advanced routing |
| Multivalue Answer | Return multiple IPs (basic load balancing) | Simple distribution |

---

## 11. Reserved Instances vs. Savings Plans vs. Spot Instances

| Feature | Reserved Instances | Savings Plans | Spot Instances |
|---|---|---|---|
| Discount | Up to 72% | Up to 72% | Up to 90% |
| Commitment | 1 or 3 years (specific instance type/region) | 1 or 3 years ($/hour spend) | None |
| Flexibility | Standard (fixed) or Convertible (flexible type) | Compute (any instance), EC2 (family), SageMaker | Bid on unused capacity |
| Interruption | No | No | YES (can be interrupted) |
| Use case | Steady-state, predictable | Flexible long-term | Fault-tolerant, interruptible |
| Sell unused | Yes (RI Marketplace) | No | N/A |
| Keywords | 1/3 year, committed, steady-state | flexible commitment, compute | interruptible, cheapest, batch |

---

## 12. AWS Shield vs. WAF vs. GuardDuty vs. Inspector vs. Macie

| Service | Protects Against | Level | Keywords |
|---|---|---|---|
| AWS Shield | DDoS attacks | Network/Transport (L3/L4) | DDoS, automatic, always-on |
| AWS WAF | Web exploits (SQL injection, XSS) | Application (L7) | Web app, rules, filter, SQL injection |
| Amazon GuardDuty | Account threats, compromised instances | Account/workload | Threat detection, ML, VPC Logs, CloudTrail |
| Amazon Inspector | EC2/container/Lambda vulnerabilities | Resource level | Vulnerability scanning, CVE, assessment |
| Amazon Macie | Sensitive data (PII) in S3 | Data level | PII, sensitive data, S3, classification |

---

## 13. AWS Organizations vs. IAM Identity Center

| Feature | AWS Organizations | IAM Identity Center |
|---|---|---|
| Purpose | Manage multiple AWS accounts | Single sign-on for workforce |
| Function | Create accounts, apply SCPs, consolidated billing | SSO portal for AWS accounts and apps |
| Scope | Account-level governance | User access management |
| Keywords | multiple accounts, SCP, consolidated billing, OU | SSO, single login, SAML, workforce |

---

## 14. Cost Explorer vs. Budgets vs. Cost and Usage Report

| Feature | Cost Explorer | AWS Budgets | Cost and Usage Report (CUR) |
|---|---|---|---|
| Purpose | Analyze historical costs and forecast | Set limits and receive alerts | Most comprehensive raw billing data |
| Use case | Understand spending patterns | Set monthly budget alerts | Detailed data for analysis with Athena |
| Direction | Backward-looking (historical) + forecast | Forward-looking (alerts) | Historical (most detailed) |
| Integration | — | SNS for alerts | Athena, Redshift, QuickSight |
| Keywords | analyze, visualize, forecast, rightsizing | alert, limit, threshold | comprehensive, all data, line items |

---

## 15. Shared Responsibility Model

| Responsibility | AWS | Customer |
|---|---|---|
| Physical security | ✅ Data centers, hardware | ❌ |
| Infrastructure | ✅ Network, hypervisor, hardware | ❌ |
| Host OS | ✅ For managed services | ✅ For EC2 |
| Guest OS | ❌ | ✅ EC2 patches |
| Application | ❌ | ✅ |
| Data | ❌ | ✅ Encryption, data management |
| IAM | ❌ | ✅ Users, roles, policies |
| Network firewalls | ❌ (provide tools) | ✅ Configure security groups, NACLs |
| Encryption | ❌ (provide KMS) | ✅ Enable encryption, manage keys |
| Shared | Both | Patch Management, Configuration Management |

**Key exam rules:**
- RDS: AWS patches OS/DB engine; customer manages access, data, encryption settings.
- S3: AWS manages infrastructure; customer manages bucket policy, versioning, encryption.
- Lambda: AWS manages hardware, OS, runtime; customer manages code, IAM, environment.
- DynamoDB: AWS manages OS and infrastructure; customer manages data, access permissions.
- EC2: Customer manages guest OS patches, applications, security groups; AWS manages hardware.

---

# PART 5: Cloud Practitioner Core Concepts

## AWS Global Infrastructure

| Component | Description | Exam Notes |
|---|---|---|
| AWS Region | Geographic cluster of data centers (e.g., us-east-1) | Most services are region-scoped |
| Availability Zone (AZ) | 1+ data centers in a region; isolated from disasters | Min 3 per region, max 6; connected with low-latency |
| Edge Location | Points of Presence for CDN; 400+ globally | Used by CloudFront, Route 53, Global Accelerator |
| Local Zone | Extension of Region to cities for latency-sensitive apps | Subset of Region services |
| Wavelength Zone | AWS at 5G network edge; ultra-low latency | Telecommunications; smart cities, AR/VR |
| AWS Outposts | AWS infrastructure at customer's data center | Customer responsible for physical security |

**Infrastructure relationships:**
- More edge locations than AZs.
- More AZs than Regions.
- Edge locations ≠ Availability Zones.

---

## AWS Pricing Models

| Model | Description | Use Case | Keywords |
|---|---|---|---|
| On-Demand | Pay by second (Linux/Windows) or hour; no commitment | Short-term, unpredictable, tests | flexible, no commitment |
| Reserved Instances | 1 or 3 year commitment; up to 72% off | Steady-state, predictable, 1+ year | commitment, steady-state |
| Savings Plans | Commit to $/hour for 1 or 3 years; up to 72% off | Flexible long-term; covers EC2, Fargate, Lambda, SageMaker | flexible, compute savings |
| Spot Instances | Bid on unused capacity; up to 90% off; CAN BE INTERRUPTED | Fault-tolerant, interruptible, batch | cheapest, interruptible |
| Dedicated Hosts | Physical server dedicated to you; BYOL licensing | Compliance, BYOL software | physical server, licensing |
| Dedicated Instances | Hardware dedicated to account; less control | Hardware isolation without full server | isolated hardware |
| Capacity Reservations | Reserve capacity in AZ; billed at On-Demand rate | Guarantee capacity availability | reserved capacity, no discount |

---

## Five Advantages of Cloud Computing (from course notes)

1. **Trade capital expense (CAPEX) for operational expense (OPEX)** — pay-as-you-go, no upfront hardware.
2. **Benefit from massive economies of scale** — AWS's aggregate usage = lower prices for everyone.
3. **Stop guessing capacity** — scale up/down based on actual demand.
4. **Increase speed and agility** — resources available in minutes.
5. **Stop spending money running and maintaining data centers** — focus on business.
6. **Go global in minutes** — leverage global infrastructure.

---

## Five Characteristics of Cloud Computing

1. **On-demand self-service** — provision without human interaction.
2. **Broad network access** — access over network from any platform.
3. **Multi-tenancy and resource pooling** — multiple customers share infrastructure.
4. **Rapid elasticity and scalability** — scale based on demand.
5. **Measured service** — pay for what you use.

---

## Cloud Deployment Models

| Model | Description | Keywords |
|---|---|---|
| Public Cloud | Resources owned by cloud provider; delivered over internet | AWS, Azure, GCP |
| Private Cloud | Cloud used by single organization; not public | On-premises, complete control |
| Hybrid Cloud | Mix of on-premises and public cloud | Outposts, VPN, Direct Connect, Storage Gateway |

---

## Service Models

| Model | AWS Example | Who Manages Infrastructure |
|---|---|---|
| IaaS | EC2 | Customer manages OS, apps |
| PaaS | Elastic Beanstalk | Provider manages infrastructure |
| SaaS | Rekognition, Gmail | Provider manages everything |

---

# PART 6: Final Exam Cheat Sheet

| Service | One-line meaning | Exam keyword |
|---|---|---|
| IAM | Manage AWS access | users, roles, policies, MFA, least privilege |
| S3 | Object storage | buckets, unlimited, durable, static files |
| EC2 | Virtual servers | compute, VM, instance, AMI |
| RDS | Managed relational DB | SQL, MySQL, PostgreSQL, Multi-AZ |
| DynamoDB | Managed NoSQL DB | key-value, serverless, millisecond latency |
| Lambda | Serverless functions | run code, no servers, 15-min limit |
| CloudFront | CDN | edge caching, global delivery, static content |
| Route 53 | DNS service | domain, routing policies, failover |
| VPC | Virtual private network | subnets, internet gateway, NAT, peering |
| CloudWatch | Monitoring | metrics, alarms, logs, dashboards |
| CloudTrail | API audit logs | who did what, governance, compliance |
| AWS Organizations | Multi-account management | consolidated billing, SCP, OU |
| AWS Budgets | Spending alerts | cost threshold, notification, limit |
| Cost Explorer | Cost analysis | historical costs, forecast, visualization |
| Trusted Advisor | Best practice checks | 5 categories, recommendations |
| AWS Artifact | Compliance docs | SOC, PCI, ISO, download, auditor |
| KMS | Encryption keys | encrypt at rest, key management |
| Secrets Manager | Credential rotation | auto-rotate, database passwords |
| SSM Parameter Store | Config storage | parameters, no auto-rotation, cheaper |
| SQS | Message queue | decouple, FIFO, consumers poll |
| SNS | Pub/sub notifications | topic, broadcast, push, subscribers |
| EventBridge | Event routing | react to events, schedule, cron |
| ALB | HTTP/HTTPS load balancer | Layer 7, web apps, WAF |
| NLB | TCP/UDP load balancer | Layer 4, ultra-high performance, static IP |
| EC2 Auto Scaling | Add/remove EC2 | scale in/out, dynamic, CloudWatch trigger |
| EBS | Block storage | EC2 volume, persistent, AZ-bound |
| EFS | Shared file system | NFS, Linux, multi-AZ, multi-EC2 |
| FSx Windows | Windows file server | SMB, NTFS, Active Directory |
| FSx Lustre | HPC file system | Linux, high-performance, S3 integration |
| Storage Gateway | Hybrid storage | on-premises + cloud, locally cached |
| AWS Backup | Centralized backup | automate, cross-region, PITR |
| Snowball Edge | Edge computing + data migration | offline, intermittent connectivity, <210TB |
| Snowmobile | Massive data migration | exabyte-scale, >50PB, physical truck |
| Direct Connect | Private dedicated network | physical, consistent, no internet |
| VPN (Site-to-Site) | Encrypted VPN | public internet, quick setup, Customer Gateway |
| Global Accelerator | Global routing optimization | TCP/UDP, no caching, static Anycast IP |
| S3 Transfer Acceleration | Fast S3 uploads | edge locations, large files |
| Transit Gateway | Network hub | connect many VPCs + on-premises |
| NAT Gateway | Private subnet internet | outbound only, private subnet |
| Internet Gateway | VPC internet access | inbound/outbound, public subnet |
| VPC Endpoint | Private AWS service access | no internet, S3/DynamoDB |
| PrivateLink | Private VPC service connectivity | 3rd party services, private |
| VPC Peering | VPC-to-VPC connection | non-transitive, private |
| VPC Flow Logs | Network traffic logging | IP traffic, monitoring, troubleshooting |
| AWS WAF | Web application firewall | Layer 7, SQL injection, XSS, geo-block |
| AWS Shield | DDoS protection | always-on, automatic, Layer 3/4 |
| GuardDuty | Threat detection | ML, VPC logs, CloudTrail, threats |
| Inspector | Vulnerability scanning | EC2, containers, Lambda, CVE |
| Macie | PII data classification | S3, sensitive data, ML |
| Config | Configuration compliance | track changes, audit, remediation |
| Security Hub | Security aggregation | CSPM, findings from multiple services |
| Detective | Security investigation | root cause, ML, graphs |
| Firewall Manager | Cross-account security rules | WAF, Shield, organization-wide |
| CloudHSM | Hardware key management | FIPS 140-2, dedicated hardware, customer manages |
| STS | Temporary credentials | federated, cross-account, assume role |
| Cognito | App user identity | mobile/web users, social login |
| IAM Identity Center | SSO for workforce | multiple AWS accounts, SAML, portal |
| CloudFormation | Infrastructure as Code | YAML/JSON, stack, declarative |
| CDK | Code-based IaC | Python, TypeScript, compiles to CloudFormation |
| Elastic Beanstalk | PaaS | deploy app without managing infra |
| ECS | Docker container orchestration | containers, EC2 launch type |
| Fargate | Serverless containers | no EC2, Docker, no time limit |
| EKS | Managed Kubernetes | Kubernetes, cloud-agnostic |
| ECR | Docker image registry | private container registry |
| Athena | Serverless S3 queries | SQL, pay per scan, serverless |
| Glue | ETL service | extract, transform, load, serverless |
| Redshift | Data warehouse | OLAP, columnar, petabyte-scale |
| QuickSight | BI dashboards | visualizations, ML insights, serverless |
| Kinesis | Real-time streaming | streaming data, real-time analytics |
| EMR | Big data clusters | Hadoop, Spark, managed |
| Neptune | Graph database | social networks, fraud, highly connected |
| Timestream | Time-series database | IoT, trillions of events, time-based |
| ElastiCache | In-memory caching | Redis, Memcached, low latency |
| Batch | Batch job processing | jobs, start/end, EC2/Spot |
| API Gateway | API management | REST, WebSocket, serverless backend |
| Step Functions | Workflow orchestration | state machine, Lambda orchestration |
| SageMaker | ML platform | build, train, deploy models |
| Rekognition | Image/video ML | faces, labels, content moderation |
| Transcribe | Speech to text | ASR, audio, subtitles |
| Polly | Text to speech | lifelike audio, accessibility |
| Comprehend | NLP | sentiment, entities, classification |
| Lex | Chatbot builder | conversational AI, Alexa tech |
| Kendra | Document search | ML search, FAQ, knowledge base |
| Personalize | Recommendations | real-time, ML, retail |
| Textract | Document extraction | OCR, forms, tables, invoices |
| Translate | Language translation | localization, multilingual |
| Connect | Cloud contact center | voice, chat, AI, call center |
| WorkSpaces | Virtual desktop (DaaS) | remote employees, Windows/Linux |
| AppStream 2.0 | App streaming | browser-based, lightweight clients |
| Outposts | AWS on-premises | hybrid, compliance, same APIs |
| Local Zones | City-level AWS | latency-sensitive, extension of Region |
| WaveLength | 5G edge | ultra-low latency, telecommunications |
| IoT Core | IoT connectivity | billions of devices, serverless |
| Migration Evaluator | Migration business case | on-premises baseline, projected costs |
| Application Discovery Service | Pre-migration discovery | hostname, IP, configuration, server data |
| Application Migration Service | Server migration (lift and shift) | rehost, convert servers to AWS |
| DMS | Database migration | homogeneous/heterogeneous, source stays up |
| DataSync | File data migration | network-based, scheduled, incremental |
| Migration Hub | Migration tracking | central visibility, progress tracking |
| Lightsail | Beginner cloud | simple apps, WordPress, predictable pricing |
| AWS Marketplace | Third-party software | ISV software, AMIs, SaaS, containers |
| Service Catalog | Approved product catalog | governance, IaC templates, compliance |
| Compute Optimizer | EC2 rightsizing | ML, CloudWatch metrics, recommendations |
| Cost Anomaly Detection | Unusual cost detection | ML, cost spikes, alerts |
| Customer Carbon Footprint Tool | Sustainability tracking | emissions, renewable energy path |
| AWS Professional Services | Cloud adoption consulting | expert guidance, paid engagements |
| AWS Partner Network (APN) | AWS certified partners | consulting, technology partners |
| AWS re:Post | Community Q&A | crowd-sourced, expert-reviewed answers |
| AWS IQ | Expert marketplace | certified third-party experts, paid projects |
| AWS Managed Services (AMS) | Fully managed operations | reduce operational overhead, security, compliance |

---

# PART 7: Coverage Check

## Coverage Summary

- **Total questions found:** 720 (Q1-Q719/720)
- **Questions analyzed:** 720
- **Missing/unclear questions:** 0
- **Services covered:** 100+ AWS services including all major services from notes and dump
- **AWS Certification path questions:** Included in framework sections

## Services from Notes But Not Heavily Tested in Dump

The following services appear in course notes but have minimal or indirect question coverage:

- **AWS AppSync** (mobile data sync with GraphQL)
- **AWS Amplify** (full-stack mobile/web development)
- **AWS IoT Core** (IoT device connectivity)
- **Amazon Pinpoint** (marketing communications)
- **AWS Ground Station** (satellite communications)
- **Amazon Elastic Transcoder** (media format conversion) — Q622
- **Amazon DMS Schema Conversion Tool** — Q478
- **Amazon DocumentDB** (MongoDB-compatible)
- **Amazon QLDB** (quantum ledger database)
- **AWS CodeArtifact** (artifact management)
- **AWS App Runner** (automated container app deployment)
- **AWS EC2 Image Builder** (automate AMI creation)
- **AWS Infrastructure Composer** (formerly Application Composer)
- **AWS Device Farm** (mobile/web app testing)
- **AWS Elastic Disaster Recovery (DRS)** (CloudEndure replacement)
- **AWS Network Firewall** (VPC-level firewall)
- **Amazon AppStream 2.0** — Q152, Q64
- **Amazon WorkDocs** (collaborative document service)
- **AWS DataExchange** (third-party data marketplace)
- **AWS Lake Formation** (data lake setup)
- **AWS Cost and Usage Report** — covered in billing comparisons
- **AWS Transit Gateway** — Q70, Q443, Q445, Q653

## High-Priority Weak Areas to Review

1. **CAF Perspectives and capabilities** — many questions test specific perspectives and capabilities (Business, People, Governance, Platform, Security, Operations).
2. **Well-Architected Framework pillars** — know all 6 pillars and specific design principles per pillar.
3. **EC2 Purchasing Options** — critical to distinguish between On-Demand, Reserved, Spot, Savings Plans, Dedicated Hosts for various scenarios.
4. **Shared Responsibility Model** — know exact boundaries for EC2, RDS, Lambda, DynamoDB, S3.
5. **Migration Strategies (7Rs)** — rehost vs. replatform vs. refactor scenarios.
6. **Storage comparison** — EBS vs. EFS vs. FSx vs. S3 vs. Storage Gateway.
7. **Security services** — GuardDuty vs. Inspector vs. Macie vs. Shield vs. WAF.
8. **Networking** — Security Groups vs. NACLs, VPC Endpoints vs. PrivateLink, Direct Connect vs. VPN.
9. **Cost tools** — Pricing Calculator vs. Cost Explorer vs. Budgets vs. CUR.
10. **Support plans** — TAM, concierge, Trusted Advisor access levels.

---

*This revision guide covers all 720 questions from the exam dump, all AWS services from the course notes (Stéphane Maarek's CLF-C02 material), and all high-yield topics from the exam question patterns. Review Parts 3, 4, and 6 immediately before the exam for maximum retention.*