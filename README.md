# 2110837746_Maria_Heinrich

### Conversion Use Case
To evaluate the implementation of currency conversion in a cloud-native analytics platform, a realistic dataset was constructed, simulating accounting transactions across multiple currencies and time periods. The use case reflects a common enterprise requirement: converting local transaction values into a standardized reporting currency (EUR) at the line-item level, using daily historical exchange rates.

### Scenario Definition
The selected scenario mimics a global enterprise operating in serveral countries with more 15 currencies. Each legal entity conducts financial transactions in its lo-cal currency. For unified financial reporting, all transactions must be converted to euros (EUR) using official daily exchange rates. This mirrors challenges previously addressed using SSIS-based ETL pipelines and OLAP cubes in traditional data warehouses, which must now be replaced with scalable, cloud-native alternatives.

Key challenges addressed in the scenario include:
•	Accurate date-aligned matching of transaction and exchange rate records
•	Handling of missing or delayed exchange rate entries (e.g., weekends, public holidays)
•	Support for batch processing at scale using modern Python and Spark-based tools
•	Export of enriched accounting data for downstream Power BI reporting   


Azure Databricks was selected as one of the two cloud environments for implementing the currency conversion use case due to its robust support for distributed data processing, seamless integration with the Azure ecosystem, and scalable architec-ture built on Apache Spark. This platform offers an ideal foundation for performing large-scale transformations and exploratory analytics in Python and SQL, while supporting advanced orchestration and security features needed for enterprise-grade development.

![Databricks](https://github.com/user-attachments/assets/368f7d62-5b75-4ab3-aeba-89246238aa25)
![Databricks_Scheduler](https://github.com/user-attachments/assets/ed4d33f5-8e2b-437d-8a33-37a411718c24)
![Databricks_Scheduler_01](https://github.com/user-attachments/assets/475232b8-52f6-4ccd-a08f-f001648a85cf)
![250521_Databricks_Abrechnung](https://github.com/user-attachments/assets/6e82cb0c-f579-4865-a599-1ab1130a4b24)

[Azure Databricks Pricing](https://azure.microsoft.com/en-us/pricing/details/databricks/)


Microsoft Fabric was selected as the second platform for implementing the currency conversion use case, offering a fully managed Software-as-a-Service (SaaS) approach to analytics. In contrast to the infrastructure-as-a-service (IaaS) model used in Azure Databricks, Fabric abstracts compute and storage provisioning, allowing developers to focus solely on data engineering logic, business rules, and orchestration workflows.

A dedicated Microsoft Fabric workspace was provisioned using the trial license tier. The setup details are summarized below:   
•	License Type: Trial   
•	License Capacity: Trial-20240905T162916Z-xxxxxxxxx   
•	SKU: FT1   
•	Region: North Europe   

Although categorized under the FT1 (Trial) SKU, the workspace internally allocated 64 Capacity Units (CU) - equivalent to the F64 SKU in production-grade deployments. This configuration enabled the execution of large-scale transformations, notebook operations, and pipeline scheduling without incurring additional cost during the evaluation period.


![Fabric](https://github.com/user-attachments/assets/6202799e-20fd-4b6e-a60a-71a81c08661b)


[Mircosoft Fabric Pricing](https://azure.microsoft.com/de-de/pricing/details/microsoft-fabric/)
