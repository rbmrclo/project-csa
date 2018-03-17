# Lifecycle Policies

An object lifecycle policy is a set of rules that automate the migration of an
object's storage class to a different storage class (or deletion), based on
specified time intervals.

- By default, lifecycle policies are disable on a bucket/object.
- Are customizable to meet your company's data retenion policies.
- Great for automating the management of object storage and to be more cost efficient.
- Can be used with versioning to create a great archiving and backup solution in S3.

##### Example:

1) I have a work file that I am going to access every day for the next 30 days
2) After 30 days, I may only need to access that file once a week for the 60 next days.
3) After which (90 days total) I will probably never access the file again but want to keep it just in case.

