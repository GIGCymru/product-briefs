# Integration Hub

!!! info
    **Owner**: DHCW Integration Services Team

    **Phase**: Private-Beta

    **Updated**: 2025/06/26

## Summary

NHS Wales requires a modern solution to connect disparate digital health
systems that use incompatible data formats and standards. The Integration Hub
is a cloud-native platform providing robust data validation and transformation
capabilities to enable the seamless and secure exchange of sensitive clinical
information. This new, internally-owned product replaces proprietary systems,
unlocking agility, reducing costs, and ensuring data flows reliably between
internal (NHS Wales) and third-party products to support patient care.

## Vision

To enable clinical data to flow securely and seamlessly between systems,
empowering timely, data-driven decisions and improving patient outcomes.

## Business Problem

Generally integrating products is challenging and time-consuming due to
inconsistent data formats and varying standards across the health ecosystem.
This results in data silos and unreliable data exchange. There is a future
target for products to read and write data to/from the Clinical Data
Repository (CDR), reducing the need for data transformation and exchange.
However, in the interim and for products that are unable or prohibitively
expensive/difficult to enable to follow this pattern, we need a fast,
secure and reliable way to enable integration and data exchange.

There is a solution currently in place that:

* Relies on a third-party vendor product and incurs the associated licence costs.
* Is hosted in a private data centre and requires significant persistent infrastructure.
* Scaling is tied to hardware and licensing limitations.
* Has a GUI based workflow, making automation and codified assurance difficult.
* Requires specialist/propriety product-specific knowledge and skills to work with.
* Lacks the inherent scalability, resilience, and other features of modern Cloud.

## Business Outcomes & Benefits

The expected business outcomes and benefits are:

* Reduced operational costs (e.g. license fees, private data centre overhead.)
* A more predictable and significantly lower long-term cost profile.
* Full ownership and control over code & architecture of a critical piece of infrastructure.
* Unlimited flexibility to build precisely what the business needs.
* Decreased  time required to develop and deploy a new integration, enabling faster delivery of business value.
* Improved reliability from Cloud native services and modern architectural patterns.
* Enhanced business continuity and reduced risk of downtime.
* Natively scalable with cloud infrastructure. Pay-as-you-grow model.
* Enhanced Security through Secure-by-design approaches and security automation.
* A more efficient architecture, leading to reduced carbon footprint associated with the service.

## Users

| Users                  | Needs           |
| ---------------------- | --------------- |
| DHCW Integration Team  | The internal team responsible for building, deploying, and managing integrations. They need a powerful, code-first environment with robust automation to work efficiently. |
| 3rd Party & Internal Devs | Teams (both within NHS Wales and at partner organisations) who need to connect their products to the hub. They require clear documentation, stable APIs/endpoints, and straightforward onboarding processes. |
| DHCW Platform & Security Teams  | The teams that manage the underlying cloud infrastructure and ensure the platform is secure and reliable. |
| Clinical & Administrative Staff | The end-users of the connected systems who indirectly benefit from the timely and accurate availability of data. |
| Information Governance Teams    | Responsible for overseeing the appropriate use and security of patient data. |

## User Outcomes & Benefits

* High-demand, transferable skills and cloud-native development.
* Investment in our team's professional growth and future career opportunities.
* Faster and more consistent development and deployment of new integrations, supported by comprehensive automation.
* Greater agility and flexibility in building and adapting integration solutions to meet evolving needs.
* Improved patient outcomes and timely, data-driven decisions through reliable access to accurate clinical information.
* Enhanced system reliability, resilience, and scalability through a modern, cloud-native architecture.
* Centralised visibility and easier troubleshooting of integration health via comprehensive observability dashboards.
* Stronger assurance of data security, quality, and compliance for sensitive patient information.

## Strategic Alignment

This product is a foundational component for delivering the [DHCW Organisational Strategy 2024-2030](https://dhcw.nhs.wales/about-us/key-documents/strategies/organisational-strategy-2024-2030/),
directly enabling several key missions and principles:

* **Mission 1**: Provide a platform for enabling digital transformation. The Integration
Hub is the core engine for this mission. It directly facilitates the move to a
clean, open, and secure-by-design architecture, enables the decommissioning of
legacy data centres by being cloud-native, and provides the essential mechanism
for data to flow into the National Data Resource (NDR) where services are unable
to integrate directly (the preferred approach).

* **Mission 2**: Deliver high quality digital products and services. This mission
requires that all digital health and social care systems can flow data to and from
the NDR. The Hub makes this possible for systems that today are unable to flow
data directly (without transformation/standardisation).

The product embodies key DHCW principles including:

* Simplify: It replaces a complex, proprietary ESB with a modern, streamlined, code-first approach.
* Use open, interoperable, and resilient infrastructure: It is built on open
standards and cloud-native services to ensure resilience and interoperability by design.
* Design for more data, more digital: It provides the scalable foundation needed
to handle the growing volume of digital data across the health and care system.

## Scope

In-Scope:

* Validation of incoming and outgoing data against defined schemas and standards.
* Transformation of data between different formats and standards (e.g., HL7v2, FHIR).
* Fully automated testing and deployment (CI/CD) pipelines.
* Robust monitoring, logging, and alerting for all integrations.
* Handling of sensitive (patient-identifiable) clinical data.

Out-of-Scope:

* Long-term storage of clinical data (it is a transient data-in-motion hub, not a data repository or lake).
* Providing a user interface for clinical or administrative staff.
* Business intelligence, analytics, or reporting on the data content itself.
* The source or destination applications themselves.

## Key Capabilities

* Data Standard Transformation - map and convert data between major health standards.
* Validation - enforce data quality rules and schemas for all messages.
* Developer Toolkit & Documentation - A comprehensive set of resources to enable
fast and consistent development of new integrations.
* Observability Dashboard: A centralised view of system health, transaction volumes, and error rates etc.

## Key Dependencies & Integrations

* Cloud Platform Provider (i.e. Azure) for all underlying infrastructure services.
* Integration with a wide range of internal NHS Wales systems and approved third-party applications.

## Objectives and Key Results (OKRs)

**Objective 1:** Prove the platform's value and drive initial adoption

| Key Result | Description |
| :--------: | ----------- |
| 1.1        | Successfully migrate 3 integrations from the legacy system to the Integration Hub. |
| 1.2        | Reduce the average time to develop and deploy a new integration by 30% compared to the legacy system. |

**Objective 2:** Enhance platform stability and operational excellence

| Key Result | Description |
| :--------: | ----------- |
| 2.1        | Maintain 99.9% uptime for all production integrations running on the hub. |
| 2.2        | Achieve an average end-to-end data processing latency of under 500ms for 95% of transactions. |
| 2.3        | Ensure 100% of integration errors are captured and alerted on via the observability dashboard within 5 minutes of occurrence. |
| 2.4        | Successfully handle a 2x spike in transaction volume during a load test with no manual intervention and a proportional cost increase, proving the pay-as-you-grow model. |
