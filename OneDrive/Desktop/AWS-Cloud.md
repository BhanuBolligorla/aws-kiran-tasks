# AWS Infrastructure – Detailed Explanation

## What is Infrastructure (Infra)?

Infrastructure is everything needed to run applications and services.

It includes:

* Physical servers (computers)

* Storage (hard disks)

* Network (routers, cables)

* Data centers

Traditional Infrastructure :
--

* Companies buy servers

* Maintain data centers

* Handle power, cooling, hardware failures.

### AWS Infrastructure

* AWS owns and manages all hardware

* Users rent resources over the internet

* No need to worry about maintenance

Note : Infrastructure is the foundation on which applications run.

## What is an AWS Region?

An AWS Region is a geographical area where AWS operates.

Examples:

* ap-south-1 – Mumbai

* us-east-1 – North Virginia

* eu-west-1 – Ireland

### Why AWS Uses Regions

* Reduce delay (latency)

* Follow government and legal rules

* Protect from large-scale failures

Each region is:

* Physically separate

* Completely independent

 If one region goes down, other regions are not affected.

## What is an Availability Zone (AZ)?

An Availability Zone (AZ) is a data center inside a region.

Each region has 2 or more AZs

* AZs are far enough apart to avoid common failures

* AZs are connected using fast private networks

Example :

Mumbai Region (ap-south-1)
- AZ A
- AZ B
- AZ C


Why AZs Are Important

High availability

Fault tolerance

Disaster recovery

 Best practice: Run applications in multiple AZs.

### Difference Between Region and AZ :

| Region                         | Availability Zone           |
| ------------------------------ | --------------------------- |
| Large geographic area          | Data center inside a region |
| Independent from other regions | Connected to other AZs      |
| Used for global availability   | Used for high availability  |

## What is Virtualization?

Virtualization is a technology that allows one physical server to act like many servers.

### Without Virtualization

- One server runs one OS

- Hardware is underused

- Expensive and slow to scale

### With Virtualization

- One server runs multiple virtual machines (VMs)

- Each VM has its own OS

- Resources are shared efficiently

- Benefits of Virtualization

- Saves cost

- Better performance

- Faster server creation

- Easy scaling

AWS uses virtualization to provide services like EC2.

##  How Virtualization Works (Step by Step)

- A physical server is installed in a data center

- A hypervisor is installed on the server

- The hypervisor divides hardware into virtual machines

- Each VM runs its own operating system

- Applications run inside these VMs

-  Multiple users safely share the same physical machine.

## What is a Hypervisor?

A Hypervisor is the software that controls virtualization.

It:

- Runs on physical hardware

- Creates and manages virtual machines

- Allocates CPU, memory, and storage

- Ensures isolation between VMs

 Hypervisor is the brain behind virtualization.

## Types of Hypervisors
### Type 1 (Bare Metal Hypervisor)

- Runs directly on hardware

- Faster and more secure

- Used in data centers

Example:

- AWS Nitro Hypervisor

### Type 2 (Hosted Hypervisor)

- Runs on top of an OS

- Used for personal systems

Example:

- VirtualBox, VMware Workstation

- AWS uses Type 1 hypervisors.

## How Hypervisor Works (Simple Flow)

- Physical server starts

- Hypervisor loads

- Hypervisor creates virtual machines

- Resources are shared safely

- VMs run independently

 If one VM fails, others continue running.

##  How Everything Connects Together

- AWS has global regions

- Regions contain multiple AZs

- AZs contain data centers

- Data centers have physical servers

- Servers run hypervisors

- Hypervisors create virtual machines

- Applications run on virtual machines

