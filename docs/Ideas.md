{docsify-updated}
# Pocketful of Rainbows:

### 1 - opentelemetry-browser
👉 https://github.com/devrimdemiroz/opentelemetry-browser


### 2 - opentelemetry-collector visualization
As discussed in latest Grafana Agent community call https://www.youtube.com/watch?v=ftopI1chyG0&t=1080s "Focus on data flow..." section, I tried how i would like to extract a visual from otel-config.yaml. [A couple of tries with mermaid](ideas/otelcol-mermaid.md)



### 3 - Flamegraph like tracing graphs


### 4 - Aggregation on collector

https://github.com/grafana/tempo/pull/1378#discussion_r860658223
```text
Such TraceQL in my point of view as well needs to be available on the collection point with the aggregation feature. 
I would prefer to use TraceQL as a processor on the collector, especially for aggregation. 
This is a known tactic to overcome some usual cons. Filter more, have less cardinality, less noise... 
so to solve some of them with aggregation as a layer before it reaches to a storage layer.
```
