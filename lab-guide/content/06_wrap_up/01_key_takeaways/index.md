## Key Takeaways

* Management Zones are still supported for Gen2 use cases
    - Customers can continue to manage access and filter visualizations to Classic Dynatrace using MZ
* Managing access and filtering visualizations with Grail uses IAM + Segments
    - Manage access to data in Grail with IAM Policies, including record-level permission statements
    - Filter visualizations with Grail using Segments
* Customers should strategize their IAM Policies for data access management first before developing Segment configurations
    - Segments are quick and reusable DQL query filters, not like management zones!
* Segment feature improvements are coming
    - Many of today’s limitations are due to the entity model not being in Grail
* Best practice implementation sequence:
    - Ingest data into Dynatrace, Configure OpenPipeline, Configure IAM, Configure Segments
