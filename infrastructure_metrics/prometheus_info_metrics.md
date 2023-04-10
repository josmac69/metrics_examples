# Prometheus info metrics

ChatGPT4:

* In Prometheus and Alertmanager, "info" metrics are a special kind of metrics used to provide metadata about monitored entities, software versions, or configurations.
* They are generally represented as Gauge metrics with a value of 1 and are used in combination with labels to expose additional information.

1. Usage in Prometheus:
* Exposing metadata: Info metrics are used to expose metadata about the monitored services or systems. This metadata can include software version numbers, build information, configurations, or any other relevant details.
* For example, consider an application that provides an API. You can create an info metric to expose the API version: `api_info{version="1.2.3"} 1`
  * Here, "api_info" is the metric name, "version" is a label with the value "1.2.3", and the metric value is 1.

2. Joining with other metrics
* Info metrics can be used in combination with other metrics in PromQL queries.
* By joining info metrics with other metrics, you can filter or aggregate data based on the metadata provided by the info metric.
* For example, you can calculate the error rate for a specific version of the API: `sum(rate(http_requests_total{status_code=~"5.."}[5m])) / sum(rate(http_requests_total[5m])) * on(version) group_left api_info`
  * This PromQL query calculates the error rate for each API version by dividing the sum of 5xx status code requests by the total number of requests, using the "version" label from the "api_info" metric.

3. Usage in Alertmanager:

* In Alertmanager, info metrics can be used as part of alerting rules.
* By incorporating info metrics into alerting rules, you can create more specific or targeted alerts based on metadata.

4. Creating alerts based on metadata:
* Info metrics can be included in alerting rules to trigger alerts based on specific metadata values.
* For example, you can create an alert that triggers when the error rate exceeds a certain threshold for a specific API version:
```
- alert: HighErrorRateByVersion
  expr: sum(rate(http_requests_total{status_code=~"5.."}[5m])) / sum(rate(http_requests_total[5m])) * on(version) group_left api_info > 0.1
  for: 5m
  labels:
    severity: critical
  annotations:
    summary: "High error rate for API version {{$labels.version}}"
```
* This alerting rule calculates the error rate for each API version, as in the previous example, and triggers an alert when the error rate exceeds 10% for any version.

In summary, info metrics are a valuable tool for exposing metadata in Prometheus and Alertmanager. They can be used to provide more context for monitoring and alerting, making it easier to understand and troubleshoot issues in your systems.