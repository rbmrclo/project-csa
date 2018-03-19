# CloudWatch EC2 Monitoring

#### System Status Checks (things that are outside of our control)

- Loss of network connectivity
- Loss of system power
- Software issues on the physical host
- Hardware issues on the physical host
- **How to solve**: Generally stopping and restarting the instance will fix the
  issue. This causes the instance to launch on a different physical hardware device.

#### Instance Status Checks (software issues that we do control)

- Failed system status checks
- Misconfigured networking or startup configuration
- Exhausted memory
- Corrupted file system
- Incompatible kernel
- **How to solve**: Generally a reboot, or solving the file system configuration issue.

By default, CloudWatch will automatically monitor metrics that can be viewed at
the host level (NOT the software level), such as:

- CPUUtilization
- CPUCreditBalance
- CPUCreditUsage
- Network in/out

OS level metrics that required a third party script (perl) to be installed (provided by AWS)

- Memory utilization, memory used, and memory available
- Disk swap utilization
- Disk space utilization, disk space used, disk space available
