# Learn more about Kubecost<a name="cost-monitoring-kubecost-bundles"></a>

Amazon EKS provides an AWS optimized bundle of Kubecost for cluster cost visibility\. Amazon EKS supports Kubecost, which you can use to monitor your costs broken down by Kubernetes resources including Pods, nodes, namespaces, and labels\.

This topic covers the available versions of Kubecost, and the differences between the available tiers\. EKS supports Kubecost Version 1 and Version 2\. Each version is available in different tiers\. You can use *Amazon EKS optimized Kubecost custom bundle* for your EKS clusters at no additional cost\. Also, you can use your existing AWS support agreements to obtain support\. 

 As a Kubernetes platform administrator and finance leader, you can use Kubecost to visualize a breakdown of Amazon EKS charges, allocate costs, and charge back organizational units such as application teams\. You can provide your internal teams and business units with transparent and accurate cost data based on their actual AWS bill\. Moreover, you can also get customized recommendations for cost optimization based on their infrastructure environment and usage patterns within their clusters\. For more information about Kubecost, see the [https://guide.kubecost.com](https://guide.kubecost.com) documentation\.

**What is the difference between the custom bundle of Kubecost and the free version of Kubecost \(also known as OpenCost\)?**

AWS and Kubecost collaborated to offer a customized version of Kubecost\. This version includes a subset of commercial features at no additional charge\. See the tables below for features that are included with in the custom bundle of Kubecost\.

## Kubecost v2<a name="kubecost-v2"></a>

**What is the difference between Kubecost v1 and v2?**

Kubecost 2\.0 is a major upgrade from previous versions and includes major new features including a brand new API Backend\. Note the [Allocation](https://docs.kubecost.com/apis/monitoring-apis/api-allocation) and [Assets](https://docs.kubecost.com/apis/monitoring-apis/assets-api) APIs are fully backwards compatible\. [Please review the Kubecost documentation to ensure a smooth transition\.](https://docs.kubecost.com/install-and-configure/install/kubecostv2) For the full list of enhancements, [please see the Kubecost release notes](https://github.com/kubecost/cost-analyzer-helm-chart/releases/tag/v2.0.0) 

**Important**  
[Review the Kubecost documentation before upgrading\.](https://docs.kubecost.com/install-and-configure/install/kubecostv2) Upgrading may impact report availability\. 

**Core features comparison:**


| Feature | Kubecost free tier 2\.0 | Amazon EKS optimized Kubecost bundle 2\.0 | Kubecost Enterprise 2\.0 | 
| --- | --- | --- | --- | 
| Cluster cost visibility | Single clusters up to 250 cores | Unified multi\-cluster without core limits | Unified and unlimited number of clusters across unlimited numbers of environments \(i\.e\. multi\-cloud\) | 
| Deployment | User hosted |  User hosted  | User hosted, Kubecost hosted \(dedicated tenant\), SaaS | 
| Databases supported | Local Prometheus | Amazon Managed Service for Prometheus or Local Prometheus | Any prometheus flavor and custom databases | 
| Database retention support \(raw metrics\) | 15 days | Unlimited historical data | Unlimited historical data | 
| Kubecost API and UI retention \(ETL\) | 15 days | 15 days | Unlimited | 
| Hybrid cloud visibility | \- | Amazon EKS and Amazon EKS Anywhere clusters | Multi\-cloud and hybrid cloud | 
| Alerts and recurring reports | Only supported on the primary cluster, limited to 250 cores | Efficiency alerts, budget alerts, spend change alerts, and [more supported](https://docs.kubecost.com/using-kubecost/navigating-the-kubecost-ui/alerts) across all clusters | Efficiency alerts, budget alerts, spend change alerts, and [more supported](https://docs.kubecost.com/using-kubecost/navigating-the-kubecost-ui/alerts) across all clusters | 
| Saved reports | \- | Reports using 15 days of metrics | Reports using unlimited historical data and metrics | 
| Cloud billing integration | Only supported on the primary cluster, limited to 250 cores | Custom pricing support for AWS \(including multiple clusters and multiple accounts\) | Custom pricing support for any cloud | 
| Savings recommendations | Only supported on the primary cluster, limited to 250 cores | Primary cluster insights, but there is no 250 core limit | Multi\-cluster insights | 
| Governance: Audits | \- | \- | Audit historical cost events | 
| Single sign\-on \(SSO\) support | \- | Amazon Cognito supported | Okta, Auth0, PingID, KeyCloak, and anything else custom | 
| Role\-based access control \(RBAC\) with SAML 2\.0 | \- | \- | Okta, Auth0, PingID, KeyCloak, and anything else custom | 
| Enterprise training and onboarding | \- | \- | Full\-service training and FinOps onboarding | 
| Teams | \- | \- | Yes | 

**New Features:**

The following features have metric limits:
+ Kubecost Aggregator
+ Network Monitoring
+ Kubecost Actions
+ Collections
+ Anomaly detection
+ Container Request Right\-Sizing
+ Kubecost Forecasting
+ Autocomplete for filtering and aggregation

**Metric limits:**


| Metric | Kubecost Free Tier 2\.0 | Amazon EKS Optimized Kubecost Custom Bundle 2\.0 | Kubecost Enterprise 2\.0 | 
| --- | --- | --- | --- | 
| Cluster size | Limited to 250 cores | Unlimited | Unlimited | 
| Metric retention | 15 days | 15 days | Unlimited | 
| Multi\-cluster support | Not available | Available | Available | 
| Core limits | 250 cores per cluster | No core limits | No core limits | 

## Kubecost v1<a name="kubecost-v1"></a>


| Feature | Kubecost free tier | Amazon EKS optimized Kubecost custom bundle | Kubecost Enterprise | 
| --- | --- | --- | --- | 
| Deployment | User hosted | User hosted | User hosted or Kubecost hosted \(SaaS\) | 
| Number of clusters supported | Unlimited | Unlimited | Unlimited | 
| Databases supported | Local Prometheus | Local Prometheus or Amazon Managed Service for Prometheus | Prometheus, Amazon Managed Service for Prometheus, Cortex, or Thanos | 
| Database retention support | 15 days | Unlimited historical data | Unlimited historical data | 
| Kubecost API retention \(ETL\) | 15 days | 15 days | Unlimited historical data | 
| Cluster cost visibility | Single clusters | Unified multi\-cluster | Unified multi\-cluster | 
| Hybrid cloud visibility | \- | Amazon EKS and Amazon EKS Anywhere clusters | Multi\-cloud and hybrid\-cloud support | 
| Alerts and recurring reports | \- | Efficiency alerts, budget alerts, spend change alerts, and more supported | Efficiency alerts, budget alerts, spend change alerts, and more supported | 
| Saved reports | \- | Reports using 15 days data | Reports using unlimited historical data | 
| Cloud billing integration | Required for each individual cluster | Custom pricing support for AWS \(including multiple clusters and multiple accounts\) | Custom pricing support for AWS \(including multiple clusters and multiple accounts\) | 
| Savings recommendations | Single cluster insights | Single cluster insights | Multi\-cluster insights | 
| Governance: Audits | \- | \- | Audit historical cost events | 
| Single sign\-on \(SSO\) support | \- | Amazon Cognito supported | Okta, Auth0, PingID, KeyCloak | 
| Role\-based access control \(RBAC\) with SAML 2\.0 | \- | \- | Okta, Auth0, PingID, Keycloak | 
| Enterprise training and onboarding | \- | \- | Full\-service training and FinOps onboarding | 

## Frequently asked questions<a name="cost-monitoring-faq"></a>

See the following common questions and answers about using Kubecost with Amazon EKS\.

**What is the Kubecost API retention \(ETL\) feature?**

The Kubecost ETL feature aggregates and organizes metrics to surface cost visibility at various levels of granularity \(such as `namespace-level`, `pod-level`, and `deployment-level`\)\. For the custom Kubecost bundle, customers get data and insights from metrics for the last 15 days\.

**What is the alerts and recurring reports feature? What alerts and reports does it include?**

Kubecost alerts allow teams to receive updates on real\-time Kubernetes spend as well as cloud spend\. Recurring reports enable teams to receive customized views of historical Kubernetes and cloud spend\. Both are configurable using the Kubecost UI or Helm values\. They support email, Slack, and Microsoft Teams\.

**What do saved reports include?**

Kubecost saved reports are predefined views of cost and efficiency metrics\. They include cost by cluster, namespace, label, and more\.

**What is cloud billing integration?**

Integration with AWS billing APIs allows Kubecost to display out\-of\-cluster costs \(such as Amazon S3\)\. Additionally, it allows Kubecost to reconcile Kubecost’s in\-cluster predictions with actual billing data to account for spot usage, savings plans, and enterprise discounts\.

**What do savings recommendations include?**

Kubecost provides insights and automation to help users optimize their Kubernetes infrastructure and spend\.

**Is there a charge for this functionality?**

No\. You can use this version of Kubecost at no additional charge\. If you want additional Kubecost capabilities that aren’t included in this bundle, you can buy an enterprise license of Kubecost through the AWS Marketplace, or from Kubecost directly\.

**Is support available?**

Yes\. You can open a support case with the AWS Support team at [Contact AWS](https://aws.amazon.com/contact-us/)\.

**Do I need a license to use Kubecost features provided by the Amazon EKS integration?**

No\.

**Can I integrate Kubecost with AWS Cost and Usage Report for more accurate reporting?**

Yes\. You can configure Kubecost to ingest data from AWS Cost and Usage Report to get accurate cost visibility, including discounts, Spot pricing, reserved instance pricing, and others\. For more information, see [AWS Cloud Billing Integration](https://docs.kubecost.com/install-and-configure/install/cloud-integration/aws-cloud-integrations) in the Kubecost documentation\.

**Does this version support cost management of self\-managed Kubernetes clusters on Amazon EC2?**

No\. This version is only compatible with Amazon EKS clusters\.

**Can Kubecost track costs for Amazon EKS on AWS Fargate?**

Kubecost provides best effort to show cluster cost visibility for Amazon EKS on Fargate, but with lower accuracy than with Amazon EKS on Amazon EC2\. This is primarily due to the difference in how you’re billed for your usage\. With Amazon EKS on Fargate, you’re billed for consumed resources\. With Amazon EKS on Amazon EC2 nodes, you’re billed for provisioned resources\. Kubecost calculates the cost of an Amazon EC2 node based on the node specification, which includes CPU, RAM, and ephemeral storage\. With Fargate, costs are calculated based on the requested resources for the Fargate Pods\.

**How can I get updates and new versions of Kubecost?**

You can upgrade your Kubecost version using standard Helm upgrade procedures\. The latest versions are in the [Amazon ECR Public Gallery](https://gallery.ecr.aws/kubecost/cost-analyzer)\.

**Is the `kubectl-cost` CLI supported? How do I install it?**

Yes\. `Kubectl-cost` is an open source tool by Kubecost \(Apache 2\.0 License\) that provides CLI access to Kubernetes cost allocation metrics\. To install `kubectl-cost`, see [Installation](https://github.com/kubecost/kubectl-cost#installation) on GitHub\.

**Is the Kubecost user interface supported? How do I access it?**

Kubecost provides a web dashboard that you can access through `kubectl` port forwarding, an ingress, or a load balancer\. You can also use the AWS Load Balancer Controller to expose Kubecost and use Amazon Cognito for authentication, authorization, and user management\. For more information, see [How to use Application Load Balancer and Amazon Cognito to authenticate users for your Kubernetes web apps](https://aws.amazon.com/blogs/containers/how-to-use-application-load-balancer-and-amazon-cognito-to-authenticate-users-for-your-kubernetes-web-apps/) on the AWS blog\.

**Is Amazon EKS Anywhere supported?**

No\.

## Additional Kubecost Features<a name="kubecost-additional"></a>
+ The following features are available in both Kubecost v1 and v2\. 
+ **Export cost metrics** – Amazon EKS optimized cost monitoring is deployed with Kubecost and Prometheus, which is an open\-source monitoring system and time series database\. Kubecost reads metric from Prometheus and then performs cost allocation calculations and writes the metrics back to Prometheus\. The Kubecost front\-end reads metrics from Prometheus and shows them on the Kubecost user interface\. The architecture is illustrated in the following diagram\.  
![\[\]](http://docs.aws.amazon.com/eks/latest/userguide/images/kubecost-architecture.png)

  With [https://prometheus.io/](https://prometheus.io/) pre\-installed, you can write queries to ingest Kubecost data into your current business intelligence system for further analysis\. You can also use it as a data source for your current [https://grafana.com/](https://grafana.com/) dashboard to display Amazon EKS cluster costs that your internal teams are familiar with\. To learn more about how to write Prometheus queries, see the [Prometheus Configuration](https://github.com/opencost/opencost/blob/develop/PROMETHEUS.md) `readme` file on GitHub or use the example Grafana JSON models in the [Kubecost Github repository](https://github.com/kubecost/cost-analyzer-helm-chart/tree/develop/cost-analyzer) as references\.
+ **AWS Cost and Usage Report integration** – To perform cost allocation calculations for your Amazon EKS cluster, Kubecost retrieves the public pricing information of AWS services and AWS resources from the AWS Price List API\. You can also integrate Kubecost with **AWS Cost and Usage Report** to enhance the accuracy of the pricing information specific to your AWS account\. This information includes enterprise discount programs, reserved instance usage, savings plans, and spot usage\. To learn more about how the AWS Cost and Usage Report integration works, see [AWS Cloud Billing Integration](https://docs.kubecost.com/install-and-configure/install/cloud-integration/aws-cloud-integrations) in the Kubecost documentation\.