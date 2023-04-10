# Prometheus naming conventions

### Links
* [Prometheus - metrics and labels naming](https://prometheus.io/docs/practices/naming/)

***

ChatGPT4:

Prometheus is an open-source monitoring and alerting toolkit designed for reliability and scalability. When using Prometheus to monitor your infrastructure, it's essential to follow best practices for naming conventions to ensure consistency, readability, and ease of use. Here's a detailed guide on naming conventions for infrastructure metrics intended for Prometheus:

1. Metric names:
* Use lowercase alphanumeric characters and underscores for metric names.
* Begin the metric name with a letter and avoid starting with a number.
* Use a verb, like "requests_total" or "bytes_received," to describe the measured action or event.
* Prefer concise and descriptive names that convey the meaning of the metric without being overly verbose.

2. Prefixes:
* Use a common prefix for all metrics related to a specific application or subsystem. This makes it easier to discover and group related metrics.
* The prefix typically consists of the application or subsystem name, followed by an underscore, e.g., "http_requests_total" or "node_cpu_seconds_total."

3. Units:
* Include the unit of measurement in the metric name when applicable, using a suffix like "_bytes," "_seconds," or "_percent."
* For rates or ratios, use a "per" separator, like "requests_per_second" or "errors_per_request."
* For gauges measuring time, use the "_seconds" suffix, e.g., "node_time_seconds."

4. Metric types:
* Prometheus supports four metric types: Counter, Gauge, Histogram, and Summary. Include the metric type in the name to provide context and clarity.
  * For Counters, add a "_total" suffix, e.g., "http_requests_total" or "errors_total."
  * For Gauges, use a descriptive name without a specific suffix, like "memory_usage_bytes" or "temperature_celsius."
  * For Histograms, use a "_bucket" suffix for the bucket series, "_sum" for the sum, and "_count" for the count, e.g., "request_duration_seconds_bucket," "request_duration_seconds_sum," and "request_duration_seconds_count."
  * For Summaries, use a "_sum" suffix for the sum, "_count" for the count, and "_quantile" for the quantile series, e.g., "request_latency_seconds_sum," "request_latency_seconds_count," and "request_latency_seconds{quantile="0.9"}."

5. Labels:
* Use labels to add dimensions and context to metrics without creating an excessive number of new metric names.
* Keep label names lowercase, descriptive, and concise.
* Common label names include "instance" for the target instance, "job" for the overall job, and "method" or "status" for HTTP requests.

6. Avoid high cardinality:
* High cardinality refers to a large number of unique combinations of metric names and label values, which can impact the performance of Prometheus.
* Limit the number of label values and avoid using labels for data that can have a high number of unique values, like user IDs or timestamps.
* By following these naming conventions for infrastructure metrics in Prometheus, you can maintain a consistent and understandable monitoring environment, making it easier to analyze, troubleshoot, and optimize your infrastructure.

