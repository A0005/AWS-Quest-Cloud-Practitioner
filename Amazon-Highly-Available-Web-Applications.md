1 - Amazon EC2 Auto Scaling Groups:

    By placing your web servers in an Amazon EC2 Auto Scaling group behind
    a load balancer, you can achieve high availability for your application.
    
    Minimum and maximum capacity define boundaries for the number of instances
    allowed in the Auto Scaling group. The desired capacity is the initial capacity
    of the Auto Scaling group and the capacity it attempts to maintain. This auto
    scaling group can currently contain only one instance.
    
    An Auto Scaling group starts by launching enough instances to meet
    its desired capacity. It maintains this number of instances by 
    performing periodic health checks on the instances in the group.
    
    You must specify at least one Availability Zone when you are creating 
    your Auto Scaling group. An Auto Scaling group can be configured across
    multiple Availability Zones for increased availability.
    
    You define which subnets, from one or more Availability Zones, are linked
    to the Auto Scaling group. This defines where your Amazon EC2 resources 
    linked ti the Auto Scaling group can reside.
    
    Attaching a load balancer to your Auto Scaling group registers the group
    with the load balancer, which acts as a single point of contact for all
    incoming web traffic to your Auto Scaling group.
    
    For managing web-based applications requiring HTTPS connectivity, choose
    the Application Load Balancer. If the web applications are for public access,
    the load balancer must be internet-facing.
    
    A load balancer takes request from clients and distributes them across
    target in a target group. After you enable an Availability Zone, the load
    balancer starts routing request to the registered targets in the Availability Zone.
    
    To customize the traffic flow between the ALB and the web servers you can create
    new security groups that define what traffic is allowed to the load balancer
    and what traffic is allowed to the web servers behind the load balancer.
    
    Security groups are assigned to a VPC. This means the security group can only
    be assigned to resources within the VPC.
    
    For a public-facing load balancer, you specify 0.0.0.0/0 as source to
    accept traffic from any address. By specifying a security group as an
    outbound destination, you can restrict traffic to only be sent to instances
    associated with the specified security group.
    
    Scurity groups are not active unless they are assigned a resource.
    
    To increase security, you can edit the security group in use by Amazon EC2
    instances behind the load balancer to only allow inbound traffic from the
    Application Load Balancer (ALB).
    
    By removing the 0.0.0.0/0 source and replacing it with a security group,
    you can easily control which reources are allowed to send traffic to 
    instances without having to inout address ranges. Only traffic from the 
    instances associated with the securtiy group is allowed.
    
    Custom security groups are only active after you assign them to an instance.
    You can assign multiple security groups to an instance.
    
    
    The security groups you associate with your load balancer determine your rules
    for controlling where traffic can come from and where it is allowed to be sent
    
    To test access to your application through the load balancer, you can copy the 
    DNS name into a browser window.
    
    Use the DNS name to get quick feedback and view your application. If you 
    don't see your application, be sure to check the rules in the security 
    group that you aassociated to the load balancer.
    
    The default ALB health check only validates the root path of an HTTP
    server. Applications will generally implement a much more robust application 
    health check to validate server configuration and external access.
    You can manually verify that health checks are active on your load balancer.
    
    You can modify load balancer health check settings to match your performance requirements.
    
    After your target is registered, it must pass one health check to be considered healthy.
    After each health check is completed, the load balancer node closes the connection that
    was established for the health check.
    
    The default settings allow 150 seconds to pass (30 second intervals * 5
    unhealthy checks) before marking an instance unhealthy. The new values will 
    cause unhealthy instances to be marked unhealthy after 10 seconds (2 failed
    checks, 5 seconds apart).
    
    After you have created an internet-facing load balancer, you can now 
    run your applications in a private subnet. You can add or remove subnets
    associated with the Auto Scaling group.
    
    If you add or remove a subnet you are defining where the Auto Scaling group
    resources can reside.
    
    Changing the subnet will not automatically cause instances to rebuild in the 
    Auto Scaling group. Terminating the instance reduces the number of instances
    below the minimum for the Auto Scaling group and triggers a new instance launch
    in the private subnet.
    
    If you terminate an instance within an Auto Scaling group which results in 
    lowering the number of running instances below the Auto Scaling minimum
    requirement, then a new instance will be launched automatically.
    
    You can review Auto Scaling group operations in Activity history.
    
    Eeach item in Activity history lists an Auto Scaling action and the cause
    of the action.
    
    Make sure to get verification that your new instances are running and considered 
    healthy by the load balancer.
    
    To take advantage of the safety and reliability of geographic redundancy,
    span your Auto Scaling group across multiple Availability Zones within a Region.
    Attach a load balancer to distribute incoming traffic across those Availability Zones.
    
    When one Availability Zone becomes unhealthy or unavailable, Amazon EC2
    Auto Scaling launches new instances in an unaffected Availability Zone.
    Auto Scaling attempts to launch new instances in the Availability Zone
    with the fewest instances.
    
    The desired capacity is the initial capacity of the Auto Scaling group
    after this operation completes and the capacity it attempts to maintain.
    Desired capacity is what Auto Scaling changes based on instance performance
    or other alarm-based actions that you configure.
    
    By changing desired capacity manually, you can test your Auto Scaling group
    behavior. Increasing the desired capacity, while not exceeding the maximum
    capacity, will launch new instances to meet the desired capacity vaule.
    
    You can review Activity history to verfiy yout expected results.
    
    Connection draining enables the load balancer to complete in-flight requests
    made to instances that are de-reregistering or unhealthy before stopping traffic 
    flow from the load balancer.
    
    When Auto Scaling launches a new instance, you can verify the subnet ID 
    to ensure that your instance was deployed to the correct subnet.
    
    After an instance has been deployed to a new subnet, you can check on the
    health of the new instance.
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
