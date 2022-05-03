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
flowchart LR
subgraph pipeline_traces
  subgraph t_receivers
            tr(otlp)
            
        end
    subgraph t_processor
            tp1(spanmetrics)
            tp2(batch)
        end
        subgraph t_exporter
            te(otlp)
            
        end
        tr-->t_processor-->te
    end

    
    metrics((M))
```