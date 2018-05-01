# Security Token Service (STS)

#### Understanding Key Terms

- **Federation:** Combining or joining a list of users in one domain (such as IAM) with a list
  of users in another domain (such as Active Directory, Facebook, etc)

- **Identity Broker:** A service that allows you to take an identity from point
  A and join it (federate it) to point B.

- **Identity Store:** Services like Active Directory, Facebook, Google, etc.

- **Identities:** A user of a service like Facebook, etc.

#### Scenario

- You are hosting a company website on some EC2 web servers in your VPC. Users
  of the website must log in to the site which then authenticates against the
  companies active directory servers which are based on site at the companies
  head quarters. Your VPC is connected to your company HQ via a secure IPSEC
  VPN. Once logged in the user can only have access to their own S3 bucket. How
  do you set this up?
