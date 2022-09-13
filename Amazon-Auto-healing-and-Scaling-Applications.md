1 - AWS Auto Scaling:

    AWS Auto Scaling monitors your applications and automatically adjusts capacity
    to maintain steady, predictable performance at the lowest possible cost.
    
    AWS Auto Scaling is free to use, and allows you to optimize the costs of
    your AWS environment.
    
    AWS Auto Scaling can help you optimize your utilization and cost efficiencies
    when consuming AWS services so you only pay for the resources you actually
    need. When demand drops, AWS Auto Scaling will automatically remove any excess 
    resource capacity so you avoid overspending.
    
    AWS Auto Scaling continually mmonitors your applications to make sure that
    they are operating at your desired performance levels. Using AWS Auto Scaling,
    you maintain optimal application performance and availability, even when workloads
    are periodic, unpredictable, or continuously changing.
    
    It's important to test your build steps whenever possible. Identify potential
    issues as soon as possible during your build.
    
    AWS Auto Scaling lets you build scaling plans that automate how groups
    of different resources respond to changes in demand. You can optimize for 
    balance between availability and costs. AWS Auto Scaling automatically 
    creates all of the scaling policies and sets targets for you based on your
    preference.
    
    Notice the properties that were previously specified in the launch template
    default for the Auto scaling group. Information such as Instance Type has 
    already been selected for you.
    
    If you host an application on mutiple Amazon EC2 instances, you can launch instances
    across multiple instance types and purchase options (Spot and On-Demand Instances)
    by choosing Combine purchase options and instance types. This is an advanced feature
    in which your team can optimize costs using different deployment strategies.
    
    Amazon EC2 Auto Scaling can determine the health status of an instance using
    one or more of the following. First is the status checks provided by Amazon
    Ec2 to identify hardware and software issues that may impair an instance.
    The second is health checks provided by a load balancer. These can include custom
    health checks.
    
    With target tracking scaling policies, you select a scaling metric (e.g., CPU
    Utilization) and set a target vaule. Amazon EC2 Auto Scaling creates and manages the 
    Amazon CloudWatch alarms that trigger the scaling policy and calculates the scaling
    adjustment based on the metric and the target vaule.
    
    You can be notified when Amazon EC2 Auto Scaling is launching or terminating
    the Amazon EC2 instances in your Auto Scaling group. You manage notifications using Amazon
    Simple Notification Service (Amazon SNS).
    
    After you create a scaling policy, Amazon EC2 Auto Scaling starts evaluation 
    the policy against the metrics you selected.
    
    You can see the history of your scaling group. If additional conditions are
    added to your scaling group you can view which condition group you can
    view which condition has caused the system to scale.
    
    Scheduled scaling helps you to set up your own scaling schedule according
    to predicatable load changes. For example, let's say that every week the
    traffic to your web application starts to increase based on a predictable
    factor, you can configure your system to preempt this event.
    
    By default, the times that you set are in Coordinated Universal Time (UTC).
    When specifying a recurring schedule with a cron expression using the AWS
    CLI or an SDK, you can change the time zone to correspond to your local time
    zone or a time zone from another part of your network.
    
    
2 - Amazon Machine Image:
    
    You can capture the contents of an instance and its volume into an Amazon
    Machine Image (AMI). An AMI is a template used for launching new instances 
    with identical configurations.
    
    By default, Amazon EC2 shuts down the instance, takes snapshots of any attached volumes,
    creates and registers the AMI, and then reboots the instance. You can enable the No reboot 
    option, if you don't want your instance to be shut down.
    
    After you create an AMI, it is only available, by default, within the region
    of creation. To use the same AMI in another region, you must copy the AMI
    to the other region.
    
3 - Launch Templates:

    Launch templates enable you to store launch paramenters so that you do not
    have to specify them every time you launch an instance. For example, a launch
    template can contain the AMI ID, instance type, and network settings that
    you typically use to launch instances.
    
    You are limited to creating 5,000 launch templates per Region and 10,000
    versions per launch template.
    
    For each launch template, you can create one or more numbered
    launch template versions. The first version specifies the instance 
    type, AMI ID, subnet, and key pair to use to launch the instance.
    
    If you plan to access your Amazon EC2 instance through Windows or the PuTTY
    program then you will use a .ppk file. If you are using a unix-based (e.g Linux,
    MacOS) shell with OpenSSH then select the .pem format.
    
    For Resource tags, specify tags by providing key and vaule combinations.
    You can tag the instance, the volumes, Spot Instance request, you can specify 
    up to two network interfaces for the instance.
    
    This launch template can be used to configure Auto Scaling and healing
    properties of your system. When a server goes down this will be the 
    information that is used to create a new instance.
    
  
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
