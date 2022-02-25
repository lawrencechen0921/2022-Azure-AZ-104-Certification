# AZ-104 Microsoft Azure Administrator Certification


az-104, az-204, devops engineer expert.

40 - 60 questions in 120 minutes, A score of 700

### 題型

有多選，單選，拖拉，指令， template 選填
後面有 Yes, NO 不能再回去點擊了，還有情境題，時間很短
多做 lab


- [x] Azure Administration (43:13) 11/9
- [X] Governance and Compliance (1:44:50) 11/21
- [x] Identity (3:34:36) 11/21
- [x] Role-Based Access Control (1:21:39) 11/21 21:00
- [x] Azure Storage (3:14:28) 11/21 21:00
- [x] Virtual Networking (4:25:18) (vvv) 11/14
- [x] Intersite Connectivity (1:57:11) (vvv) 11/14
- [x] Azure Virtual Machines (5:19:17) (vvv) 11/15
- [x] Network Traffic Management (1:29:51) (vvv) 11/14
- [x] Web Apps and Containers (4:37:51) 11/16
- [x] Monitoring (47:40) 11/22 
- [x] Backup and Recovery (1:31:38) 11/22 
- [x] Wrap-Up and Practice (3:48:33) 11/22
- [x] 11/24 總複習加上考古題
- [ ] 這週做實驗考古題再深入
- [ ] Failed on 628
- [ ] 下週五考 12/17 



- Storage have multiple services
- Storage fundamentals
- Azure Blob storage
- Azure Data Lake Storage
- Azure Files
- Azure Files sync
- Queue Storage
- Table Storage
- Azure Disks





## Manage Azure Identities and governance (15-20%)

**Manage Azure Active Directory (Azure AD) objects**

* create users and groups (v)
* create administrative units(v)
* manage user and group properties (v)
* manage device settings (v)
* perform built user updates (v)
* manage guest accounts (v)
* configure Azure AD join (v)
* configure self-service password reset (SSPR v)

**Manage role-based access control(RBAC)**

* create a custom role (v)
* provide access to Azure resources by assigning roles at different scopes (v)
* interpret access assignments (v)

**Manage subscriptions and governance**

* configure Azure policies (v)
* configure resource locks (v)
* apply and manage tags on resources (v)
* manage resource groups (v)
* manage subscriptions (v)
* manage costs (v)
* configure management groups (v)

## Implement and manage storage (15-20%)

**Secure storage**

* configure network access to storage accounts (v)
* create and configure storage accounts (v)
* generate shared access signature (SAS) tokens (v)
* manage access keys (v)
* configure Azure AD authentication for a storage account (v)
* configure access to Azure Files (v)

**Manage storage** (v)

* export from Azure job
* import into Azure job
* install and use Azure Storage Explorer
* copy data by using AZCopy
* implement Azure Storage replication
* configure blob object replication



**Configure Azure files and Azure Blob Storage** (v)

* create an Azure file share
* create and configure Azure File Sync service
* configure storage tiers (v)
* configure blob lifecycle management (v)

## Deploy and manage Azure compute resources(20-25%)

**Automate deployment of virtual machines (VMs) using Azure Resource Manager templates** (v)

* modify an Azure Resource Manager template
* configure a virtual hard disk (VHD) template
* deploy from a template
* save a deployment as an Azure Resource Manager template
* deploy virtual machine extensions

**Configure VMs** (v)

* configure Azure Disk Encryption
* move VMs from one resource group to another
* manage VM sizes
* add data disks
* configure networking
* redeploy VMs
* configure high availability
* deploy and configure virtual machine scale sets(new)


**Create and configure containers** (v)

* configure sizing and scaling for Azure Container Instances
* configure container groups for Azure Container Instances
* configure storage for Azure Kubernetes Service (AKS)
* configure scaling for AKS
* configure network connection for AKS
* upgrade an AKS cluster

**Create and configure Azure App Service** (v)

* create an App Service plan
* configure scaling settings in an App Service plan
* create an App service
* secure an App service 
* configure custom domain names
* configure backup for an App Service
* configure networking settings
* configure deployment settings

## Configure and manage virtual networking (25-30%)

**Implement and manage virtual networking** (v)

* create and configure virtual networks, including peering
* configure private and public IP addresses
* configure user-defined network routes
* implement subnets
* configure endpoints on subnet
* configure private endpoints
* configure Azure DNS, including custom DNS settings and private or public DNS zones

**Secure access to virtual networks**

* create security rules (v)
* associate a netwrok security group (NSG) to a subnet or network interface 
* evaluate effective security rules
* implement Azure Firewall
* implement Azure Bastion

**Configure load balancing**
* configure Azure Application Gateway
* configure an internal or public load balancer
* troubleshoot load balancing

**Monitor and troubleshoot virtual networking** (v)

* monitor on-premises connectivity
* configure and use Azure Monitor for Networks
* use Azure Network Watcher 
* troubleshoot external networking
* troubleshoot virtual network connectivity


**Integrate an on-premises network with Azure virtual network** (v)

* create and configure Azure VPN Gateway
* create and configure Azure ExpressRoute
* configure Azure Virtual WAN 
## Monitor and backup Azure Resources (10-15%)

**Monitor resources by using Azure Monitor**(v)

* configure and interpret metrics
* configure Azure Monitor logs
* query and analyze logs
* set up alerts and actions


**Implement backup and recovery**(v)

* create a Recovery Services vault
* create a Backup vault(new)
* create and configure backup policy
* perform backup and restore operartions by using Azure Backup
* perform site-to-site recovery by using Azure Site Recovery
* configure and review backup reports

---

## Understanding RAM

Azure Resource Manager (ARM) is the orchestration layer for managing the azure cloud.

* Access Way:
  * Azure Portal
  * Azure CLI
  * Azure Powershell

You have a trust relationship between Azure AD and Azure Resource Manager.

![](https://i.imgur.com/AJgk9ww.png)

![](https://i.imgur.com/4EeNf4D.png)
 
 
 今天完成 Administration(finished) 跟 virtual machines (11/25 考過)
 
 
* Powershell create resource group method

![](https://i.imgur.com/1A2079i.jpg)


powershell -> $rg = (Get-AzResourceGroup).ResourceGroupName
              $rg (to print it out)
              (也能用 az cli)$ RG = az group list --query [].name -o tsv
              $RG
              
             
             
             
             
powershell 可以煎著 bash 一起用！！

可以在 cloudshell ssh 進入 instance, 只要你的 key 存在 cloudshell 環境裡頭就 okay.


Could use : `Get-AzResource -ResourceType Microsoft.Compute/virtualMachines`


## ARM Template Details

* parameters and variables:
Are used to pass information to the template
* resources:
The resources component is used to define resources in the template
* Outputs: 
The outputs component is used to return output from the execution of the template.

Deploy template 叫做 purchase! ><

redeploy 會發生 dns 的錯誤。解決辦法進去 defaultValue 改他的值即可



![](https://i.imgur.com/4WZDisS.jpg)


## Virtual Networking


![](https://i.imgur.com/xxY3Iu1.jpg)

Network security group can allow and deny!

* Isolated Network


* Private Network Access

* Network Integration

on-premise


### Virtual Network (VNet) Features

* Subnetting
Azure VNet


* Network Gateway
Azure VNet uses gateway subnets to make VPN connections.



### When you create a Virtual Network

* Only add one subnet at one times(but finished VNet create , you could add more subnets as well)
* security have three type

![](https://i.imgur.com/FOdKdTJ.png)


* Public ip will have one network interface as well, so you have to notice the details between two.
* ipconfiguration menu (like elastic ip modified), if we want a static ip we could change it, DHCP server will dynamic help us to do it.

**Key Takeaways**

* Default Connectivity

By default, intra-network traffic and outbound internet traffic is allowed

* Address Restrictions

Use of private addresses using RFC 1918 provide best results. The smallest VNet subnet from /8 to /29 wtf
(10.0.0.0/8 最多), 但 (0.0.0.0/2 可以) 因為有 IP 有分五種等級


* Reserved IPs 
subnet reserved ip like aws , x.x.x.0-3 and x.x.x.255

* DNS and DHCP
Azure-provided DNS or custom DNS. For VNets, DHCP is built-in.

* Network Integration
VNets are built for integration with one another, hybrid connectivity using VPNs and ExpressRoute

* Supported Protocols
VNets support TCP, UDP, and ICMP protocols.

## Deploying Network resources

Public IP have different SKU-

* Basic SKU

Statically or dynamically assignable PIP(public ip) that is accessible by default and requires an NSG to restrict traffic. Does not support a availability zone deployments.

* Standard SKU
Statically assignable PIP that is not accessible by default and requires an NSG to allow traffic. Supports availability zone deployments.


NIC(Network interface card)have to be the same region of Virtual Network.

### 創建 vm 指令

```bash=
az vm create `
--resource-group ( az group list --query [].name -o tsv)`
--name awslc
--image UbuntuLTS `
--admin-username lc`
--generate-ssh-keys `
--nics lc-pro
```
### Routing Virtual Network

Customer rule > BGP > default rule
### Network Security Groups

Could for Subnet and instance.

It was a AWS NACL + SG


Default have a lot of rules (like AllowVnetInBound, AllowAzureLoadBalancer)


這個差異也很大
![](https://i.imgur.com/uKrwCYG.png)

if you want to allow instance have an ability to connect with internet, you have to associate NIC to instance.

Network security group is stateful, if you allow inbound traffic then outbound traffic is allow to return traffic as well.



1. Traffic Filtering

Allow or deny traffic using rules that are defined by properties such as priority, port, protocol, source, destination,and action.

2. Association

NSGs can be associated with subnets or NICs of virtual machines. When associated, they have no affect on traffic.

3. Rules 
Default rules that cannot be deleted and user-defined rules that can be created

4. Follow the Traffic
Evaluate rules by following the traffic. Inbound traffic checks the subnet, then the NIC for NSGs. Outbound traffic checks the NIC, then the subnet for NSGs. Intra-net traffic is affected.



### Azure DNS 

If you wanna map your DNS to the virtual machine, just add record set to it.

![](https://i.imgur.com/kKy2LOe.jpg)

Azure DNS have to different zone interface:

* DNS zones
* Private DNS zones

Add virtual network link, then you could link resource privately.

`Enable auto registrtion`: This setting enables automatic creation of DNS records in this privated DNS zone, for the virtual machines connected to the virtual network.

### Azure Firewall

* Filter traffic with a Platform as a service (Paas) firewall
* Fully qualified domain name (FQDN) support
* NAT rules, Application rules, network rule -> Azure Policy



![](https://i.imgur.com/TyFuvx5.jpg)



#### Feature


1. DNAT and SNAT (Configure outbound/inboud NAT rules for your networks)
2. Network Rules (Configure network (layer 4) rules for what traffic is allowed)
3. Application Rules (configured rules for filter websites visited from your network)
4. Threat intel (malicious ip or domain)
5. Monitoring (integrate with Azure Monitor to capture firewall traffic)


Firewall tier have - SSL termination and intrusion detection/prevention systems.

When you creat a firewall, you have to apply route to private ip of Azure Firewall.

Later if you want to let private ip out of reaching to internet you have to set up public ip of firewall.


![](https://i.imgur.com/ESm9k1j.png)



> Azure firewall need to have `AzureFirewallSubnet` ( and subnet have to /26 or lower)

Have different rules you can apply.


![](https://i.imgur.com/q9Yl4b8.png)




![](https://i.imgur.com/9rA9WYj.png)

Add route to virtual network.


### Using Service Endpoints

Accessing Paas Services (like Azure Storage Account, sub resource: Azure Files, Azure Blob, Tables, and Queue)


![](https://i.imgur.com/zMS43cD.jpg)


![](https://i.imgur.com/9hOVBmr.jpg)

設定好之後可以用 firewall 的 public ip 進入 private VM ip

#### Service Endpoint

* Enabled per subnet 
* Not all service are supported
* Supported services differ per region
* Does not give services a private IP
* Provide source ip as private ip
* Firewall can enhance security (optional)


To get list of service-endpoints resource


`az network service-endpoint list --location southasia`


### Servcie Endpoint policies

create service endpoint policies to allow traffic to specific azure resources from your virtual network over service endpoint.


#### Wrap-Up

*Using service endpoints, you can enable private connectivity to your services.*

* Decreased attack surface
* Enable use of NSG rules
* Enhanced routing
* You can use service tag to route service
* No private IP !!!


### Private Endpoints

Using Azure Private Link, you can connect your services as connected resource in your network with a private ip known as a private endpoint.

Private Endpoint connectivity for:
* Azure services
* Customer/partner services

Provide direct service (sub-resource) mapping.





78 private endpoint 無法在 subnet 介面直接開，要到 private link center 才可以 ＝＝


![](https://i.imgur.com/sxv0QSc.jpg)

![](https://i.imgur.com/qPxcvlp.png)



#### Wrap up

* A private IP for your connected services
* Connectivity to Azure Services
* Connectivity to customer/partner services
* Direct service (sub-resource) mapping



## Intersite Networking

* Configure Azure VNet Peering

Mostly like AWS VPC peering(a little bit different)



![](https://i.imgur.com/fAZMD1g.jpg)
> This means that you have to setup on both sites.

When you're in the Vnet 3 for example, wanting to connect to Vnet 2 you have to set up vnet to connect back to vnet 3 as well.


(It was better than AWS, i mean that)

#### Wrap-Up


* Types of Peering
  * Virtual network peering
  * Global virtual network peering

* Benefits
  * Low-latency, high-bandwidth connections
  * Cross-network communications
  * Data transfer between/across subscriptions,AAD tenants via Azure Roles, and Azure regions.

* Transitivity
  * Peering connection are non-transitive

* Reciprocity
  * Peering connection is non-reciprocal (and it will help you to connect to each other automatically, no worries)


### VPN Gateway
*Need 45 mins to create*

Establishes connectivity between VNets, similar to VNet peering

Components:

* VNet gateway for VPN Gateway
* Gateway subnet
* Public Ip per VNet Gateway
* IPsec tunnel for encryption

It is transitive!

#### Policy Based v.s Routing Based


![](https://i.imgur.com/enRxb88.jpg)

> VPN Gateway could transitive routing 


![](https://i.imgur.com/bsZq1lA.jpg)



![](https://i.imgur.com/sIGBJrf.png)

![](https://i.imgur.com/Jn3cHxZ.jpg)
> Have different price layer

#### Active-Active  v.s Active-Passive


![](https://i.imgur.com/mQE4JUr.jpg)


> If one failed, it will have another stand-by



![](https://i.imgur.com/WGmhHVl.jpg)


#### Demonstration

You have to create local network gateway as well.

![](https://i.imgur.com/NCQS6iF.png)

![](https://i.imgur.com/1Wc1duE.png)

Three type: VNet to VNet or site-to-site or express route.

三種方法差異: 參考此[文章](https://docs.microsoft.com/en-us/azure/vpn-gateway/vpn-gateway-howto-vnet-vnet-resource-manager-portal)

如果要接 Vnet gateway 到 local network gateway 需要加 connection.


When you create a VNet-to-VNet connection, the local network gateway address space is automatically created and populated. If you update the address space for one VNet, the other VNet automatically routes to the updated address space. It's typically faster and easier to create a VNet-to-VNet connection than a Site-to-Site connection. However, the local network gateway is not visible in this configuration.

If you know you want to specify additional address spaces for the local network gateway, or plan to add additional connections later and need to adjust the local network gateway, you should create the configuration using the Site-to-Site steps.
The VNet-to-VNet connection does not include Point-to-Site client pool address space. If you need transitive routing for Point-to-Site clients, then create a Site-to-Site connection between the virtual network gateways, or use VNet peering.

![](https://i.imgur.com/IVTbJPT.jpg)



## ExpressRoute 

Like AWS Direct Connect? NO!

ExpressRoute have :

1. ExpressRoute circuit(through ISP, like AT&T)
2. ExpressRoute connect( Go global)

Just a physical dedicated connection.

![](https://i.imgur.com/CffM9bW.jpg)


All inbound data transfer to Microsoft is free.


![](https://i.imgur.com/x1iZ7Ja.jpg)

* Their have two connection
* If you want a high bandwidth think about ExpressRoute
* It could do private peering as well
* But it do not have encrypted by default 


## Virtual WAN

![](https://i.imgur.com/zOxQvxO.jpg)

![](https://i.imgur.com/YfufgWf.jpg)


![](https://i.imgur.com/LbsnHAX.jpg)


#### Wrap-Up

* Connect networks using hub-spoke architecture
* Basic and Standard SKUs
* Connect S2S and P2S VPN gateways, global reach ExpressRoute, and VNets
* Secure with Azure Firewall and Firewall Manager
* Any-to-Any connectivity
* Connections propagated to managed route
* Managed virtual network


## Network Traffic Management

### Introducing Azure Load Balancer

You can use `help me choose` to determine which combination ypu shoud choose.


![](https://i.imgur.com/rDD8Bes.jpg)


![](https://i.imgur.com/yHlb784.jpg)
> It was like target group of AWS


![](https://i.imgur.com/x5X3Gsu.jpg)


LB

![](https://i.imgur.com/vJ31ubZ.jpg)


The standard SKU would provide HTTPS (layer 7)


Different rules on Azure:
[Rules](https://docs.microsoft.com/en-us/azure/load-balancer/manage-rules-how-to)


### Application Gateway


![](https://i.imgur.com/blSPjb8.jpg)

> Have app services!!!


![](https://i.imgur.com/NiWSyZe.jpg)

Have different tier to choose

![](https://i.imgur.com/VK3MvZc.png)

And also you have autoscaling!!


![](https://i.imgur.com/qND3MUb.png)


![](https://i.imgur.com/nFqbz51.jpg)
> If you want https have to upload your SSL


![](https://i.imgur.com/RuZnIRo.jpg)

> Use session stickness 

![](https://i.imgur.com/EwcZLwj.jpg)
> Connection Drainning

Application Gateway have public ip.


![](https://i.imgur.com/8y4mfa8.jpg)


## Creating Azure VM

Storage - Azure Disk, consisting of OS disk, temporary disk, and data disk.

Instance Family

![](https://i.imgur.com/PBErq5o.png)


![](https://i.imgur.com/LHesSKa.png)


![](https://i.imgur.com/PhnChpe.png)

You can use AAD credential to login Azure as well.

![](https://i.imgur.com/TnILsaP.png)

### Virtual Hard Disks


![](https://i.imgur.com/LJLL9dv.png)

* unmanaged v.s managed 

![](https://i.imgur.com/JPVBRGJ.png)

* Disk Type


![](https://i.imgur.com/P68gldN.png)

> Disk storage performance is limited to specific VM sizes.


* Disk Encryption

![](https://i.imgur.com/bLk0jhU.png)

BitLocker and DM-Crypt


Use key-vault to encrypt

![](https://i.imgur.com/KjrjTL9.png)

### VM Scale Set

Availability set 可以 create!


When you finished created your availability set, you cann't put your VM into it.

> The max platform fault domain count in the selected subscription and location is 2.

### Virtual Machine Scale Sets

Purpose of Virtual Machine Scale Sets

* Simplify scaling configuration
* Save costs by aligning usage with demand
* Scale to meet demand for traffic


![](https://i.imgur.com/YLCM08m.jpg)

![](https://i.imgur.com/Naf984I.png)

![](https://i.imgur.com/Bo8OXD5.png)

* Health Check


![](https://i.imgur.com/AX1qD3V.png)

### Wrap-up

![](https://i.imgur.com/WIW5ERk.png)


### Automating Virtual Machine Deployment


![](https://i.imgur.com/EwDAMUM.jpg)


![](https://i.imgur.com/nlk0frW.jpg)


![](https://i.imgur.com/MBHgmVg.png)


![](https://i.imgur.com/noBdUnx.png)



## Automating VM deployment

Why Automate deployment?

* Patch/Update operating system(OS)
* Pre Install software
* Preconfigure settings

---
Source VM as golden images (AMI)


![](https://i.imgur.com/N37HiHP.png)


`sudo waagent -deprovision+user`





### Managing 
Virtual Machine Update

Update Management-

Manages system updates and patches for workloads both in the `Azure Cloud ` and `on-premises`.


* Support Linux and Windows VMs
* Provide capabilities for:
  * Scheduling
  * Compliance Scanning
  * Reporting





![](https://i.imgur.com/9hrOGan.jpg)


1. 先確認 operating system 是在本地還是雲，接著需要 Automation Account，還需要 Log Analytics Agent 在 OS 裡面，







Find `Guest + host updates` to do update management.



![](https://i.imgur.com/TUUHgQN.jpg)


![](https://i.imgur.com/N3ALtTI.png)

點擊之後的畫面，需要 15 分鐘才能完成。





Compliance-

![](https://i.imgur.com/YrWf3vW.jpg)

![](https://i.imgur.com/sLKONAw.jpg)


Also it support the extension of Microsoft Monitoring Agent!

2023 Aug would be Microsoft Monitor Agent!






### Automation Virtual Machine Configuration（要筆記）

明天自己 demo 一次

![](https://i.imgur.com/CTTrDxW.jpg)

### Azure Bastion

Fully Managed Paas!

![](https://i.imgur.com/bpZugSY.jpg)
> No Public IP

![](https://i.imgur.com/hHqzkXN.png)

要在 private virtual machine 點擊 connect 選擇 Bastion 才有用

做 bastion host lab

![](https://i.imgur.com/MWj8mSY.jpg)


### Create an App Service Plan(要筆記)

App Service Plan


![](https://i.imgur.com/EuVmC6Y.jpg)



![](https://i.imgur.com/qp5mzD2.png)

> Create your fucking plan


Also, you have application insight to monitor performance

![](https://i.imgur.com/UXUoaT2.png)



### Creating Web App


Deployment could use Github Actions

Web application, would have azurewebsites.net



#### Part 2: Deploy your web

$rg = (Get-AzResourceGroup).ResourceGroupName (要定義好你的 rg)

$appname = "xxx"

dotnet new mvc -o demowebapp

> Here you have to change your directory

dotnet publish -o pub

> Here you have to change directory to pub as well (進入到這個 directory 之後才開始 zip)

zip -r site.zip *(allfile)

az webapp deployment source config-zip `
--src ./site.zip `
--resource-group $rg `
--name $appname 


![](https://i.imgur.com/XBUlCFW.jpg)

### Configuring Web App

You can pick up your own.


![](https://i.imgur.com/5ZqL8N7.png)



![](https://i.imgur.com/lgNBsQQ.jpg)


![](https://i.imgur.com/Z9TlXrq.jpg)

Azure Provided TXT record is going to validate our ownership


#### Deploy Slot-

1. Swap Deployment slots
2. Secondary web app



![](https://i.imgur.com/2il0QRe.jpg)



![](https://i.imgur.com/oebaDh5.jpg)

Github, Bitbucket, Local Git, Azure Repos


#### Backup

![](https://i.imgur.com/Uu10l2O.jpg)

Could use this blob to restore web app.


#### Connection string with DB

![](https://i.imgur.com/EHaKN2T.jpg)


#### Identity Provider 

![](https://i.imgur.com/9B3UDWM.png)



![](https://i.imgur.com/NMicd8F.png)


#### Wrap-Up 

![](https://i.imgur.com/jZRLLI5.jpg)

### Describing Containers in Azure

A container is a unit of software. This unit consists of code, it's dependencies, and configurations to be shipped and run anywhere.



![](https://i.imgur.com/f5YIiZW.jpg)


![](https://i.imgur.com/VxLw3sy.png)


Finished Container tmr(明天到 100 題)

xxx.azurecr.io 

then you can use `docker login xxx.azurecr.io --username xxx`


![](https://i.imgur.com/zFCQ342.jpg)

明天做個 lab



### Azure Container Instances (ACI)


![](https://i.imgur.com/0bvJvSo.png)

#### Container Groups


![](https://i.imgur.com/u5AADCA.png)

![](https://i.imgur.com/e9GgsG5.png)

### Container Networking

Could use public and private.


![](https://i.imgur.com/xV2p32U.png)




![](https://i.imgur.com/rwbC18u.jpg)


## AKS

ACI Limitation 有些限制：

* can't automatically scale up 
* Do not have orchestration layer, so you have to do very cumbersome settings.




![](https://i.imgur.com/WrXLIsY.jpg)


![](https://i.imgur.com/bgpUf3V.jpg)


![](https://i.imgur.com/AgzYuOX.jpg)


![](https://i.imgur.com/4qBOx6h.jpg)


* Control Plane - Master Node
* Node Pools - workder node(container actually running)
* Pods - Container Group
* Network -kubenet , CNI


## Governance and Compliance 

### Manage Subscription

![](https://i.imgur.com/olwGYd4.jpg)

* Billing Unit
* Only associate one Azure AD tenant.


### Using Management Groups

![](https://i.imgur.com/87Ws321.jpg)

Can enforce the policy and compliance on management group.

![](https://i.imgur.com/UmKrrTR.jpg)

![](https://i.imgur.com/ZClOUDw.jpg)



![](https://i.imgur.com/HX75IDx.jpg)
* Global Administrators 必須要升級到 User Access Administrator 才可以管理 root group.


### Understanding Azure Policy

![](https://i.imgur.com/SKiZLqy.jpg)



![](https://i.imgur.com/YMYX892.jpg)

他會 require 需要 tag resource or not.


![](https://i.imgur.com/JpvcAQf.jpg)


![](https://i.imgur.com/g8evjOL.png)

套一個 policy 要 30 mins


### Tagging Resource

![](https://i.imgur.com/qKgROXn.jpg)

* Tag are not inherited


Use Command like

`az resource list --tag xxx --query [].name -o tsv`

可以看到哪些有上 tag

若要 delete 需要 id


![](https://i.imgur.com/W0GD3wq.jpg)


Update Tags


![](https://i.imgur.com/wkPUEiu.png)


![](https://i.imgur.com/Gj8vnaU.png)

### Locking and Moving Resources

![](https://i.imgur.com/XOmmy3b.jpg)


![](https://i.imgur.com/b2quOIn.jpg)


* ReadOnly: allow read a resource, but they cannot delete or update resource
* CanNotDelete allow read and modify, but cann't delete.
* Locks are inherited


![](https://i.imgur.com/lv0b2X9.png)


Move resources:

![](https://i.imgur.com/rm3Wsh7.jpg



Not all services have move 

![](https://i.imgur.com/eHPfJmZ.jpg)



### Managing Azure Costs





TCO compared with on-premise.

### Build a Cloud Governance Strategy


![](https://i.imgur.com/MvFHu00.jpg)


![](https://i.imgur.com/Ps8nxoy.jpg)


## Identity


Principal:
An unauthenticated entity that will seek to authenticate as identity.




![](https://i.imgur.com/bhUc3Tr.jpg)

Organization = Tenant = Directory



![](https://i.imgur.com/mD07EbT.jpg)

PIM (Privileged Identity Management)

Just-in-Time Approval-based




![](https://i.imgur.com/iRP8xmp.jpg)


![](https://i.imgur.com/NnIWSJa.jpg)

### Managing Tenants

![](https://i.imgur.com/jCe9GMZ.jpg)


![](https://i.imgur.com/EreubO4.jpg)

### Create and managin user

![](https://i.imgur.com/mlVXfCv.png)


![](https://i.imgur.com/m21IaPe.jpg)



Go to AD to create user.

![](https://i.imgur.com/rZ4GovM.png)


While creating an user could assign Azure AD roles


![](https://i.imgur.com/tU7aJOp.jpg)


You can use bulk operations to create users, like uploading csv files.

![](https://i.imgur.com/YB0r9ON.jpg)


### Configuring SSPR(self-service password reset)

![](https://i.imgur.com/4gk6bov.jpg)


![](https://i.imgur.com/TBRxhN7.jpg)



### Azure AD Device Management

![](https://i.imgur.com/dfl41Ts.jpg)


![](https://i.imgur.com/m2whVy6.jpg)




Required Azure AD P1 license or Microsoft 365 Business License.





![](https://i.imgur.com/KUMaDjJ.jpg)




Microsofr Defender for Cloud Changed alot of stuff.

[Microsoft Defender for Cloud Apps overview](https://docs.microsoft.com/zh-tw/cloud-app-security/what-is-defender-for-cloud-apps)





![](https://i.imgur.com/aLMJfVy.jpg)


### Azure AD Joined 


![](https://i.imgur.com/o1r2F3Z.jpg)



![](https://i.imgur.com/TLx8YIZ.jpg)


## Role-Based Access Control




![](https://i.imgur.com/dbXULWV.jpg)


We have two types role:

Azure RBAC role:

Three typical roles:

**Owner Role**: Full access to resources and delegates access

**Read-Only**: Can only view resources

**Contributor**: Can create and manage resources, but cann't delegate resources with other users.


**User Access Administrator**: Can delegate access to resources.





![](https://i.imgur.com/pURD3cw.jpg)



Azure AD role:

Identity resources rather than cloud resources

**Global Administrator role**: Can manage Azure AD Resources

**Billing Administrator**: Can perform billing task

**User Administrator**: Can manage users and group

**Helpdesk Administrator**: Can reset password for users.


![](https://i.imgur.com/saTJAMh.jpg)




![](https://i.imgur.com/XdsQBGH.jpg)


Azure AD Roles 只有 for 它自己而已


### Assigning Access to Resources


![](https://i.imgur.com/hqJIdf7.jpg)


![](https://i.imgur.com/cl7qOum.jpg)


1. Select user -> Select Role -> Select Scope

![](https://i.imgur.com/pAaEQOQ.png)


Contributor role cann't assign role to others.

### Create Custom Roles



![](https://i.imgur.com/m0CG70v.jpg)


## Azure Storage  (天坑)

### Storage Account

*Name is global unique*




![](https://i.imgur.com/3aLQJ75.png)



![](https://i.imgur.com/dpaHS5z.jpg)


![](https://i.imgur.com/KotOP9E.jpg)




![](https://i.imgur.com/oqVRD1a.png)


* Geo-Redundant  (GRS)
for secondary region, for backup senarios

* Zone-Redundant  (ZRS)
for HA, datacenter-level

* Geo-Zone-redundant storage (GZRS)
both, for critical data scenarios



![](https://i.imgur.com/hA4wqR7.jpg)


### Conceptualize Azure Blob Storage





![](https://i.imgur.com/6HeNdyW.jpg)




Container is bucket, blob is object





![](https://i.imgur.com/mAcrnp5.jpg)

* Blob have three types:
    * Block Blob: Storing images or Videos, Best suited for streaming
    * Append Blob: Logs file
    * Page Blob: Virtual Machine Disks



![](https://i.imgur.com/oOs4v5w.png)




* Access Levels:


![](https://i.imgur.com/CdHYtTI.jpg)


### Object Replication

![](https://i.imgur.com/CMwb2hw.jpg)







![](https://i.imgur.com/wHQhRX7.jpg)



* You have to turn on the blob change feed that you could use object replication.




![](https://i.imgur.com/JGbunps.jpg)






![](https://i.imgur.com/25WwzGV.jpg)






![](https://i.imgur.com/Dt04ArL.png)



![](https://i.imgur.com/Xbt4OdZ.jpg)



### Configure Azure File

Fully managed file service.

Features:
* SMB connectivity
* Supports Windows, Linux, and macOS
* Extended by Azure File Sync
* Traditional file structure



![](https://i.imgur.com/3BOFmOy.png)




![](https://i.imgur.com/0z6zZe3.png)

SMB 2.1 is not encrypted.



![](https://i.imgur.com/yxrFONi.png)

VM 的 fileshare 是用 connect 指令去加入的。


![](https://i.imgur.com/7eBf6s7.png)




### Condifgure Azure File Sync

Azure File Sync is an extension of Azure Files that allows you to extend the capabilities of on-premises file servers.


Features:

* Locally cache frequently accessed files.
* Requires Windows 2021 R2 or later
* SMB, NFS, and FTPS
* Require File Sync Agent


![](https://i.imgur.com/e3lrihQ.jpg)

### Storage Network Access


![](https://i.imgur.com/Nmo83m8.jpg)

We do have storage account firewall.



![](https://i.imgur.com/2SGYOZO.jpg)


### Securing Storage Accounts





![](https://i.imgur.com/SktRgdV.jpg)



![](https://i.imgur.com/gjfEpXn.jpg)


A shared access signature (SAS) is a URI that grants restricted access rights to Azure Storage resources. You can provide a shared access signature to clients who should not be trusted with your storage account key but whom you wish to delegate access to certain storage account resources. By distributing a shared access signature URI to these clients, you grant them access to a resource for a specified period of time.
An account-level SAS can delegate access to multiple storage services (i.e. blob, file, queue, table). Note that stored access policies are currently not supported for an account-level SAS.



![](https://i.imgur.com/rWV8mlw.jpg)


### Using Azure Jobs (storage gateway)


![](https://i.imgur.com/VP9MrRL.jpg)




![](https://i.imgur.com/FcCLsPA.jpg)


![](https://i.imgur.com/N8uMfWe.jpg)



it was an import/export jobs.




### Storage Utilities



Right now is Storage Browser.

console 叫 browser, 但 download 是 explorer



![](https://i.imgur.com/chTXtdO.png)



![](https://i.imgur.com/47ubJyR.jpg)






## Backup and Recover

### Understanding Disaster Recovery

What is Disaster Recovery?
The purpose of recovering from a disasterm such as a datacenter poewer outage. Every business needs a business continuity and disaster recovery plan.

* Assess risks
* Determine critical workloads
* Decide backup technique
* Test disaster recovery

#### RPO, RTO



![](https://i.imgur.com/RlJhgmY.png)


#### Methods



![](https://i.imgur.com/cNIRg38.png)

* Cold Site and Hot Site



### Configuring Azure Backup

Backup as a Service-
Azure Backup is managed service for backing up and recovering workloads.

On-premise workloads could be Hyper-V or VMWare Workloads.

* Requires an Azure Recovery Services Vault!!


![](https://i.imgur.com/U21czjz.png)


Backup could restore cross region


supported workloads:
* Azure Virtual Machines
* On-premises machines
* SQL Server Workloads
* SAP HANA workloads
* Azure file share



![](https://i.imgur.com/kO62OJx.png)



![](https://i.imgur.com/Re0jL0H.png)




![](https://i.imgur.com/XqYleAM.png)


![](https://i.imgur.com/J1CiMsa.png)



![](https://i.imgur.com/h5VFIaO.png)


#### Backup Policy for Schedule retention

![](https://i.imgur.com/B9erlqg.png)


As soon as VM stop, we could restore it.

You could create another storage account for backing up.



![](https://i.imgur.com/YqPzyeX.png)



### Azure Site Recovery

Azure Site Recovery service provides a solution for automating DR.

Also, it need to require an Azure Recovery Services vault.

你如果要跨 region 要先設置

* Cross-zone
* Cross-region

![](https://i.imgur.com/18zmtCC.png)


![](https://i.imgur.com/q3MXFrk.png)


You could test replication by this way.


![](https://i.imgur.com/fCXaskE.png)



#### Key  Takeaways


![](https://i.imgur.com/InvtPXa.png)


### Backup Reports


![](https://i.imgur.com/eO7eKRs.png)






Create Log Analytics Workspace

For restore operations, backup operations



![](https://i.imgur.com/5NqWbK7.png)










## Monitoring (非常強大)

 
 
![](https://i.imgur.com/J8vpvMM.png)


Metrics and Logs


![](https://i.imgur.com/vyWm8R3.png)



![](https://i.imgur.com/NLqjejg.png)


![](https://i.imgur.com/zVkldCg.png)

### Setting Up Alerts and Actions


![](https://i.imgur.com/nD9uYjs.png)

Logic App, Azure Automation 



![](https://i.imgur.com/ilxzp4W.png)



![](https://i.imgur.com/Bxy4ely.png)




![](https://i.imgur.com/PcIloBi.png)



![](https://i.imgur.com/eSYkUm9.png)


### Configure Azure Monitor Logs



![](https://i.imgur.com/XzKC6cC.png)



![](https://i.imgur.com/8o4EHzW.png)


You can query the log data for using kusto Query Language.

![](https://i.imgur.com/hDTvXfq.png)




![](https://i.imgur.com/1qY5FPH.png)

###  Monitor Insights

Service-specific monitoring features built into Azure Monitor.

Includes:
* VM Insights
* Network Insights
* Container Insights
* Application Insights

![](https://i.imgur.com/6bSTox0.png)

tandem with 串聯


![](https://i.imgur.com/1Xe1TtA.png)


![](https://i.imgur.com/CcDOgKU.png)


### Configuring Application Insights



![](https://i.imgur.com/9xHeQ1Y.png)


![](https://i.imgur.com/6v89xzk.png)



![](https://i.imgur.com/KlYjkVV.png)





![](https://i.imgur.com/eUg7nIh.png)


![](https://i.imgur.com/cQPe4RL.png)


### Using Network Watcher


![](https://i.imgur.com/50dw56Z.png)


![](https://i.imgur.com/exO4PfC.png)



![](https://i.imgur.com/A14cAeU.png)






### Appendix 

#### Azure Instance Type

**Bs-series**
Bs-series are economical virtual machines that provide a low-cost option for workloads that typically run at a low to moderate baseline CPU performance, but sometimes need to burst to significantly higher CPU performance when the demand rises. These workloads don’t require the use of the full CPU all the time, but occasionally will need to burst to finish some tasks more quickly. Many applications such as development and test servers, low traffic web servers, small databases, micro services, servers for proof-of-concepts, build servers, and code repositories fit into this model.


**Av2 Standard**
Av2 Standard is the latest generation of A-series virtual machines with similar CPU performance and faster disk. These virtual machines are suitable for development workloads, build servers, code repositories, low-traffic websites and web applications, micro services, early product experiments, and small databases. Like the prior A Standard generation, Av2 virtual machines will include load balancing and auto-scaling at no additional charge.



**D2as – D96as v5 (latest generation without local temporary storage)**

The Das v5-series virtual machines are based on the 3rd Generation AMD EPYCTM 7763v (Milan) processor. This processor has base frequency of 2.55Ghz and can achieve up to 3.7GHz. The Das v5 VM sizes offer a combination of vCPUs and memory able to meet the requirements associated with most production workloads.

The Das v5 virtual machine sizes do not have any temporary storage thus lowering the price of entry. You can attach Standard SSDs, Standard HDDs, and Premium SSDs disk storage to these VMs. You can also attach Ultra Disk storage based on its regional availability. Disk storage is billed separately from virtual machines. See pricing for disks.

Prices displayed in the table below may increase starting December 1st, 2021 to reflect general availability pricing.


**Compute optimized**
High CPU-to-memory ratio. Good for medium traffic web servers, network appliances, batch processes, and application servers.


**Memory optimized**
High memory-to-core ratio. Great for relational database servers, medium to large caches, and in-memory analytics.


**Storage optimized**
High disk throughput and IO. Ideal for Big Data, SQL, and NoSQL databases.


**High performance compute**
Our fastest and most powerful CPU virtual machines with optional high-throughput network interfaces (RDMA).

Too many 

https://azure.microsoft.com/en-us/pricing/details/virtual-machines/linux/





#### What us BGP ( Border Gateway Protocol)

邊界閘道器協定（英語：Border Gateway Protocol，縮寫：BGP）是網際網路上一個核心的去中心化自治路由協定。它通過維護IP路由表或「字首」表來實現自治系統（AS）之間的可達性，屬於向量路由協定。BGP不使用傳統的內部網路關協定（IGP）的指標，而使用基於路徑、網路策略或規則集來決定路由。因此，它更適合被稱為向量性協定，而不是路由協定。


### What is Azure Network Virtaul Appliance (NVA)?

Azure network virtual appliance is used in the Azure application to enhance high availability. It is used as an advanced level of control over traffic flows, such as when building a demilitarized zone (DMZ) in the cloud.


https://aviatrix.com/learn-center/cloud-security/azure-network-virtual-appliance/



### What is IKE?

網際網路金鑰交換（英語：Internet Key Exchange，簡稱IKE或IKEv2）是一種網路協定，歸屬於IPsec協定族，用以建立安全關聯（Security association，SA。它建立在奧克利協定（Oakley protocol）與ISAKMP協定的基礎之上。

### BitLocker
BitLocker（直譯為「位元鎖」）是內建於Windows Vista及其之後系統的全磁碟加密功能，透過為整個卷提供加密來保護資料。它預設在密碼塊連結（CBC）或XTS模式下使用128位元或256位金鑰的AES加密演算法。其中CBC用於每個單獨的磁碟磁區，不在整個磁碟上使用。

### DM-Crypt

dm-crypt是Linux內核2.6及以後後繼版本和DragonFly BSD中的一個磁碟加密系統。與它的前身Cryptoloop不同，dm-crypt可以避免水印攻擊。除此之外，dm-crypt解決了cryptoloop的一些可靠性問題。

一些Linux發行版支持在根文件系統上使用dm-crypt。這些發行版使用Initrd來提示用戶在控制台輸入密碼



### Custom Data 

*In other cloud, it would called user data*

You may need to inject a script or other metadata into a Microsoft Azure virtual machine at provisioning time. In other clouds, this concept is often referred to as user data. In Microsoft Azure, we have a similar feature called custom data.

Custom data is only made available to the VM during first boot/initial setup, we call this 'provisioning'. Provisioning is the process where VM Create parameters (for example, hostname, username, password, certificates, custom data, keys etc.) are made available to the VM and a provisioning agent processes them, such as the Linux Agent and cloud-init.

### 服務權限

基本上每個服務都會有 identity 可以給





## Service-Principal v.s Managed identity

Typical use cases where you would rely on a Service Principal is for example when running Terraform IAC (Infrastructure as Code) deployments, or when using Azure DevOps for example, where you define a Service Connection from DevOps Pipelines to Azure; or basically any other 3rd party application requiring an authentication token to connect to Azure resources.

Managed Identities are in essence 100% identical in functionality and use case than Service Principals. In fact, they are actually Service Principals.

What makes them different though, is: – They are always linked to an Azure Resource, not to an application or 3rd party connector – They are automatically created for you, including the credentials; big benefit here is that no one knows the credentials


[Link](https://devblogs.microsoft.com/devops/demystifying-service-principals-managed-identities/)


## Microsoft Endpoint Manager admin

IS new for microsoft intune



![](https://i.imgur.com/QPNZyLh.png)



