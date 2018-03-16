# ELB Troubleshooting

##### Load balancing is not occurring between instances in multiple availability zones

- Make sure "Enable Cross-Zone load balancing" has been selected.

##### Instances are healthy but are not registering as healthy with the ELB

- Check configuration for the "health check" to make sure you have selected the
  proper ping protocol, ping port, and ping health.

##### The ELB is configured to listen on port 80, but traffic is not making it to the instances that belong to the ELB

- You may have mistaken the "Listeners" for the security group. Listeners are
  not the same as security group rules, port 80 still needs to be open on the
  security group that the ELB is using.

##### Access logs on web servers shows IP address of the ELB not the source traffic

- Enable Access Logs to Amazon S3 (found under "attributes")

##### Unable to add instances from a specific subnet to the ELB

- Most likely the subnet that the instance lives in has not been added to the
  ELBs configuration.
