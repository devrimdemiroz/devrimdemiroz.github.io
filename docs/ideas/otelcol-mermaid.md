```yaml

    service:
      extensions: [pprof, zpages, health_check,sigv4auth]
      pipelines:
        traces:
          receivers: [otlp]
          processors: [spanmetrics,batch]
          exporters: [otlp]

        metrics/spanmetrics:
          receivers: [otlp/spanmetrics]
          exporters: [prometheus]

        metrics:
          receivers: [otlp,prometheus]
          exporters: [prometheusremotewrite,prometheusremotewrite/1]
```
```mermaid
flowchart TD
classDef tclass fill:#f96,stroke:#f66,stroke-width:2px,color:#fff

te(otlp)
subgraph pipeline_traces
    direction LR
    subgraph receivers
            
            T1((T)):::tclass
            
    end
    subgraph processors
            tp1(spanmetrics)
            tp2(batch)
    end
    subgraph exporters
            T2((T)):::tclass
            
            
    end
        otlp-->T1-->processors-->T2-->te
        linkStyle 0 stroke:#f96,stroke-width:3px,color:orange;
end

    metrics((M))
```