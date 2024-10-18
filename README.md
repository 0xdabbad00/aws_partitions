# AWS Partitions
AWS partitions are distinct clouds that are more isolated than the region concept.  Although most only interact with the Standard partition (`aws`), and may be aware of the GovCloud and China paritions, there are even more.  Many will only slightly notice the relavant partitions when seeing ARNs, such as `arn:aws:s3:::amzn-s3-demo-bucket`, which indicate the partition associated with a resource in the second element (`aws` in this example).

Much of the information for partitions comes from SDK [endpoints.json](https://github.com/boto/botocore/blob/develop/botocore/data/endpoints.json) and [partitions.json](https://github.com/boto/botocore/blob/develop/botocore/data/partitions.json).  Some hints of upcoming partitions are seen in regex updates for matching ARNs in the SDK, or the [ip-ranges.json](https://ip-ranges.amazonaws.com/ip-ranges.json) file.

# aws: Standard.
DNS: amazonaws.com

# aws-cn: China.
DNS: amazonaws.com.cn

# aws-us-gov: GovCloud
DNS: amazonaws.com (the same as Standard)

# aws-iso
DNS: c2s.ic.gov

# aws-iso-b
DNS: sc2s.sgov.gov

# aws-iso-e
DNS: cloud.adc-e.uk

# aws-iso-f
DNS: csp.hci.ic.gov 
csp = commercial service provider
hci = hybrid compute initiative
ic = intelligence community
https://fedscoop.com/hybrid-compute-initiative-intelligence-nsa/


# European sovereign
(possibly this is aws-iso-e?)
https://aws.amazon.com/blogs/security/aws-digital-sovereignty-pledge-announcing-a-new-independent-sovereign-cloud-in-europe/
One region is named eusc-de-east-1

# Australia top secret
https://www.abc.net.au/news/2024-07-04/amazon-contract-top-secret-australian-military-intelligence/104057196
