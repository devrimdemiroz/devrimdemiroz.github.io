 Discussed in  Grafana Agent community call https://www.youtube.com/watch?v=ftopI1chyG0&t=1080s "Focus on data flow..." section, I tried how i would like to extract a visual from otel-config.yaml.
```yaml

    service:
      extensions: [pprof, zpages, health_check]
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
---

```mermaid
flowchart TD

classDef tclass fill:#f96,stroke:#f66,stroke-width:2px,color:#fff
classDef mclass fill:blue,stroke:blue,stroke-width:2px,color:#fff

te(otlp)
subgraph otelcol
direction LR
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
            otlp1-->T1-->processors-->T2-->te
            linkStyle 0,1,2,3 stroke:#f96,stroke-width:3px,color:orange;
            
    end
         
    subgraph pipeline_metrics
        direction LR
        subgraph receivers2
                
                M1((M)):::mclass
                
        end
    
        subgraph exporters2
                M2((M)):::mclass
                
                
        end
            otlp2 & prometheus -->M1-->M2-->prometheusremotewrite & prometheusremotewrite2
            linkStyle 4,5,6,7,8 stroke:blue,stroke-width:3px,color:blue;
            
    end
end

    
```
