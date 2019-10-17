# snippets

Random Snippets of code and configuration for various tasks, projects, and testing.


# CloudCustodian
* EC2 Tagging Compliance - Containts various policies for the following tasks
  * Mark instaces with key:value that indicates acceptable use for CloudCustodian I.E. Custodian:true (Set to RunInstance)
  * Check for compliance on specific tag(s) - If not compliant mark for op - I.E. Stop after 3 days (Set to state:running)
  * Check for remediation of tag(s) - See if tag(s) exist yet - If they do, untag mark (Set to 30 minutes rate)
  * Check marked op tag (default maid_status) - If gte current date, perform op. I.E. Stop. (Set to 1 hour rate)
  * Check EBS Snapshots and propogate tags from parent EBS volume
  * Contains .json policy document to perform the above actions


# TerraForm



# AWS

