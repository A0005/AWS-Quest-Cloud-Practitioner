1 - Amazon EFS:

    Amazon EFS provides a simple, serverless, set-and-forget, elastic file
    system that lets you share file data without provisioning or managing
    storage.
    
    With Amazon EFS, you can grow and shrink your file systems automatically 
    as you add and remove files, eliminating the need to provision and 
    manage capabilities to accommodate growth.
    
    Amazon EFS creates a shared storage file system available 
    concurrently to multiple instances.
    
    After creating the Amazon EFS file system, you create mount targets on each
    subnet. The mount target enables communication from instances on the subnet.
    Amazon EFS uses the Network File System (NFSv4) protocol. Instances that 
    connect to the file system are NFS clients.
    
    When you create an Amazon EFS mount target, you must attach a security 
    group. The security group determines which instances can access the file
    system as NFS clients.
    
    Amazon EFS file systems require an inbound NFS rule. By selecting a security
    group as the incoming source, any instances linked to the security group
    you select will have NFS client access to the file system.
    
    After the Amazon EFS security group has been created, you are prepared 
    to create the file system.
    
    Amazon EFS is built to scale on demand up to petabytes of storage capacity 
    without disruption applications.
    
    To create Amazon EFS resources such as a file system and access points,
    a user must have AWS Identity and Access Management (IAM) permissions
    for the corresponding API action and resource.
    
    Amazon EFS offers you the choice of creating file systems using Standard 
    or One Zone storage classes. Standard storage classes store data within
    and across multiple availability zones (AZ). One Zone storage classes 
    store data redundantly within a single AZ, at a 47% lower price than
    Standard, for workloads that don't require multi-Az resilience.
    
    You can disable automatic backups and lifecycle management to
    reduce costs until you are in production.
    
    For simplicity during testing, you can start with a single mount target in a 
    single availability zone.
    
    By attaching your custom security group to the mount target, you control
    where the source of incoming traffic to the file system can originate.
    
    After the new file system is available, you can use automatically created commands
    to mount the file system.
    
    The Amazon EFS client (amazon-efs-utils) is an open source collection of Amazon EFS tools.
    This package is available in the Amazon Linux package repositories, and you can build
    and install the package on other Linux distributions.
    
    The Amazon EFS client includes a mount helper and tooling that makes it easier
    to perform encryption of data in transit for Amazon EFS file systems.
    
    Once you have copied the mount command, you can connect to your Amazon EC2 instance
    and mount the file system.
    
    Amazon EC2 supports SSH, Systems Manager Session Manager, or Amazon EC2
    Connect to connect to an instance. Amazon EC2 Instance Connect provides
    a simple and secure way to connect to your Linux instances using Secure
    Shell (SSH). With EC2 Instance Connect, you use AWS Identity and Access
    Management (IAM) policies and principals to control SSH access to your
    instances, removing the need to share and manage SSH keys. All connection
    requests using Amazon EC2 Instance Connect are logged to AWS CloudTrail
    so that you can audit connection request.
    
    Amazon EC2 Connect requires that the EC2 instance security group allows incoming
    SSh traffic over port 22.
    
    The Amazon EFS client is available in the Amazon Linux packge repositories.
    You can build and install the package on other Linux repositories. Installing
    the utilities makes the mount commands easier to process and troubleshoot.
    
    After you create a new directory, you can paste the mount command you copied 
    from Amazon EFS. Note that the sudo mount command lists the directory to 
    mount as efs by default. You need to change efs to your directory name
    before hitting enter. After mounting, you can use the cat command to create,
    view, and append to a text file.
    
    After successfully mounting the new file system, you are ready to add more mount
    points for other subnets in other availability zones within the same VPC.
    
    You can mount a file system on compute instances, including Amazon EC2, Amazon ECS,
    Amazon ECS, and AWS Lambda in your Virtual Private Cloud (VPC).
    
    The Network tab allows you to display and manage your mount targets.
    
    For Amazon EFS file systems that use Standard storage classes, you can create
    a mount target in each Availability Zone in an AWS Region.
    
    You can create mount targets for a file system using the AWS Management 
    Console, AWS CLI. or programmatically using the AWS SDKs. When using the
    console, you can create mount targets when you first create a file system
    or after the file system is created.
    
    In most cases, you will assign the same security group to each mount target.
    
    Each mount target installs and elastic network interface (ENI) into the chosen subnet.
    An elastic network interface is a logical networking component in a VPC that represents 
    a virtual network card. The ENI auotmatically receives an IP address from the VPC.
    
    After adding an additional mount target, you can mount the file system on instances
    in the specified subnet.
    
    
2 - Security Groups:

    Security groups are linked to a single VPC. You can assign a security 
    group to one or more instances, but each instance must be in the same
    VPC as the security group.
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
