# Opentelemetry Collector Visualization

### Focus on data flow
I tried how i would like to extract a visual from otel-config.yaml. Although the aim in discussion is more extensive but more grafana agent targeted, I intentionally tried my perception of visual over otelcol config. Mermaid used likewise in call for Graph as Code purposes here within.

### Notes

#### Automating dashboard

TODO: Grafana [Dashboard as Code](https://andidog.de/blog/2022-04-21-grafana-dashboards-best-practices-dashboards-as-code#:~:text=Grafana%20is%20a%20web%2Dbased,all%20based%20on%20open%20source)

#### Connecting Metrics On Dashboard
##### Option 1 : Via mermaidjs and diagram grafana plug in
<img width="1121" alt="image" src="https://user-images.githubusercontent.com/62701796/192148473-97e5273a-ca92-48a7-99ae-3d8a6877bd66.png">

##### Option 2 : Using promql and nodegraph plug in

<img width="759" alt="image" src="https://user-images.githubusercontent.com/62701796/192165733-8bd5f9ba-4449-495b-9ba5-8a2b0660ba42.png">
Using pure promql to form nodeGraph service architectures.

Additionally 
https://sriramajeyam.com/grafana-infinity-datasource/wiki/node-graph works with some effort over top, and works less tricky than the above solution. You are able to mix with other data sources, eg. you need edges as constants.

### **nodes**
```
label_replace(label_replace(label_replace(
sum by(__name__, receiver, exporter) ({__name__=~".*(accepted|sent)_metric_points", job="otelcol"})
, "id", "$0", "__name__", ".*")
, "title", "$1", "id"
, "(.*)"),"mainstat","$otelcol_receiver_accepted_metric_points","","")
```

### **edges**
```label_join(label_replace(label_replace(label_replace(
sum ({__name__=~".*(accepted|sent)_metric_points",job="otelcol"}  ) 
,"source","otelcol_receiver_accepted_metric_points","","")
,"target","otelcol_exporter_sent_metric_points","","")
,"mainstat","$otelcol_receiver_accepted_metric_points","","")
,"id","_","source","target")
```

###  template variable

```
query_result(avg(sum` by() (rate({__name__=~".*(accepted|sent)_metric_points",job="otelcol"}[1m])   )))
regex /.*\s(.+)\s.+/
```



### In action
Spiked an auto generated sample to play with here 

<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.6.1/css/all.css" integrity="sha384-gfdkjb5BdAXd+lj+gudLWI+BXq4IuLW5IT+brZEZsLFm++aCMlF1V92rMkPaX4PP" crossorigin="anonymous">
<a href="https://github.com/devrimdemiroz/opentelemetry-browser/blob/main/docs/GeneratedDiagram.md" ><i class="fab fa-github"></i> GeneratedDiagram.md</a>

<i class="fa fa-file-code-o" aria-hidden="true"></i>

```mermaid
flowchart LR


otelcol-config.yaml[fa:fa-file-code otelcol-config.yaml]-->|transform|mermaid(mermaid diagram as code)
```
### Sample otelcol-config.yaml
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

### Mermaid output sample

```mermaid
flowchart TD

classDef tclass fill:orange,stroke:#f66,stroke-width:2px,color:#fff
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

 subgraph pipeline_spanmetrics
end

end

    
```
### Mermaid output sample as plain Code
```el

flowchart TD

classDef tclass fill:orange,stroke:#f66,stroke-width:2px,color:#fff
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

subgraph pipeline_spanmetrics
end

end


```
