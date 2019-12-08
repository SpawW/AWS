Second Scenario
- Write an AWS CloudFormation (  ) template that creates a VPC in an AWS region.
Requirements :
  - The template must be able to bring up the necessary infrastructure in the Ireland region without any modifications to the former;
  - The CIDR Block range available is on the 10.0.0.0/8 network and the VPC must have at least 3000 available IPs equally divided between public and private subnets.
    - Due to address space limitations, the least possible number of IPs must be segmented;
  - Instances in the private subnets must:
    - be able to successfully use ping and traceroute to addresses outside of the VPC;
    - be able to connect to HTTP/HTTPS services outside of the VPC;
    - only accept SSH connections from the VPC address range;
    - block all other traffic.
  - Instances in the public subnets must:
    - permit all traffic, except SSH; SSH must only be possible from the VPC address range;
    - Public traffic from private subnets must be NATed.