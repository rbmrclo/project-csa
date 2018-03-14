# EC2 Key Pairs

- EC2 key pairs are two cryptographically secure keys that are used by AWS to
  authenticate a client when logging into an EC2 instance.
- Each key pair consists of a public key and a private key.
- AWS stores the public key on the instance, and you are responsible for storing
  the private key.

To login into an EC2 instance, you must create and authenticate with a key pair.

- Linux instances have no password, and you use a key pair to log in (using SSH)
- With Windows instances, you use a key pair to obtain the administrator
  password and then log in using RDP (remote desktop protocol)
- During the creation process of an EC2 instance, you are required to either
  create a new key pair OR use an existing ky pair - which will be tied to the
  instance.
- The private key is available for download and stored on your local device,
  however it is only available once (in the form of a `.pem` file).

For SSH login to linux instances:

- You will most likely need to change permissions on the `.pem` file before you
  can use it to login via SSH.
- This is done by running the following command:

```
$ chmod 400 <key_name>.pem
```
