# CloudHSM

- HSM (Hardware Security Module) is a dedicated physical machine/appliance
  isolated in order to store security keys and other types of encryption keys
  used within an application.
- The key is used within the domain of the HSM appliance instead of being
  exposed outside the appliance.
- HSM Appliances have special security mechanisms to make them more secure:
  - The security key is only used within the HSM
  - An HSM client is used to expose the APIs of the HSM
  - So an application can communicate with HSM to do the encryption (or
    decryption) of the data that we are requesting.
  - The appliance is physically isolated from other resources.
  - Tamper resistant (build to notify via advanced logging)
  - On AWS, even though they are hosting the applicance, AWS engineers have no
    access to the keys (only to manage and update the appliance).
  - If the keys are lost or reset (to access the appliance), you will never be
    able to access the data stored on the appliance.

- Some types of keys that might be stored on HSMs:
  - Keys used to encrypt file systems
  - Keys used to encrypt databases
  - Keys used to provide DRM
  - Used with S3 encryption

- When to use CloudHSM instead of something like Key Management Service?
  - Generally, compliance requiremens require it or internal security policy
    require it.
  - Not even AWS engineers have access to the keys on the CloudHSM appliance,
    only access to "manage" the appliance.
