---

copyright:
  years: 2024
lastupdated: "2025-03-25"

keywords:

subcollection: powervs-migration

---

{{site.data.keyword.attribute-definition-list}}


# Migration to Power Virtual Server on IBM Cloud
{: #white-paper}

This whitepaper describes the business challenges with On Premise and Co-Located Power workloads and provides prescriptive solution choices to move the platform to  {{site.data.keyword.powerSys_notm}} on IBM Cloud. The  many design considerations involved in making this determination and the migration approach  are described in this paper.
{: shortdesc}



## Overview
{: #1-overview}

Organizations are increasingly turning to cloud solutions to enhance scalability, reduce costs, and improve flexibility. IBM Power Virtual Server (PowerVS) in IBM Cloud offers a robust platform for running IBM AIX, Linux, and IBM i workloads with the benefits of cloud infrastructure. This white paper aims to guide businesses through the migration process, highlighting key considerations and actionable steps.This whitepaper describes the business challenges with On Premise and Co- Located Power workloads and provides prescriptive solution choices to move the platform to Power Virtual Server on IBM Cloud. The  many design considerations involved in making this determination and the migration approach  are described in this paper.

### Challenges
{: #1-1-challenges}

The challenges businesses face in maintaining their on-premises data centers or co-location facilities are driving a trend of organizations opting to exit traditional data center operations in favor of more flexible and cost-effective alternatives. Here are some common challenges for this shift:

* **High Costs of Operation**
    * **Capital Expenditures (CapEx):** On-premises data centers require significant upfront investments in hardware, software, and infrastructure.
    * **Operational Expenditures (OpEx):** Costs for maintenance, power, cooling, and staffing add up, often exceeding budgets.
    *	**Scalability Costs:** Scaling on-premises infrastructure is costly and time-consuming compared to cloud solutions.
* **Limited Scalability and Agility**
    *	**Demand Variability:** On-premises systems are not easily scalable to meet fluctuating demands, leading to over-provisioning or underutilization of resources.
    * **Rapid Innovation:** Businesses need to innovate quickly, but legacy systems in data centers can’t keep pace with emerging technologies.
*	**Complexity in Maintenance**
    * **Infrastructure Upkeep:** Regular upgrades and replacements for hardware and software create operational burdens.
    * **Specialized Skills Required:** IT teams need expertise in various aspects, including networking, storage, and security, which can be hard to maintain.
* **Security and Compliance Challenges**
    * **Cybersecurity Risks:** Managing security for on-premises systems is resource-intensive and requires continuous vigilance.
    *	**Regulatory Compliance:** Adhering to evolving data protection regulations (e.g., GDPR, HIPAA) is complex and costly for in-house systems.
*	**Business Continuity Risks**
    * **Disaster Recovery:** Maintaining robust disaster recovery and backup systems on-premises is challenging and expensive.
    *	**Downtime Risks:** Power outages, hardware failures, and other issues can lead to costly downtime.

These factors apply to the clients who maintain IBM Power servers in on-prem data centers, and one option is to take advantages of the Power Virtual Server in IBM Cloud.

### Why Power Virtual Server on IBM Cloud
{: #1-2-why-powervs}

IBM Power Virtual Server is an IBM Power server offering. Clients can use Power Virtual Server to deploy a virtual server, also known as a logical partition (LPAR), in a matter of minutes. Additionally, flexible, secure, and scalable compute capacity for Power enterprise workloads on IBM Power Virtual Server can be provisioned in IBM Cloud.

Note that IBM also offers Power Virtual Server on-prem, Power Virtual Server Private Cloud, which allows clients to take advantage of the cloud capabilities and cost models. We will focus on IBM Power Virtual Server in IBM Cloud in this article.
{: note}

Here are some of the benefits by using Power Virtual Server in IBM Cloud.

**Performance with latest Power processor**

Client can provision IBM Power Virtual Server in IBM data centers in a matter of minutes, and take advantage of the latest Power processor.

IBM makes constant innovations on the Power processors, and push out a newer version of IBM Power every 2 or 3 years. It is built to meet today’s challenges with new levels of performance, core-to-cloud data protection, and streamlined automation and insights. Power systems have more crypto accelerators per core, provides full memory encryption at scale, and support quantum-safe cryptography. Power 10 can accelerate AI training and inferencing with its built-in Matrix Math Accelerators (MMA) without requiring external accelerators, such as GPUs, for executing statistical machine learning and inferencing (scoring) workloads. It also offers memory sharing among Power Servers to handle AI models at scale. This further drives a business demand for a flexible and scalable cloud compute consumption model.

**Flexibility and scalability**

Power Virtual Server is available across 10 IBM Cloud multi-zone regions across Americas, Europe and APAC and 22 data centers. Client can deploy Power Virtual Serverin IBM data centers around the globe, with scalable resources adjustable based on demand.

**Cost-effective OPEX model**

With flexible pay-as-you-go model, client only pays for what they use. This not only applies to the Power Virtual Server compute, but also to the storage. Client can move away from costly dedicated on premise storage to more scalable cloud storage models – replacing Tape with Cloud Object Storage, SAN with Cloud block & file or use vSAN in the VMware SDDC model on cloud bare metal servers.

**Smooth transition to cloud**

IBM Power Virtual Server has the same architecture in a cloud environment as IBM Power on-premises. It supports AIX, IBM i, Linux and OpenShift, and is certified for SAP and Oracle workloads, allowing a smooth transition for businesses already using IBM Power systems to cloud.

**Improved platform availability:** The accelerated shift to a digital economy, partly due to the Covid pandemic, along increased business demand for higher availability of production critical applications requires greater platform availability of 99.99+%.

**Security:** Business requires secure the software supply chain for both intellectual capital (asset) protection and certified untampered code. The number and cost of cyber-attacks has greatly escalated in recent years. This has caused businesses to take a more disciplined approach to system and data security. End to end encryption is needed to secure business data and encryption key management has taken on increased importance. On IBM Cloud, businesses have options to use IBM provided keys or can bring their own encryption keys (BYOK).  With Hyper Protect Crypto Services (HPCS), IBM Cloud offers a unique solution which allows a business to keep their own keys (KYOK) on a dedicated key management service and Hardware Security Module.  Ransomware, cyber-attacks and other security related issues added the business requirement of a minimum viable company (MVC) platform solution.

**Sustainability** IT agility is key to business success today. Businesses need scalable and elastic environments.  Cloud platforms enable this capability and IBM Cloud provides automation for the Power VS platform to further enhance this agility. Integration with other IBM Cloud services such as Cloud Logs, Activity Tracker, Monitoring and Log Analysis provide insights to clouds usage and facilitate auditing and control.

This document outlines the migration considerations, proposes migration strategies, and directs users to the relevant documentation for Power workloads migration from on-premises to IBM Cloud,

**Benefits of Migrating to IBM Power Virtual Server**

* **Scalability:** Seamlessly scale resources up or down based on workload demands.
* **Cost Efficiency:** Reduce capital expenditure by leveraging a pay-as-you-go model.
* **Flexibility:** Easily adapt to changing business needs with cloud-based infrastructure.
* **Performance:** Benefit from high-performance computing capabilities and enhanced security features.
* **Disaster Recovery:** Implement robust disaster recovery solutions with IBM Cloud's resilience.


### Use cases for Power Virtual Server on IBM Cloud
{: #1-3-usecases}

IBM Power Virtual Server is a family of configurable multi-tenant virtual IBM Power servers with access to IBM Cloud services. It supports AIX, IBM i, Linux and OpenShift, and is certified for SAP and Oracle workloads. It has exactly the same stack as IBM Power on-premises and provides clients with a consistent experience.

Here are typical use cases for IBM Power Virtual Server:

**Data center optimization and operational excellence**

Many companies are adopting cloud strategies to address the challenges of traditional on-premises data centers. By leveraging solutions like IBM Power Virtual Server as companies exit or optimize their data centers, businesses can seamlessly lift and shift critical applications to the same stack, reducing operational costs, improving service quality with faster response times, and benefiting from flexible pay-as-you-go billing. This approach supports growth and global expansion while ensuring scalability, reliability, and performance for critical workloads.

**Business continuity planning**

Companies can enhance resilience by backing up their data to the cloud, ensuring business continuity with reliable failover solutions like backup, high availability, and disaster recovery. IBM Power Virtual Servers help reduce capital expenditure, simplify planning, and eliminate the need to maintain excess capacity, all while providing scalable and dependable protection against unexpected disruptions.

**Modernization**

IBM Power Virtual Server resources reside in IBM data centers with dedicated networking and Storage area network (SAN)-attached Fibre Channel storage. The internal networks are fenced but offer connectivity options to IBM Cloud infrastructure or private cloud environments. This infrastructure design enables Power Virtual Server to maintain key enterprise software certification and support as the Power Virtual Server architecture is identical to certified private cloud infrastructure. It also enables IBM Power Virtual Server to connect to over 190 IBM Cloud services seamlessly. Companies can utilize cloud services to modernize applications by enhancing scalability, integrating advanced tools, and enabling seamless updates. This approach supports faster innovation, improves performance, and ensures your applications are equipped to meet evolving business demands.



## Migration process
{: #2-migration-process}

**Migration considerations**

Different factors should be considered before choosing the right migration strategy.

* Environment - whether it is dev/test non-production environment or production environment
* Workloads – Host/OS, application or database
* Data size - Small,  Medium,  Large (Image/system and data size)
* Allowable downtime - how much downtime is needed to safely complete the migration
* Network options - Public Internet/IPSEC VPN, Private(Direct Link) Bandwidth and size
* Skills – Prefer managed solution or has skills to perform the tasks
* Cost – Stick to existing licenses or OS commands or acquire new software/tools

Migration strategies:
-	Storage replication: in-cloud only (eg. GRS, hard to do from on-prem to cloud with potential different storage types client owns)
-	Backup and restore: on-prem to cloud

Decision tree:
* Consider the relevant factors mentioned above
* Common tools included with Power includes: services from IBM Cloud Catalog and common tools to Power users
  * PowerHA / BRMS / SystemMirroring / ICC
  *  OS tools
  *  App tools
* Services/offerings from IBM Cloud includes:
  *  Cobalt Iron – Secure Automated Backup with Compass
  *  FalconStor StorSafe VTL for Power Virtual ServerCloud
  *  Power I Migrate 23 Services (TSP/BUS4i)
  *  Power I Migrate While Active Services (TSP/BUS4i)
  *  BUS4i System Copy – Migrate 23 for Power i (There are a few BUS4i items in the catalog)
  *  Power Virtual ServerMigration as a Service (Wanclouds, consulting services)
  *  Partner with Technology Expert Labs

**Migration process**

* Engage with IBM and utilize IBM Migration Acceleration program (out of scope of this doc)
* Client managed migration
    * Capacity planning (compute, memory, disk, network)
    * Network setup (security, performance, business (eg. KYIP) requirements)
      * FS clients may require extra security, eg. some client even uses VPN on top of DL for performance and extra security
    * Infrastructure setup (security, scalability, compliance, monitor, auditing, etc.)
      * Use of Deployable Architecture
      * SCC
      * Key protect/HPCS
      * Financial Services best practices and recommendations (Financial Services validated services)
    * Workload migration
      * Focus of this doc, will drill down into details in the following section
      * Various IBM Cloud services, tools, and ISV
	    * Different OS, apps, goals have different requirements
    * Backup/HA/DA/Resiliency
    *	Cloud ecosystem, integration with other cloud services or hybrid cloud
    * Security and compliance (SCC, LogDNA, monitoring)


## Migration AIX/Linux to IBM Cloud
{: #3-migrate-aix-linux}

**AIX Decision Tree**

![AIX migration decision tree](/images/aixmigration.svg "Reference Summary"){: caption="{{site.data.keyword.powerSysFull}} AIX decision tree" caption-side="bottom"}{: external download="aixmigration.svg"}

There are 4 migration options listed below which are discussed in detail in the following sections:

**Backup and restore using mksysb images**

Migrating AIX workloads to IBM Power Virtual Server using the mksysb method offers a reliable and efficient way to ensure data consistency and system integrity. This method leverages the well-established mksysb command, which creates comprehensive backups of the entire system, including the operating system, configurations, and data. The process minimizes downtime and disruption, allowing businesses to achieve a smooth transition from on-premises to cloud infrastructure. Additionally, the mksysb method is highly customizable, enabling organizations to tailor backups to specific needs and optimize the use of cloud resources. Power Virtual Serverenhances this flexibility by providing scalable resources that adapt to changing workload demands, ensuring cost-effective and efficient cloud infrastructure management.
Security and performance are also key benefits of migrating to Power Virtual Serverusing the mksysb method. Data encryption safeguards sensitive information both in transit and at rest, while isolated environments prevent unauthorized access. Power Virtual Serverleverages IBM Power Systems' high-performance computing capabilities, ensuring efficient operation of AIX workloads in the cloud. Enhanced networking features, including low-latency connections and high-speed data transfer, improve overall performance. Robust disaster recovery solutions and simplified management further ensure data protection, continuity, and ease of oversight, making this method a secure and effective choice for migrating AIX workloads to IBM Power Virtual Server.

**Host and Operating System Mirroring using GLVM**

Migrating AIX workloads to IBM Power Virtual Server using Host and OS System Mirroring with Geographic Logical Volume Manager (GLVM) ensures continuous data protection and high availability. GLVM replicates data at the logical volume level between on-premises systems and PowerVS, minimizing downtime and maintaining business continuity. PowerHA SystemMirror enhances this setup by automating management and monitoring, ensuring seamless operation. This method leverages PowerVS's scalable and high-performance infrastructure, providing efficient data replication and resource optimization while offering robust security through data encryption and isolated environments.
Additionally, this approach is cost-efficient, reducing infrastructure costs through a pay-as-you-go model and optimized resource utilization. It provides robust disaster recovery solutions and ensures compliance with data protection regulations. The centralized control and simplified management offered by PowerVS, combined with the automated processes of PowerHA SystemMirror, make the migration process streamlined and reliable. This ensures that businesses can efficiently transition their AIX workloads to the cloud, maximizing the benefits of cloud infrastructure while minimizing risks and costs.

**Database replication**

Migrating databases to IBM Power Virtual Server using database replication offers the advantage of maintaining real-time synchronization between your on-premises database and the cloud environment. This method ensures that the transition process is seamless, with minimal downtime and disruption to your business operations. By replicating data at the database level, any changes made to the source database are instantly reflected in the target environment, which helps maintain data consistency and integrity throughout the migration. This approach is particularly beneficial for businesses that require high availability and continuous access to their databases, as it minimizes the risks associated with data migration and ensures a smooth handover.

Moreover, the scalability and performance capabilities of Power Virtual Server allow optimization of resource utilization and adaptability to fluctuating workload demands. Power Virtual Server offers enhanced security features, including data encryption and isolated environments, which safeguard sensitive information and ensure compliance with data protection regulations. This method provides a robust disaster recovery solution, enabling quick recovery and continuity in the event of an on-premises system failure. By leveraging database replication for your migration to PowerVS, you can enhance the resilience, flexibility, and overall efficiency of your IT infrastructure, while ensuring that critical business functions remain uninterrupted and secure.

**3rd party replication software**

Migrating AIX workloads from on-premises to IBM Power Virtual Server can be efficiently managed using various third-party applications. Options such as FalconStor StorSafe VTL, Double-Take® Move™ for AIX, and MIMIX are designed to facilitate seamless migration with minimal downtime and disruption. These tools ensure robust data integrity and continuous availability during the migration process, making them ideal for critical workload transitions. They offer features like high availability, disaster recovery, and flexible data seeding options, which streamline the migration and optimize resource utilization.
Using these third-party solutions, businesses can achieve a smooth transition to Power Virtual Serverwhile benefiting from advanced backup and recovery capabilities. FalconStor StorSafe VTL, and Mimix for instance, optimizes the migration by emulating physical tape drives, while MIMIX is known for its near-zero downtime and realistic data testing. Each tool provides unique benefits tailored to different migration needs, ensuring data protection and high performance in the cloud environment. By leveraging these applications, organizations can ensure a reliable and efficient migration, enhancing their IT infrastructure's resilience and flexibility.

### Backup and restore using mksysb images
{: #1-migration-mksysb}

**Backup and restore using mksysb images**

Overview

In this option, the existing AIX lpar is backed up using the inbuilt mksysb functionality. It may also require using Savvg for LPARS with separate volume groups defined.

This option should be considered for those businesses who want an identical system migrated to IBM cloud, lowest cost and shortest timeframe to migrate.

Migrating AIX workloads to IBM Power Virtual Server using mksysb and savevg provides a comprehensive approach that ensures all system and data elements are efficiently transferred to the cloud. This method leverages native AIX tools to create and transfer backups of the entire system, making it a reliable and well-structured migration strategy. By utilizing these built-in commands, the migration process becomes more streamlined, cost-effective, and time-efficient, ensuring minimal downtime and disruption to business operations.

First, create a mksysb backup on your on-premises AIX system to capture the entire root volume group (rootvg), including the operating system, configurations, and root-level data. Transfer this backup to PowerVS, where it is restored to set up the base system environment. Next, use the savevg command to back up additional volume groups beyond rootvg, capturing their respective data. These backups are then transferred to Power Virtual Serverand restored using the restvg command, ensuring that all data and configurations are replicated accurately in the cloud environment.

This method is cost-effective because it leverages existing native AIX tools, eliminating the need for expensive third-party migration software. The mksysb and savevg commands are built into AIX, so there are no additional licensing costs. Additionally, using cloud storage for transferring backups helps avoid costs associated with physical media and dedicated migration hardware. The pay-as-you-go model of Power Virtual Serverfurther reduces capital expenditures, optimizing overall migration costs.

In terms of time efficiency, this approach minimizes downtime through a streamlined backup and restore process. The mksysb command creates a comprehensive system backup in one go, reducing the complexity and time required for data transfer. Similarly, the savevg command ensures that additional volume group data is backed up efficiently. Transferring these backups via cloud storage expedites the migration process, ensuring a quick and seamless transition. This approach ensures business continuity with minimal disruption, making it a practical and efficient solution for migrating AIX workloads to PowerVS.

**Benefits**

 **Comprehensive Backup and Recovery:** Ensures full system protection by backing up the entire root volume group (rootvg) and additional volume groups, capturing all necessary data and configurations.
 **Cost-Effectiveness:** Utilizes built-in AIX tools with no additional software costs and takes advantage of cloud storage and the pay-as-you-go pricing model of Power Virtual Serverto reduce overall costs.
 **Time Efficiency:** Streamlines the migration process with comprehensive system backups and efficient data transfer,minimizing downtime and ensuring a quick transition.
 **Flexibility and Scalability:** Offers tailored backups for specific system components and scalable resources to meet changing workload demands, optimizing the migration process.
 **Enhanced Data Integrity and Security:** Maintains data integrity with accurate replication of the entire system and secure data transfer using cloud storage.

**Limitations**

Need to fill in

 Add mksysb backup and restore diagram here
Figure 1 -AIX  mksysb

**AIX Case Study**

**Case Study: Migrating AIX Workloads to IBM Power Virtual Server Using mksysb and savevg**

**Client Overview:** XYZ Corporation, a mid-sized manufacturing company, relies heavily on AIX systems for its critical business operations, including ERP and supply chain management. With growing data needs and an aging on-premises infrastructure, XYZ Corporation decided to migrate their AIX workloads to IBM Power Virtual Server to leverage the cloud's scalability, performance, and cost efficiencies.

**Challenges:**
  *	Aging Infrastructure: XYZ Corporation's on-premises hardware was reaching end-of-life, increasing the risk of hardware failures and downtime.
  * Data Integrity: Ensuring the integrity of critical data during the migration process was paramount.
  * Minimal Downtime: The manufacturing processes could not afford significant downtime, necessitating a seamless transition.

**Solution:** To address these challenges, XYZ Corporation chose to use the mksysb and savevg commands for a comprehensive and efficient migration strategy.

**Migration Process:**

1. **Preparation:**
    * **Assessment:** Evaluated the current AIX environment, identifying all volume groups and critical data.
    * **Set Up PowerVS:** Provisioned the target environment in IBM PowerVS, ensuring compatibility with the existing AIX systems.
2. **Creating Backups:**
    * **mksysb Backup:** Generated a mksysb backup of the root volume group (rootvg), capturing the operating system, configurations, and root-level data.
    * **savevg Backup:** Used savevg to back up additional volume groups, ensuring that all critical data was included in the backups.
3. **Transferring Backups:**
    * **Cloud Storage:** Transferred the mksysb and savevg backup files to IBM Cloud Object Storage, utilizing secure and reliable transfer methods.
4. **Restoring Backups on PowerVS:**
    * **Provisioning VSI:** Created a new Virtual Server Instance (VSI) in Power Virtual Serverto match the source AIX system's specifications.
    * **Restoring mksysb Backup:** Used the mksysb backup to restore the rootvg on the new VSI, setting up the base system environment.
    * **Restoring savevg Backups:** Applied the restvg command to restore the additional volume groups from the savevg backups, ensuring all data and configurations were replicated accurately.
5. **Testing and Validation:**
    * **System Verification:** Verified that the restored system on Power Virtual Servermatched the on-premises environment, with all configurations and data intact.
    *	**Application Testing:** Conducted thorough testing of critical applications to ensure they functioned correctly in the new environment.
6. **Final Cutover:**
    *	**Data Synchronization:** Ensured the latest data changes were synchronized between the on-premises system and PowerVS.
    * **Production Cutover:** Switched production operations to the new environment on PowerVS, with minimal disruption to business processes.
7. **Post-Migration Monitoring:**
    * **Continuous Monitoring:** Implemented monitoring tools to ensure the new environment operated smoothly and addressed any issues promptly.

**Results:**

**Cost Savings:**
 **Reduced Infrastructure Costs:** By moving to PowerVS, XYZ Corporation reduced the costs associated with maintaining and upgrading on-premises hardware.
 **Optimized Resource Utilization:** Leveraging the pay-as-you-go model of Power Virtual Serveroptimized operational costs.

**Operational Efficiency:**
 **Minimal Downtime:** The streamlined migration process ensured minimal disruption to manufacturing operations.
 **Enhanced Performance:** The new cloud environment provided better performance and scalability to meet growing data needs.

**Data Integrity and Security:**
 **Accurate Replication:** The use of mksysb and savevg ensured accurate replication of the entire system and all data.
 **Secure Transfer:** Data was securely transferred and protected during the migration process.

By using mksysb and savevg, XYZ Corporation successfully migrated their AIX workloads to IBM Power Virtual Server, achieving a seamless transition with significant cost savings and improved operational efficiency.


## Migration IBM i to IBM Cloud
{: #4-migration-ibmi}

**IBM i Decision Tree**

![IBMi migration decision tree](/images/ibmimigration.svg "Reference Summary"){: caption="{{site.data.keyword.powerSysFull}} IBMi decision tree" caption-side="bottom"}{: external download="ibmimigration.svg"}

There are a number of options for migrating IBMi series from on premise to Power Virtual Server on IBM cloud
* FalconStorVTL
* Operating System level backup and restore
* Host/Operating System mirroring using PowerHA with geographic mirroring
* Application level replication for example  DB2, Oracle, SAP
* Logical replication using 3rd party software for example Mimix

**Backup and Migration using FalconStor VTL**

For images over 2 TB, it is recommended that organizations utilize FalconStor Storsafe VTL appliances to deduplicate and minimize the data transfer to the cloud. Images less than 2 TB can be transferred to IBM Cloud Object Storage using IBM Backup, Recovery, and Media Services (BRMS) and IBM Cloud Storage Solution (ICC)  IBM Cloud Direct Link is the preferred option, as it seamlessly connects on-premises resources to IBM Cloud, and provides a consistent, high-throughput connectivity without using the public internet.

**Operating System level backup and restore**
Both the SAVSYS and GO SAVE commands can be used to backup the IBM i operating system
The GO SAVE command includes multiple options, three of which are discussed in this paper:

*	Menu option 21: makes a backup of the entire system
*	Menu option 22: makes a backup of all system data
*	Menu option 23: makes a backup of all user data

Geographic mirroring can be utilized to migrate a host and operating system from an on-premises location to Power Virtual Server in IBM Cloud. Geographic mirroring occurs when all data in one environment is mirrored to a second location.  There is both a synchronous and asynchronous version of geographic mirroring. Synchronous geographic mirroring over a distance may impact application performance due to communication latency.

![Geographic mirror](/images/geomirror.svg "Reference Summary"){: caption="{{site.data.keyword.powerSysFull}} Geopgraphic Mirror" caption-side="bottom"}{: external download="geomirror.svg"}

**Application level replication**
A number of applications commonly deployed on Power have built in replication capabilities:
* [DB2 HADR](https://www.ibm.com/docs/en/db2/11.5?topic=server-high-availability-disaster-recovery-hadr){: external}
* [Oracle Dataguard](https://www.oracle.com/ie/database/data-guard/){: external}
* [SAP HANA on prem to cloud](https://help.sap.com/docs/hana-cloud/sap-hana-cloud-migration-guide/migrate-sap-hana-on-premise-database-to-sap-hana-cloud){: external}

Logical replication using 3rd party software
  * [Assure MIMIX (from Precisely)](https://www.precisely.com/product/precisely-assure/assure-mimix){: external}: A high availability (HA) and disaster recovery (DR) solution for IBM i, but it’s also widely used to support migrations — especially when businesses want minimal or near-zero downtime.
  * [Rocket iCluster](https://www.rocketsoftware.com/products/rocket-icluster/resources){: external}: Logical replication software that runs on Power systems running IBM i. iCluster uses journaling to provide high availability and disaster recovery for business applications and enables almost continuous access through real-time monitoring, notifying, and self-correcting replication.
RobotHA:


Case studies



**Case Study: Migrating IBM i Workloads from On-Premises to IBM Power Virtual Server Using FalconStor VTL**

**Client Overview:** LMN Healthcare, a medium-sized healthcare provider, relies on IBM i systems for critical applications such as patient management, billing, and electronic health records. To enhance scalability, performance, and reduce operational costs, LMN Healthcare decided to migrate their IBM i workloads from their on-premises data center to IBM Power Virtual Server (PowerVS).

**Challenges:**
 **Regulatory Compliance:** The healthcare industry has strict data protection regulations. Ensuring compliance during the migration was crucial.
 **Data Volume:** The sheer volume of patient records and historical data posed a significant challenge for migration.
 **Legacy Systems Integration:** Some older systems needed to be integrated seamlessly with the new cloud environment to maintain operational continuity.

**Solution:** To address these challenges, LMN Healthcare implemented a migration strategy leveraging FalconStor's StorSafe Virtual Tape Library (VTL) to ensure an efficient, secure, and seamless transition to PowerVS.

**Migration Process:**
1. **Preparation:**
    * **Assessment:** Conducted a thorough assessment of the existing IBM i environment, identifying all critical applications, data, and dependencies.
    * **Set Up PowerVS:** Provisioned the target environment in IBM PowerVS, ensuring it was configured to match the specifications of the on-premises IBM i systems.
2. **Creating Backups:**
    * **Virtual Tape Creation:** Utilized FalconStor's StorSafe VTL to create virtual tape backups of the IBM i systems. This included full system backups and incremental backups of critical data.
    * **Deduplication:** FalconStor's built-in deduplication technology minimized the amount of data transferred, reducing both time and resource requirements.
3. **Transferring Backups:**
    * **Secure Transfer:** Transferred the virtual tape backups to IBM Cloud Object Storage using secure transfer methods to ensure data security and integrity. FalconStor's VTL ensured efficient and secure data transfer.
4. **Restoring Backups on PowerVS:**
    * **Provisioning VSI:** Created new Virtual Server Instances (VSIs) in Power Virtual Server to replicate the on-premises IBM i environment.
    * **Restoration Process:** Used the virtual tape backups to restore the IBM i systems on the new VSIs, re-establishing the operating system, applications, and data.
5. **Testing and Validation:**
    * **System Verification:** Verified that the restored environment in Power Virtual Server matched the on-premises setup, with all configurations and data intact.
    * **Application Testing:** Conducted extensive testing of critical healthcare applications to ensure functionality and performance in the new environment.
6. **Final Cutover:**
    * **Data Synchronization:** Ensured the latest data changes were synchronized between the on-premises system and PowerVS.
    * **Production Cutover:** Transitioned production operations to the new Power Virtual Server environment, minimizing downtime and ensuring continuous availability.
7. **Post-Migration Monitoring:**
    * **Continuous Monitoring:** Implemented monitoring tools to ensure the new environment operated smoothly and addressed any issues promptly.
    *	**Ongoing Optimization:** Continued to optimize performance and scalability to meet future business needs.

**Results:**
**Cost Savings:**
 * Reduced Infrastructure Costs: By migrating to PowerVS, LMN Healthcare significantly reduced the costs associated with maintaining and upgrading on-premises hardware.
 * Optimized Resource Utilization: Leveraged the pay-as-you-go model of Power Virtual Serverto optimize operational costs and resource utilization.

**Operational Efficiency:**
 * **Minimal Downtime:** The migration process was executed with minimal downtime, ensuring continuous availability of healthcare services.
 * **Enhanced Performance:** The new Power Virtual Serverenvironment provided improved performance and scalability to meet the growing demands of healthcare operations.

**Data Integrity and Security:**
 * **Accurate Replication:** FalconStor's VTL ensured accurate replication of the entire system and all data, maintaining data integrity throughout the migration process.
 * **Secure Transfer:** Data was securely transferred and protected throughout the migration process.

By leveraging FalconStor's StorSafe VTL, LMN Healthcare successfully migrated their IBM i workloads to IBM Power Virtual Server. The migration resulted in significant cost savings, enhanced performance, and improved operational efficiency, ensuring a seamless and reliable transition to the cloud.

**Overview of Performance Metrics and Their Importance in Migrations**

When planning migrations, understanding key performance metrics is crucial for making informed decisions and ensuring a smooth transition. Three primary metrics used to evaluate the performance of IBM systems are rPerf (Relative Performance), SPECjbb2015 (Standard Performance Evaluation Corporation Java Business Benchmark 2015), and CPW (Commercial Processing Workload). Each of these metrics serves a specific purpose, helping to compare system capabilities, plan capacities, and ensure that new systems can handle existing workloads efficiently.

**RPerf** is a benchmark used to estimate the performance of IBM Power Systems servers relative to a baseline system. This metric allows for straightforward comparison between different systems, ensuring the new system can manage current workloads during migrations. You can find the latest IBM Power Performance Report, which includes rPerf values, on the IBM website. Here is the direct link to the most recent report:  [IBM Power Performance Report](https://www.ibm.com/downloads/documents/us-en/10c31775c5d40fed){: external}

**SPECjbb2015** evaluates the performance of server-side Java applications, particularly useful for Linux workloads on Power Systems. It measures throughput and response times, providing valuable insights into how well a system can handle Java-based applications, which is critical for capacity planning and system selection.

**CPW** measures the processing power of IBM i systems in terms of commercial transactions per second. This metric is essential for assessing the capacity needed for IBM i workloads, ensuring the target system can meet the expected load and future demands.

These metrics are vital in migrations as they offer standardized benchmarks to compare system performance, aiding in capacity planning, cost-benefit analysis, and risk mitigation. They ensure the new system meets performance requirements, reducing downtime and maintaining operational efficiency.



## Summary
{: #5-summary}

Migrating IBM Power workloads to IBM Power Virtual Server on IBM Cloud enables organizations to overcome the limitations of traditional on-prem infrastructure by gaining scalability, performance, and cost-efficiency. With multiple migration strategies—ranging from native backup and restore to advanced real-time replication—businesses can choose the approach that best fits their environment, downtime tolerance, and goals. IBM Power Virtual Serveroffers a secure, flexible, and familiar platform that simplifies cloud adoption while maintaining workload continuity. By leveraging the tools, services, and best practices outlined in this white paper, organizations can execute a smooth, low-risk transition to the cloud and position themselves for future growth.

## References
{: #6-references}

content
