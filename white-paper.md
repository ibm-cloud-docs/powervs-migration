---

copyright:
  years: 2025
lastupdated: "2025-03-28"

keywords:

subcollection: powervs-migration

---

{{site.data.keyword.attribute-definition-list}}


# Migrating to {{site.data.keyword.powerSys_notm}} on {{site.data.keyword.cloud_notm}}
{: #white-paper}

This white paper describes the business challenges with on-premises and colocated Power workloads and offers prescriptive solutions for migrating to {{site.data.keyword.IBM}} {{site.data.keyword.powerSysFull}}. It covers key design considerations and migration strategies to guide your transition with actionable steps.
{: shortdesc}

Organizations are turning to cloud solutions to enhance scalability, reduce costs, and improve flexibility. {{site.data.keyword.IBM}} {{site.data.keyword.powerSys_notm}} offers a robust platform for running {{site.data.keyword.IBM}} AIX and {{site.data.keyword.IBM}} i workloads with the benefits of cloud infrastructure.

## On-premises challenges
{: #challenges}

Businesses are moving away from traditional data centers as the cost and complexity of maintaining on-premises or colocation facilities drive the need for more flexible, cost-effective solutions. Common challenges include the following points:

High costs of operation
- Capital expenditures (CapEx): On-premises data centers require significant upfront investments in hardware, software, and infrastructure.
- Operational expenditures (OpEx): Costs for maintenance, power, cooling, and staffing add up, often exceeding budgets.
- Scaling costs: Scaling on-premises infrastructure is costly and time-consuming compared to cloud solutions.

Limited scalability and agility
- Demand variability: On-premises systems are not easily scalable to meet fluctuating demands, leading to over-provisioning or underutilization of resources.
- Rapid Innovation: Businesses need to innovate quickly, but legacy systems in data centers can’t keep pace with emerging technologies.

Complexity of maintenance
- Infrastructure upkeep: Regular upgrades and replacements for hardware and software create operational burdens.
- Specialized skills required: IT teams need expertise in various aspects, including networking, storage, and security, which can be hard to maintain.

Security and compliance
- Cybersecurity risks: Managing security for on-premises systems is resource-intensive and requires continuous vigilance.
- Regulatory compliance: Adhering to evolving data protection regulations, like GDPR and HIPAA, is complex and costly for in-house systems.

Business continuity risks
- Disaster recovery: Maintaining robust disaster recovery and backup systems on-premises is challenging and expensive.
- Downtime risks: Power outages, hardware failures, and other issues can lead to costly downtime.

These factors affect clients that manage [{{site.data.keyword.IBM}} Power](https://www.ibm.com/power) servers in on-premises data centers, and one solution is migrating to {{site.data.keyword.powerSys_notm}} on {{site.data.keyword.cloud_notm}}.

## Why {{site.data.keyword.powerSys_notm}} on {{site.data.keyword.cloud_notm}}?
{: #why-powervs}

{{site.data.keyword.powerSys_notm}} is an {{site.data.keyword.IBM}} Power server offering. Clients can use {{site.data.keyword.powerSys_notm}} to deploy a virtual server, also known as a logical partition (LPAR), in a matter of minutes. You can provision flexible, secure, and scalable compute capacity for Power enterprise workloads on {{site.data.keyword.powerSys_notm}} in the {{site.data.keyword.cloud_notm}} console.

{{site.data.keyword.IBM}} also offers {{site.data.keyword.powerSys_notm}} on-premises through [{{site.data.keyword.powerSys_notm}} Private Cloud](/docs/power-iaas?topic=power-iaas-getting-started){: external}, which enables clients to benefit from cloud capabilities and cost models, but keep infrastructure onsite. However, this article focuses on {{site.data.keyword.powerSys_notm}} on {{site.data.keyword.cloud_notm}}.
{: note}

Review the following benefits of using {{site.data.keyword.powerSys_notm}} on {{site.data.keyword.cloud_notm}}.

Performance with latest {{site.data.keyword.IBM}} POWER processor
:   Client can provision {{site.data.keyword.powerSys_notm}} in {{site.data.keyword.IBM}} data centers in a matter of minutes, and take advantage of the latest POWER processor.

   {{site.data.keyword.IBM}} makes constant innovations on POWER processors, and pushes out a newer version of {{site.data.keyword.IBM}} Power every 2 or 3 years. It is built to meet today’s challenges with new levels of performance, core-to-cloud data protection, and streamlined automation and insights. Power Systems have more crypto accelerators per core, provides full memory encryption at scale, and support quantum-safe cryptography. Power10 can accelerate AI training and inferencing with its built-in Matrix Math Accelerators (MMA) without requiring external accelerators, such as GPUs, for running statistical machine learning and inferencing (scoring) workloads. It also offers memory sharing among Power Servers to handle AI models at scale, which drives business demand for a flexible and scalable cloud compute consumption model.

Flexibility and scalability
:   {{site.data.keyword.powerSys_notm}} is available across 10 {{site.data.keyword.cloud_notm}} multi-zone regions across Americas, Europe, and APAC and 22 data centers, and the number is growing. Client can deploy {{site.data.keyword.powerSys_notm}} in {{site.data.keyword.IBM}} data centers around the globe, with scalable resources adjustable based on demand. Seamlessly scale resources up or down based on workload demands and adapt to changing business needs with cloud-based infrastructure.

Cost-effective OpEx model
:   With a flexible pay-as-you-go model, the client pays only for what they use. Pay-as-you-go applies not only to the {{site.data.keyword.powerSys_notm}} compute, but also to the storage. You can move from expensive on-premises storage to scalable cloud storage models. You can replace Tape with {{site.data.keyword.cos_full_notm}}, SAN with cloud block and file storage, or use vSAN in the [VMware Software Defined Data Center (SDDC)](/docs/vmware?topic=vmware-vmware-sddc-on-ibm-cloud) model on cloud bare metal servers.

Smooth migration to the cloud
:   {{site.data.keyword.powerSys_notm}} has the same architecture in a cloud environment as {{site.data.keyword.IBM}} Power on-premises. It supports AIX, {{site.data.keyword.IBM}} i, Linux, and Red Hat OpenShift, and is certified for SAP and Oracle workloads, allowing a smooth migration for businesses already by using {{site.data.keyword.IBM}} Power Systems to cloud.

Improved platform availability
:   The accelerated shift to a digital economy, partly due to the Covid pandemic, along with increased business demand for higher availability of production-critical applications, requires greater platform availability of 99.99+%. For more information about platform availability, see the [{{site.data.keyword.cloud_notm}} service level objectives](/docs/resiliency?topic=resiliency-slo).

Security
:  Security is a critical business requirement to protect intellectual capital and ensure the integrity of software supply chains. With the growing number and cost of cyberattacks, organizations must adopt a disciplined approach to system and data security. End-to-end encryption is essential for safeguarding business data, and effective encryption key management plays a vital role. On {{site.data.keyword.cloud_notm}}, businesses have the flexibility to use {{site.data.keyword.IBM}}-provided encryption keys or bring their own keys (BYOK). Using {{site.data.keyword.keymanagementserviceshort}} (Key Protect), {{site.data.keyword.cloud_notm}} offers a centralized, secure, and scalable key management solution that integrates with cloud services and applications. It enables lifecycle management of encryption keys without the complexity of hardware-based security modules. The increasing risk of ransomware and other cyberthreats reinforces the need for a minimum viable company (MVC) platform that is built with security and resilience at its core.

Sustainability
:   {{site.data.keyword.IBM}} is committed to driving sustainability through energy-efficient infrastructure and responsible cloud operations. {{site.data.keyword.powerSys_notm}} helps organizations reduce their carbon footprint by shifting workloads to shared, energy-optimized {{site.data.keyword.cloud_notm}} data centers, which are designed for high efficiency and sustainability at scale. By moving away from energy-intensive on-premises infrastructure to a cloud-based OpEx model, you can better align with ESG goals and reduce overall power consumption. {{site.data.keyword.IBM}}’s focus on processor efficiency, like with Power10, means that clients benefit from greater performance-per-watt and greener IT operations.

Disaster recovery
:   {{site.data.keyword.powerSys_notm}} offers a resilient and scalable platform to protect your critical workloads with advanced backup and disaster recovery solutions. For more information, see [Understanding disaster recovery](/docs/resiliency?topic=resiliency-understanding-dr) and [High availability and disaster recovery for {{site.data.keyword.powerSys_notm}}](/docs/power-iaas?topic=power-iaas-ha-dr).

IT agility is key to business success today. Businesses need scalable and elastic environments, which cloud platforms enable. {{site.data.keyword.cloud_notm}} provides automation for the {{site.data.keyword.powerSys_notm}} platform, and integration with other {{site.data.keyword.cloud_notm}} services provide insights to cloud usage, facilitating auditing and control.

## Use cases for {{site.data.keyword.powerSys_notm}} on {{site.data.keyword.cloud_notm}}
{: #usecases}

Review common use cases for {{site.data.keyword.powerSys_notm}}:

Data center optimization and operational excellence
:   Companies adopt cloud strategies to address the challenges of traditional on-premises data centers. By using solutions like {{site.data.keyword.powerSys_notm}} to exit or optimize data centers, businesses can lift and shift critical applications to the same stack. This way, you reduce operational costs, improve service quality with faster response times, and benefit from flexible pay-as-you-go billing. This approach supports growth and global expansion while ensuring scalability, reliability, and performance for critical workloads.

Business continuity planning
:   Companies can enhance resilience by backing up their data to the cloud, helping ensure that business have reliable failover solutions like backup, high availability, and disaster recovery. {{site.data.keyword.powerSys_notm}} helps reduce capital expenditure, simplify planning, and eliminate the need to maintain excess capacity, all while providing scalable and dependable protection against unexpected disruptions.

Modernization
:   {{site.data.keyword.powerSys_notm}} resources reside in {{site.data.keyword.cloud_notm}} data centers with dedicated networking and storage area network-attached Fibre Channel storage. The internal networks are fenced but offer connectivity options to {{site.data.keyword.cloud_notm}} infrastructure or private cloud environments. This infrastructure design enables {{site.data.keyword.powerSys_notm}} to maintain key enterprise software certification and support as the {{site.data.keyword.powerSys_notm}} architecture is identical to certified private cloud infrastructure. It also enables {{site.data.keyword.powerSys_notm}} to connect to over 190 {{site.data.keyword.cloud_notm}} services seamlessly. Companies can use cloud services to modernize applications by enhancing scalability, integrating advanced tools, and enabling seamless updates. This approach supports faster innovation, improves performance, and ensures that your applications are equipped to meet evolving business demands.

## Migration process
{: #migration-process}

Consider different factors before choosing the right migration strategy:

* Environment - Is it a dev or test non-production environment or production environment?
* Allowable downtime - How much downtime is allowed to safely complete the migration?
* Workloads – Is it OS level backup, application, or database backup?
* Data size - Is the data size small (< 2TB), medium (3-10TB), or large (>10TB)?
* Network options - Does the backup need to use public internet with VPN, is Direct Link available? What is the network bandwidth?
* Skills – Do you prefer a managed solution or does your team have the skills to complere the migration?
* Cost – Do you need to use existing licenses or OS commands, or are you open to using new software and tools?

Depending on your organization's skillset, you might need assistance in your migration from on-premises to cloud. Contact the [IBM Technology Expert Labs](https://www.ibm.com/products/expertlabs) to connect with client engineering.
{: tip}

If you want to manage the migration, review the general process:

1. Planning. When you migrate workloads to cloud, especially from older generation of Power Systems to newer generations, system configuration planning is important. For more information on migration planning, see [Planning a workload migration to IBM® Power® Virtual Server](https://www.ibm.com/docs/en/power-virtual-server?topic=strategies-planning-workload-migration-power-virtual-server) and [Hints and Tips](https://www.ibm.com/downloads/documents/us-en/10a99803f32fd7bd) for migration.
1. Network setup. Choose the network setup for the migration. Direct Link is preferred, especially for large data size. For smaller data size, use VPN.
1. Infrastructure setup. Provision the cloud infrastructure as the target of the workload migration.
   * Use deployable architectures. {{site.data.keyword.cloud_notm}} deployable architecture is cloud automation for deploying a common architectural pattern that combines one or more cloud resources. It offers a modular, flexible foundation for businesses to build, deploy, and manage applications securely in the cloud. {{site.data.keyword.cloud_notm}} offers a few different flavors of [deployable architectures](https://cloud.ibm.com/docs/powervs-vpc?topic=powervs-vpc-automation-solution-overview) that provide an automated deployment method to create an isolated {{site.data.keyword.powerSys_notm}} workspace and connect it with {{site.data.keyword.cloud_notm}} services and public internet.
   * For clients in regulated industries, follow the [{{site.data.keyword.cloud_notm}} Framework for Financial Services best practices](/docs/framework-financial-services?topic=framework-financial-services-best-practices).
1.  Workload migration. Your workload migration options depend on your OS, applications, and databases. Consider the various factors mentioned previously.
1.  Workload resiliency. {{site.data.keyword.cloud_notm}} offers various services to enhance resiliency.
   * Choose a strategy for backup ([AIX](/docs/power-iaas?topic=power-iaas-backup-strategies), [IBM i](/docs/power-iaas?topic=power-iaas-backup-ibmi)) and [High Availability and Disaster Recovery for {{site.data.keyword.powerSys_notm}}](/docs/power-iaas?topic=power-iaas-ha-dr).
1. Security and compliance. {{site.data.keyword.powerSys_notm}} provides programs and certifications that help you establish and strengthen compliance for a wide range of internationally recognized standards. For more information, see [Compliance certifications](/docs/power-iaas?topic=power-iaas-compliances-list).

Review the following scenarios you encounter in the migration process and the recommended approach.

| Scenario | Recommended approach |
|----------|----------------------|
| **Secure, high-bandwidth transfer** | Use **Direct Link** when possible. If unavailable, use VPN as an alternative. |
| **Small data migrations (OS-level transfers)** | Use OS-native backup and restore tools. |
| **Small data transfers** | Cloud Object Storage (COS) can be suitable. Use **Aspera** for faster, more efficient transfers when available. |
| **Large data transfers** | Direct network transfers to {{site.data.keyword.powerSys_notm}} are preferred. Use Aspera when possible. |
| **Very large data migrations** | Use deduplication tools, like FalconStor StorSafe VTL, to reduce data transfer volume. |
| **Zero-downtime environments** | Combine backup and restore for initial seeding, followed by replication, to maintain data synchronization. |
{: caption="Markdown coding for tables" caption-side="bottom"}

## Using performance metrics to plan a migration
{: #migration-perfmetrics}

When you plan for migrations, understanding key performance metrics is crucial for making informed decisions for a smooth migration. Three primary metrics that you can use to evaluate the performance of {{site.data.keyword.IBM}} systems are Relative Performance (rPerf), Standard Performance Evaluation Corporation Java Business Benchmark 2015 (SPECjbb2015), and Commercial Processing Workload (CPW). These metrics help you compare your current system to future options, estimate performance needs, and ensure that the new environment can handle your workloads.

rPerf
:   rPerf is a benchmark that is used to estimate the performance of {{site.data.keyword.IBM}} Power Systems servers relative to a baseline system. This metric allows for straightforward comparison between different systems, helping to ensure that the new system can manage current workloads during migrations. You can find the latest {{site.data.keyword.IBM}} Power rPerf values in the [{{site.data.keyword.IBM}} Power Performance Report](https://www.ibm.com/downloads/documents/us-en/10c31775c5d40fed){: external}.

SPECjbb2015
:   SPECjbb2015 evaluates the performance of server-side Java applications, which is useful for Linux workloads on Power Systems. It measures throughput and response times, providing valuable insights into how well a system can handle Java-based applications, which is critical for capacity planning and system selection.

CPW
:   CPW measures the processing power of {{site.data.keyword.IBM}} i systems in terms of commercial transactions per second. This metric is essential for assessing the capacity that is needed for {{site.data.keyword.IBM}} i workloads, which helps you make sure that the target system can meet the expected load and future demands.

These metrics are vital for planing your migrations as they offer standardized benchmarks to compare system performance. They also aid in capacity planning, cost-benefit analysis, and risk mitigation. Use key metrics to make sure that the new system meets performance requirements so that you can reduce downtime and maintain operational efficiency.

## Migrating AIX to {{site.data.keyword.cloud_notm}}
{: #migrate-aix}

Review the AIX decision tree and the migration options in the following sections.

![AIX migration decision tree](/images/aixmigration.svg "Reference Summary"){: caption="{{site.data.keyword.powerSysFull}} AIX decision tree" caption-side="bottom"}{: external download="aixmigration.svg"}

### Backup and restore by using mksysb images
{: #backup-mksysb}

Migrating AIX workloads to {{site.data.keyword.powerSys_notm}} by using the mksysb method offers a reliable and efficient way to ensure data consistency and system integrity. This method uses the well-established [`mksysb` command](https://www.ibm.com/docs/fi/aix/7.1?topic=m-mksysb-command), which creates comprehensive backups of the entire system, including the operating system, configurations, and data. The process minimizes downtime and disruption, allowing businesses to achieve a smooth migration from on-premises to cloud infrastructure. The mksysb method is highly customizable. Organizations can tailor backups to specific needs and optimize the use of cloud resources.

Security and performance are also key benefits of migrating to {{site.data.keyword.powerSys_notm}} by using the mksysb method. Data encryption safeguards sensitive information both in transit and at rest, while isolated environments prevent unauthorized access. {{site.data.keyword.powerSys_notm}} uses {{site.data.keyword.IBM}} Power Systems' high-performance computing capabilities, helping ensure efficient operation of AIX workloads in the cloud. Enhanced networking features, including low-latency connections and high-speed data transfer, improve overall performance. Robust disaster recovery solutions and simplified management further ensure data protection, continuity, and ease of oversight, making this method a secure and effective choice for migrating AIX workloads to {{site.data.keyword.powerSys_notm}}.

In this option, the existing AIX LPAR is backed up by using the built-in `mksysb` command. It might also require using `savevg` for LPARs with separate volume groups defined.

Consider this option for businesses that want an identical system that is migrated to {{site.data.keyword.cloud_notm}}. It has the lowest cost and shortest time frame to migrate.

Migrating AIX workloads to {{site.data.keyword.powerSys_notm}} by using `mksysb` and `savevg` provides a comprehensive approach that efficiently transfers all system and data elements to the cloud. This method uses AIX tools to create and transfer backups of the entire system, making it a reliable and well-structured migration strategy. By using these built-in commands, the migration process is streamlined, cost-effective, and time-efficient, with minimal downtime and disruption to business operations.

1. Create a `mksysb` backup on your on-premises AIX system to capture the entire root volume group (`rootvg`), including the operating system, configurations, and root-level data.
1. Transfer this backup to {{site.data.keyword.powerSys_notm}}, where it is restored to set up the base system environment.
1. Use the `savevg` command to back up other volume groups beyond `rootvg`, capturing their respective data.
1. Transfer the backups to {{site.data.keyword.powerSys_notm}}.
1. Restore by using the `restvg` command to check that all data and configurations are replicated accurately in the cloud environment.

This method is cost-effective because it uses existing AIX tools and eliminates the need for expensive third-party migration software. The `mksysb` and `savevg` commands are built into AIX, so you incur no licensing costs. Also, using cloud storage for transferring backups helps avoid the costs that are associated with physical media and dedicated migration hardware. The pay-as-you-go model of {{site.data.keyword.powerSys_notm}} further reduces capital expenditures, optimizing overall migration costs.

In terms of time efficiency, this approach minimizes downtime through a streamlined backup and restore process. The `mksysb` command creates a comprehensive system backup in one go, reducing the complexity and time required for data transfer. Similarly, the `savevg` command ensures that additional volume group data is backed up efficiently. Transferring these backups through cloud storage expedites the migration process, ensuring a quick and seamless transition. This approach ensures business continuity with minimal disruption, making it a practical and efficient solution for migrating AIX workloads to {{site.data.keyword.powerSys_notm}}.

Other benefits include the following points:
- Comprehensive backup and recovery: Ensures full system protection by backing up the entire root volume group (rootvg) and extra volume groups, capturing all necessary data and configurations.
- Cost-effectiveness: Uses built-in AIX tools with no additional software costs and takes advantage of cloud storage and the pay-as-you-go pricing model of {{site.data.keyword.powerSys_notm}} to reduce overall costs.
- Time efficiency: Streamlines the migration process with comprehensive system backups and efficient data transfer, minimizing downtime and ensuring a quick transition.
- Flexibility and scalability: Offers tailored backups for specific system components and scalable resources to meet changing workload demands, optimizing the migration process.
- Enhanced data integrity and security: Maintains data integrity with accurate replication of the entire system and secure data transfer by using cloud storage.

### Host and OS mirroring by using Geographic Logical Volume Manager (GLVM)
{: #host-GLVM}

Migrating AIX workloads to {{site.data.keyword.powerSys_notm}} by using Host and OS system mirroring with Geographic Logical Volume Manager (GLVM) helps ensure continuous data protection and high availability. GLVM replicates data at the logical volume level between on-premises systems and {{site.data.keyword.powerSys_notm}}, minimizing downtime and maintaining business continuity. PowerHA SystemMirror enhances this setup by automating management and monitoring. This method uses {{site.data.keyword.powerSys_notm}}'s scalable and high-performance infrastructure, providing efficient data replication and resource optimization while offering robust security through data encryption and isolated environments.

This approach is cost-efficient, reduces infrastructure costs through a pay-as-you-go model and optimizes resource use. It provides robust disaster recovery solutions and ensures compliance with data protection regulations. The centralized control and simplified management that is offered by {{site.data.keyword.powerSys_notm}}, combined with the automated processes of PowerHA SystemMirror, make the migration process streamlined and reliable. This ensures that businesses can efficiently move their AIX workloads to the cloud, maximizing the benefits of cloud infrastructure while minimizing risks and costs.

### Database replication
{: #db-replication}

Migrating databases to {{site.data.keyword.powerSys_notm}} by using database replication offers the advantage of maintaining real-time synchronization between your on-premises database and the cloud environment. This method can offer minimal downtime and disruption to your business operations. By replicating data at the database level, any changes that are made to the source database are instantly reflected in the target environment, which helps maintain data consistency and integrity throughout the migration. This approach is beneficial for businesses that require high availability and continuous access to their databases, as it minimizes the risks that are associated with data migration and ensures a smooth handover.

The scalability and performance capabilities of {{site.data.keyword.powerSys_notm}} allow optimization of resource utilization and adaptability to fluctuating workload demands. {{site.data.keyword.powerSys_notm}} offers enhanced security features, including data encryption and isolated environments, which safeguard sensitive information and ensure compliance with data protection regulations. This method provides a robust disaster recovery solution, enabling quick recovery and continuity if of an on-premises system failure occurs. By using database replication for your migration to {{site.data.keyword.powerSys_notm}}, you can enhance the resilience, flexibility, and overall efficiency of your IT infrastructure, while ensuring that critical business functions remain uninterrupted and secure.

### Third-party replication software
{: #third-party-replication}

Migrating AIX workloads from on-premises to {{site.data.keyword.powerSys_notm}} can be efficiently managed by using various third-party applications. Options such as FalconStor StorSafe VTL, Double-Take® Move™ for AIX, and MIMIX are designed to facilitate seamless migration with minimal downtime and disruption. These tools ensure robust data integrity and continuous availability during the migration process, making them ideal for critical workload transitions. They offer features like high availability, disaster recovery, and flexible data seeding options, which streamline the migration and optimize resource utilization.

Using these third-party solutions, businesses can achieve a smooth migration to {{site.data.keyword.powerSys_notm}} while benefiting from advanced backup and recovery capabilities. FalconStor StorSafe VTL, and Mimix for instance, optimizes the migration by emulating physical tape drives, while MIMIX is known for its near-zero downtime and realistic data testing. Each tool provides unique benefits that are tailored to different migration needs, ensuring data protection and high performance in the cloud environment. By using these applications, organizations can ensure a reliable and efficient migration, enhancing their IT infrastructure's resilience and flexibility.

### AIX migration method limitations
{: #3-3-migration-aix-limitations}

Backup and restore by using mksysb images
:   Migrating to {{site.data.keyword.powerSys_notm}} using a backup and restore approach with `mksysb` is straightforward and cost-effective, but it comes with several limitations. It requires system downtime, as it’s a point-in-time snapshot that doesn’t support incremental changes or live migration. The process only backs up the root volume group (rootvg), so extra data must be handled separately using tools like `savevg`. Post-migration, network, and device configurations often need to be manually adjusted to fit the cloud environment. It’s also less ideal for large systems due to potential performance and transfer bottlenecks, and it lacks the automation and real-time sync capabilities of advanced methods like GLVM or MIMIX. Despite these drawbacks, it’s a solid option for smaller, noncritical workloads where downtime is acceptable.

Host and Operating System Mirroring using GLVM
:   Migrating to {{site.data.keyword.powerSys_notm}} using Host and Operating System Mirroring with GLVM offers high availability and real-time data replication but comes with several limitations. The setup is technically complex and requires expertise in AIX, LVM, and networking. It’s heavily dependent on high-speed, low-latency network connectivity, which can be costly and impact performance over long distances. GLVM replicates at the volume level, lacking application awareness and transaction-level consistency, making it less suitable for workloads that require fine-grained control. It’s also not ideal for small or one-time migrations due to its infrastructure and operational overhead. This method is best suited for environments that demand continuous availability and robust disaster recovery rather than basic workload transfers.

Database replication
:   Migrating AIX workloads to {{site.data.keyword.powerSys_notm}} using database replication is a powerful approach for minimizing downtime and maintaining real-time data consistency. However, it has several important limitations to consider. First, database replication only transfers the data layer, it does not replicate the operating system, middleware, applications, or system configurations. The target environment in {{site.data.keyword.powerSys_notm}} must be manually configured to match the source system, which can add complexity and risk if there are environment-specific dependencies. Also, the replication process often requires compatible database versions and schemas between the source and target, and sometimes, database upgrades might be necessary before replication can begin.

   Setting up replication can also be technically complex, requiring deep knowledge of features like Db2 HADR, Oracle Data Guard, or third-party replication tools. These tools might have licensing costs and require specialized skills to configure and maintain. There’s also a potential performance impact on the source system, particularly in high-transaction environments, as real-time replication uses compute and I/O resources. During the final cutover, ensuring complete data synchronization and avoiding data drift can be challenging, especially if the source database remains active while switching to the target.

   Overall, while database replication is ideal for scenarios where data availability is critical and application layers can be rebuilt or reinstalled separately, it is less suitable for full-stack system migrations or when an identical environment is required in {{site.data.keyword.powerSys_notm}}. Proper planning, testing, and coordination are essential to avoid surprises during migration.

Third-party replication software
:   Migrating AIX workloads to {{site.data.keyword.powerSys_notm}} using third-party tools (like FalconStor, MIMIX, Double-Take) can streamline the process and reduce downtime, but there are important limitations to consider. Licensing and subscription costs for these tools can be significant, especially for small or budget-constrained projects. Setup and configuration often require specialized expertise, and vendors might have differing support models or integration complexity. These tools might introduce compatibility issues with specific AIX versions, storage layouts, or custom configurations. Sometimes, third-party tools add infrastructure costs or require agents that impact performance. Vendor lock-in can be a concern if ongoing replication or HA/DR functions depends on the samfunctionsigration. Finally, while these tools are great for minimizing downtime, they often need careful testing and validation to ensure data consistency and full system functions in the {{site.data.keyword.powerSys_notm}} environment.

## AIX case study
{: #aix-case-study}

Migrating AIX workloads to {{site.data.keyword.powerSys_notm}} with `mksysb` and `savevg`.

**Client overview:** XYZ Corporation, a mid-sized manufacturing company, relies heavily on AIX systems for its critical business operations, including ERP and supply chain management. With growing data needs and an aging on-premises infrastructure, XYZ Corporation decided to migrate their AIX workloads to {{site.data.keyword.powerSys_notm}} to leverage the cloud's scalability, performance, and cost efficiencies.

**Challenges:**
* Aging infrastructure: XYZ Corporation's on-premises hardware was reaching end-of-life, increasing the risk of hardware failures and downtime.
* Data integrity: Ensuring the integrity of critical data during the migration process was paramount.
* Minimal downtime: The manufacturing processes might not afford significant downtime, needing a seamless transition.

**Solution:** To address these challenges, XYZ Corporation chose to use the `mksysb` and `savevg` commands for a comprehensive and efficient migration strategy.

### Migration process
{: #aix-migration-process}

1. Preparation
    * Assessment: Evaluated the current AIX environment, identifying all volume groups and critical data.
    * Set up {{site.data.keyword.powerSys_notm}}: Provisioned the target environment in {{site.data.keyword.powerSys_notm}}, ensuring compatibility with the existing AIX systems.
2. Create backups
    * mksysb backup: Generated a mksysb backup of the root volume group (`rootvg`), capturing the operating system, configurations, and root-level data.
    * savevg backup: Used `savevg` to back up extra volume groups, ensuring that all critical data was included in the backups.
3. Transfer backups
    * Cloud storage: Transferred the mksysb and savevg backup files to {{site.data.keyword.cos_full_notm}}, using secure and reliable transfer methods.
4. Restore backups on {{site.data.keyword.powerSys_notm}}
    * Provision VSI: Created a Virtual Server Instance (VSI) in {{site.data.keyword.powerSys_notm}} to match the source AIX system's specifications.
    * Restore mksysb backup: Used the mksysb backup to restore the rootvg on the new VSI, setting up the base system environment.
    * Restore savevg backups: Applied the restvg command to restore the additional volume groups from the savevg backups, ensuring that all data and configurations were replicated accurately.
5. Testing and validation
    * System verification: Verified that the restored system on {{site.data.keyword.powerSys_notm}} matched the on-premises environment, with all configurations and data intact.
    * Application testing: Conducted thorough testing of critical applications to ensure that they functioned correctly in the new environment.
6. Final cutover
    * Data synchronization: Ensured that the latest data changes were synchronized between the on-premises system and {{site.data.keyword.powerSys_notm}}.
    * Production cutover: Switched production operations to the new environment on {{site.data.keyword.powerSys_notm}}, with minimal disruption to business processes.
7. Post-migration monitoring
    * Continuous monitoring: Implemented monitoring tools to ensure that the new environment operated smoothly and addressed any issues promptly.

![AIX migration diagram that uses mksysb backup and restore method](/images/mksysbmigration.svg "Reference Summary"){: caption="{{site.data.keyword.powerSysFull}} backup and restore migration" caption-side="bottom"}{: external download="mksysbmigration.svg"}

### Results
{: #results}

Cost savings
- Infrastructure: By moving to {{site.data.keyword.powerSys_notm}}, XYZ Corporation reduced the costs that are associated with maintaining and upgrading on-premises hardware.
- Resource usage: Using the pay-as-you-go model of {{site.data.keyword.powerSys_notm}} optimized operational costs.

Operational efficiency
- Downtime: The streamlined migration process ensured minimal disruption to manufacturing operations.
- Performance: The new cloud environment provided better performance and scalability to meet growing data needs.

Data integrity and security
- Replication: The use of mksysb and `savevg` ensured accurate replication of the entire system and all data.
- Data transfer: Data was securely transferred and protected during the migration process.

By using `mksysb` and `savevg`, XYZ Corporation successfully migrated their AIX workloads to {{site.data.keyword.powerSys_notm}}, achieving a seamless transition with significant cost savings and improved operational efficiency.


## Migrating {{site.data.keyword.IBM}} i to {{site.data.keyword.cloud_notm}}
{: #4-migration-ibmi}

Review the {{site.data.keyword.IBM}} i decision tree and the migration options in the following sections.

![IBM i migration decision tree](/images/ibmimigration.svg "Reference Summary"){: caption="{{site.data.keyword.powerSysFull}} IBM i decision tree" caption-side="bottom"}{: external download="ibmimigration.svg"}

There are several options for migrating IBM i series from on-premises to {{site.data.keyword.powerSys_notm}} on {{site.data.keyword.cloud_notm}}
* Operating System level backup and restore
* Host/Operating System mirroring by using PowerHA with geographic mirroring
* FalconStorVTL
* Application level replication, for example,   Db2, Oracle, SAP
* Logical replication by using 3rd-party software, for example,  Mimix

### Backup and migration by using FalconStor VTL
{: #backup-falconstor}

For images over 2 TB, use FalconStor Storsafe VTL appliances to deduplicate and minimize the data transfer to the cloud. Images less than 2 TB can be transferred to {{site.data.keyword.IBM}} {{site.data.keyword.cos_full_notm}} using {{site.data.keyword.IBM}} Backup, Recovery, and Media Services (BRMS) and {{site.data.keyword.cloud_notm}} Storage Solution (ICC) {{site.data.keyword.cloud_notm}} Direct Link is the preferred option, as it seamlessly connects on-premises resources to {{site.data.keyword.cloud_notm}}, and provides a consistent, high-throughput connectivity without using the public internet.

### Operating system-level backup and restore
{: #os-restore}

Both the SAVSYS and GO SAVE commands can be used to backup the {{site.data.keyword.IBM}} i operating system
The GO SAVE command includes multiple options, three of which are discussed in this paper:

*	Menu option 21: makes a backup of the entire system
*	Menu option 22: makes a backup of all system data
*	Menu option 23: makes a backup of all user data

Geographic mirroring can be utilized to migrate a host and operating system from an on-premises location to {{site.data.keyword.powerSys_notm}} in {{site.data.keyword.cloud_notm}}. Geographic mirroring occurs when all data in one environment is mirrored to a second location.  There is both a synchronous and asynchronous version of geographic mirroring. Synchronous geographic mirroring over a distance might impact application performance due to communication latency.

![Geographic mirror](/images/geomirror.svg "Reference Summary"){: caption="{{site.data.keyword.powerSysFull}} Geopgraphic Mirror" caption-side="bottom"}{: external download="geomirror.svg"}

### Application-level replication
{: #app-replication}

Several applications that are commonly deployed on Power have built-in replication capabilities:
* [Db2 HADR](https://www.ibm.com/docs/en/db2/11.5?topic=server-high-availability-disaster-recovery-hadr){: external}
* [Oracle Dataguard](https://www.oracle.com/ie/database/data-guard/){: external}
* [SAP HANA on-premises to cloud](https://help.sap.com/docs/hana-cloud/sap-hana-cloud-migration-guide/migrate-sap-hana-on-premise-database-to-sap-hana-cloud){: external}

Logical replication by using 3rd-party software
   * [Assure MIMIX (from Precisely)](https://www.precisely.com/product/precisely-assure/assure-mimix){: external}: A high availability (HA) and disaster recovery (DR) solution for {{site.data.keyword.IBM}} i, but it’s also widely used to support migrations — especially when businesses want minimal or near-zero downtime.
   * [Rocket iCluster](https://www.rocketsoftware.com/products/rocket-icluster/resources){: external}: Logical replication software that runs on Power Systems running {{site.data.keyword.IBM}} i. iCluster uses journaling to provide high availability and disaster recovery for business applications and enables almost continuous access through real-time monitoring, notifying, and self-correcting replication.
   * [Robot HA](https://www.fortra.com/products/high-availability-software-ibm-i){: external}: A high availability and disaster recovery solution for IBM i that provides real-time data replication and failover capabilities, ensuring business continuity, and it plays a critical role in migration by enabling seamless cutovers to new systems with minimal downtime and data integrity preserved.

### {{site.data.keyword.IBM}} i migration method limitations
{: #migration-ibmi-limitations}

Falconstor VTL
:   Migrating {{site.data.keyword.IBM}} i workloads to {{site.data.keyword.powerSys_notm}} using FalconStor VTL is a reliable method that uses virtual tape backups to simulate traditional tape-based restore processes in the cloud. However, it comes with several limitations. It is a point-in-time backup and restore approach, meaning that it does not support real-time replication, and any changes that are made after the backup must be reapplied manually. This process typically requires planned downtime, making it less suitable for high-availability environments. The migration involves multiple manual steps, including backup creation, data transfer, and system restoration, and might require adjustments to system configurations in {{site.data.keyword.powerSys_notm}}. Setting up FalconStor VTL also requires specialized expertise and proper network connectivity between the on-premises and cloud environments. For large workloads, data transfer times can be significant, even with deduplication. Also, it does not preserve active jobs, sessions, or in-flight data, which might impact business continuity during cutover. While FalconStor VTL is effective for full system migrations, it’s not ideal for environments that need incremental or near-zero downtime migrations.

Operating system-level backup and restore
:   Migrating {{site.data.keyword.IBM}} i workloads to {{site.data.keyword.powerSys_notm}} by using OS-level backup and restore, such as SAVSYS, GO SAVE menu options, or full system save (Option 21), is a traditional and cost-effective approach, but it also has several limitations. This method requires a full system shutdown or restricted state to run a consistent backup, resulting in planned downtime. It captures the system as a snapshot, meaning no real-time synchronization, and any changes after the backup must be reapplied manually. Also, it involves manual configuration steps during the restore process in {{site.data.keyword.powerSys_notm}}, including setting up devices, network configurations, and IPL settings. Large environments might face long backup and restore times, especially if cloud storage or lower-bandwidth networks are used for transfer. The method also does not preserve active sessions or jobs, and doesn’t support automation or rollback features that are typically offered by replication tools. While suitable for smaller or noncritical systems, this approach might fall short for complex, high-availability environments that require minimal disruption and fast recovery.

Application-level replication (Db2, Oracle, SAP)
:   Migrating {{site.data.keyword.IBM}} i workloads to {{site.data.keyword.powerSys_notm}} by using application-level replication, such as Db2 HADR, Oracle Data Guard, or SAP HANA replication, offers targeted data replication with minimal downtime, but it has several limitations. This method replicates only the application data, not the operating system, user configurations, or the broader application environment. As a result, the target system in {{site.data.keyword.powerSys_notm}} must be manually prepared, including OS setup, user provisioning, application installation, and configuration to match the source. It also requires that the replication-capable version of the application is installed and supported in both the source and target environments. Application-level replication typically involves complex setup, licensing, and infrastructure requirements, and might need expert knowledge to manage logs, failovers, and synchronization. Also, this method does not handle nonapplication files (for example, spool files, custom scripts, system objects), so full system functions might work without extra migration steps. While effective for business-critical databases or ERP systems, application-level replication is best used as part of a hybrid migration strategy, not as a complete solution on its own.

Logical replication with third-party software
:   Migrating {{site.data.keyword.IBM}} i workloads to {{site.data.keyword.powerSys_notm}} by using logical replication with third-party software, such as Assure MIMIX, Rocket iCluster, or RobotHA, is a powerful strategy for achieving near-zero downtime, but it has several limitations. First, these tools typically require separate licensing and ongoing costs, which can be significant, especially for small to mid-sized environments. Logical replication is journal-based, meaning that it relies on proper journal configuration and object selection; if not set up correctly, critical objects or data might be missed. These tools replicate libraries, files, configurations, and user profiles, but often exclude some system-level objects like licensed programs or temporary system data. Also, the setup is technically complex and might require specialized expertise in both the software and {{site.data.keyword.IBM}} i internals. Successful failover and cutover require rigorous testing and monitoring, and while rollback is possible, it might not be as simple as with snapshot-based approaches. Finally, logical replication tools often introduce infrastructure costs and require stable, high-performance network connections between the source and target systems. Despite these challenges, this method is ideal for environments that require high availability and minimal disruption during migration.

## {{site.data.keyword.IBM}} i case Study
{: #migration-ibmi}

Migrating on-premises {{site.data.keyword.IBM}} i workloads to {{site.data.keyword.powerSys_notm}} with FalconStor VTL.

**Client overview:** LMN Healthcare, a medium-sized healthcare provider, relies on {{site.data.keyword.IBM}} i systems for critical applications such as patient management, billing, and electronic health records. To enhance scalability, performance, and reduce operational costs, LMN Healthcare decided to migrate their {{site.data.keyword.IBM}} i workloads from their on-premises data center to {{site.data.keyword.powerSys_notm}} (PowerVS).

**Challenges:**
- Regulatory compliance: The healthcare industry has strict data protection regulations. Ensuring that compliance during the migration was crucial.
- Data volume: The sheer volume of patient records and historical data posed a significant challenge for migration.
- Legacy systems integration: Some older systems needed to be integrated seamlessly with the new cloud environment to maintain operational continuity.

**Solution:** To address these challenges, LMN Healthcare implemented a migration strategy using FalconStor's StorSafe Virtual Tape Library (VTL) to ensure an efficient, secure, and seamless transition to {{site.data.keyword.powerSys_notm}}.

### Migration process
{: #process-ibmi}

1. Preparation
    * Assessment: Conducted a thorough assessment of the existing {{site.data.keyword.IBM}} i environment, identifying all critical applications, data, and dependencies.
    * Set up {{site.data.keyword.powerSys_notm}}: Provisioned the target environment in {{site.data.keyword.powerSys_notm}}, ensuring that it was configured to match the specifications of the on-premises {{site.data.keyword.IBM}} i systems.
2. Create backups
    * Virtual Tape creation: Used FalconStor's StorSafe VTL to create virtual tape backups of the {{site.data.keyword.IBM}} i systems. This included full system backups and incremental backups of critical data.
    * Deduplication: FalconStor's built-in deduplication technology minimized the amount of data transferred, reducing both time and resource requirements.
3. Transfer backups
    * Secure transfer: Transferred the virtual tape backups to {{site.data.keyword.IBM}} {{site.data.keyword.cos_full_notm}} using secure transfer methods to ensure data security and integrity. FalconStor's VTL ensured efficient and secure data transfer.
4. Restore backups on {{site.data.keyword.powerSys_notm}}
    * Provision VSI: Created new Virtual Server Instances (VSIs) in {{site.data.keyword.powerSys_notm}} to replicate the on-premises {{site.data.keyword.IBM}} i environment.
    * Restoration: Used the virtual tape backups to restore the {{site.data.keyword.IBM}} i systems on the new VSIs, reestablishing the operating system, applications, and data.
5. Testing and validation
    * System verification: Verified that the restored environment in {{site.data.keyword.powerSys_notm}} matched the on-premises setup, with all configurations and data intact.
    * Application testing: Conducted extensive testing of critical healthcare applications to ensure functions in the new environment.
6. Final cutover
    * Data synchronization: Ensured the latest data changes were synchronized between the on-premises system and {{site.data.keyword.powerSys_notm}}.
    * Production cutover: Transitioned production operations to the new {{site.data.keyword.powerSys_notm}} environment, minimizing downtime and ensuring continuous availability.
7. Post-migration monitoring
    * Continuous monitoring: Implemented monitoring tools to ensure that the new environment operated smoothly and addressed any issues promptly.
    * Ongoing optimization: Continued to optimize performance and scalability to meet future business needs.

### Results
{: #ibmi-results}

Cost saving
* Infrastructure: By migrating to {{site.data.keyword.powerSys_notm}}, LMN Healthcare significantly reduced the costs that are associated with maintaining and upgrading on-premises hardware.
* Resource usage: Used the pay-as-you-go model of {{site.data.keyword.powerSys_notm}} to optimize operational costs and resource utilization.

Operational efficiency
* Downtime: The migration process was run with minimal downtime, ensuring continuous availability of healthcare services.
* Performance: The new {{site.data.keyword.powerSys_notm}} environment provided improved performance and scalability to meet the growing demands of healthcare operations.

Data integrity and security
* Replication: FalconStor's VTL ensured accurate replication of the entire system and all data, maintaining data integrity throughout the migration process.
* Data transfer: Data was securely transferred and protected throughout the migration process.

By using FalconStor's StorSafe VTL, LMN Healthcare successfully migrated their {{site.data.keyword.IBM}} i workloads to {{site.data.keyword.powerSys_notm}}. The migration resulted in significant cost savings, enhanced performance, and improved operational efficiency.

![IBM i migration diagram using FalconStor method](/images/falconstormigration.svg "Reference Summary"){: caption="{{site.data.keyword.powerSysFull}} falconstor migration" caption-side="bottom"}{: external download="falconstormigration.svg"}

## Summary
{: #summary}

Migrating on-premises {{site.data.keyword.IBM}} Power workloads to {{site.data.keyword.powerSys_notm}} on {{site.data.keyword.cloud_notm}} helps organizations overcome the limitations of traditional on-premises infrastructure with cloud scalability, performance, and cost-efficiency. With multiple migration strategies, ranging from backup and restore to advanced real-time replication, you can choose the approach that best fits your environment, downtime tolerance, and goals. {{site.data.keyword.powerSys_notm}} offers a secure, flexible, and familiar platform that simplifies cloud adoption while maintaining workload continuity. By using the tools, services, and best practices that are outlined in this white paper, you can run a smooth, low-risk transition to the cloud and position your organization for future growth.

## References
{: #references}

 * [Planning a workload migration to IBM® Power® Virtual Server](/docs/power-iaas?topic=power-iaas-system-migration){: external}
 * [Migration strategies for AIX](/docs/power-iaas?topic=power-iaas-migration-aix){: external}
 * [Migration strategies for {{site.data.keyword.IBM}} i](/docs/power-iaas?topic=power-iaas-migration-strategies-power){: external}
 * [Additional migration strategies](/docs/power-iaas?topic=power-iaas-additional-migration-strategies-power){: external}
 * [IBM {{site.data.keyword.powerSys_notm}} Guide for IBM AIX and Linux](https://www.redbooks.ibm.com/redpieces/pdfs/sg248512.pdf){: external}
