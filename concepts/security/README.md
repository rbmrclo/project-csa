# Security

#### 4 Areas of Security

- Data protection
- Privilege Management
- Infrastructure Protection
- Detective Controls

#### Best Practices - Data Protection

- AWS customers maintain full control over their data.
- AWS makes it easier for you to encrypt your data and manage keys, including
  regular key rotation, which can be easily automated natively by AWS or
  maintained by a customer.
- Detailed logging is available that contains important content, such as file
  access and changes.
- AWS has designed storage systems for exceptional resiliency.

##### Questions

- How are you encrypting and protecting your data at rest?
- How are you encrypting and protecting your data in transit? (SSL)

#### Best Practices - Privilege Management

- Access Control Lists (ACLs)
- Role Based Access Controls
- Password Management (such as password rotation policies)

##### Questions

- How are you protecting access to and use of the AWS root account credentials?
- How are you defining roles and responsibilities of system users to control
  human access to the AWS Management Console and APIs?
- How are you limiting automated access (such as from applications, scripts, or
  third-party tools or services) to AWS resources?
- How are you managing keys and credentials?

#### Best Practices - Infrastructure Protection

- Outside of Cloud, this is how you protect your data centre. RFID controls,
  security, lockable cabinets, CCTV etc. Within AWS they handle this, so really
  infrastructure protection exists at a VPC level.

##### Questions

- How are you enforcing network and host-level boundary protection?
- How are you enforcing AWS service level protection?
- How are you protecting the integrity of the operating systems on your Amazon
  EC2 instances?

#### Best Practices - Detective Controls

- You can use detective controls to detect or identify a security breach. AWS
  services to achieve this include:
  - CloudTrail
  - CloudWatch
  - AWS Config
  - S3
  - Glacier

##### Questions

- How are you capturing and analyzing AWS logs?

#### Key AWS Services

##### Data Protection

- You can encrypt your data both in transit and at rest using; ELB, EBS, S3
  & RDS

##### Privilege Management

- IAM
- MFA

##### Infrastructure Protection

- VPC

##### Detective Controls

- CloudTrail
- Config
- CloudWatch
