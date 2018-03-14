# Virtualization

- Virtualization is the process of creating a "virtual" version of something
  rather than the actual version of that thing.
- In AWS EC2, virtualization refers to using a "portion" of a server's computing
  power and storage to setup and run an operating system.
- Virtualization for EC2 is run using the Xen Hypervisor Software.
- The maintenance of the physical AWS server and the Xen Hypervisor is handled by AWS.

## Linux AMI Virtualization Types

#### `HVM AMIs (Hardware Virtual Machine)`

- This virtualization type provides the ability to run an operating system
  directly on top of a virtual machine without any modification, as if it were
  run on the bare-metal hardware.
- The Amazon EC2 host system emulates some or all of the underlying hardware
  that is presented to the guest.
- Unlike PV guests, HVM guests can take advantage of hardware extensions that
  provide fast access to the underlying hardware on the host system.

#### `PV AMIs (Paravirtual)`

- Guests can run on host hardware that does not have explicit support for
  virtualization, but they cannot take advantage of special hardware extensions
  such as enhanced networking or GPU processing.
- Historically, PV guests had better performance than HVM guests in many cases,
  but because of enhancements in HVM virtualization and the availability of PV
  drivers for HVM AMIs, this is no longer true.

