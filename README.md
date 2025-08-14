# Theia

**Reusable CDKTF modules for AWS service dashboards in Datadog.**

Theia is a collection of ready-to-use [CDK for Terraform](https://developer.hashicorp.com/terraform/cdktf) modules that automatically create **best-practice dashboards and monitors** in [Datadog](https://www.datadoghq.com/) for common AWS services like **Lambda** and **RDS**.

It’s designed to give teams **production-ready observability** with minimal setup, so you can spend less time wiring dashboards and more time shipping features.

---

## What it does

- **Out-of-the-box dashboards** for supported AWS services.
- **Curated metrics** and widgets following observability best practices (latency, errors, saturation, throughput, cost).
- **Optional monitors** with sensible defaults to avoid alert fatigue.
- **Tag-based queries** so dashboards work across accounts, regions, and environments.

---

## Why use it

Without Theia, every team has to reinvent the same dashboards and alerts for each service they own.  
With Theia, you:

- Get consistent, high-quality dashboards in minutes.
- Reduce human error in dashboard setup.
- Keep everything as code for version control and reproducibility.

---

## Example services covered

- AWS Lambda
- Amazon RDS

> More services planned: API Gateway, ECS, DynamoDB, S3...

---

## Quick example

```ts
import { DatadogProvider } from "@cdktf/provider-datadog/lib/provider";
import { AwsLambdaDashboards } from "@theia/aws-lambda-dashboards";

new DatadogProvider(this, "dd", {
  apiKey: process.env.DATADOG_API_KEY!,
  appKey: process.env.DATADOG_APP_KEY!,
});
```
