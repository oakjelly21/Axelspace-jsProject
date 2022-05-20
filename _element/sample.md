## Component and interface diagram
The hosted payload interface diagram below represents what is explained in this document by showing several types of interface between the hosted payload and the satellite. Each of the interface symbol corresponds to a section of this document. Also it shows some of the satellite components that are mentioned in this document.

```plantuml
@startuml
title
__Hosted Payload Interface Diagram__
end title

scale 0.8
skinparam nodesep 30
skinparam ranksep 50
left to right direction

rectangle {
component Satellite {
  component Connector_S2PH
  component OBC
  component STR_PZ_Panel
  component Thermometer
  component Thermal_Insulator
  component Fasteners
  component Others
}
component GroundSystem
}
component Payload 
component PayloadUser
component Payload_Harness
together {
interface Electrical_Interface as "Electical\nI/F"
interface Data_Interface as "Data I/F"
interface Mechanical_Interface as "Thermal I/F\nStructural I/F"
interface Orbit_Interface as "Orbit I/F"
interface Electrical_Connector_Interface as  "Electrical\nConnector\nI/F"
interface Environmental_Interface as "Environmental\nI/F"
}
interface UserInterface as "User I/F"

PayloadUser -- UserInterface
UserInterface -- GroundSystem
GroundSystem -left- Satellite
OBC -- Connector_S2PH
OBC -- Electrical_Interface
OBC -- Data_Interface
Connector_S2PH -- Electrical_Connector_Interface
STR_PZ_Panel -- Mechanical_Interface
Thermometer -- Mechanical_Interface
Thermal_Insulator -- Mechanical_Interface
Fasteners -- Mechanical_Interface
Satellite -- Orbit_Interface
Satellite -- Environmental_Interface

Electrical_Connector_Interface -- Payload_Harness 
Payload_Harness -- Payload

Electrical_Interface -- Payload
Data_Interface -- Payload
Mechanical_Interface -- Payload
Orbit_Interface --Payload
Environmental_Interface --Payload


@enduml
```



```plantuml
title
__Ground System Interface Diagram__
end title

autonumber 0

participant PayloadUser
participant GroundSystem
participant Satellite
participant Payload

Satellite <-- Payload : Telemetry
...
PayloadUser --> GroundSystem : Request
activate GroundSystem
rnote over GroundSystem: Create command
Satellite <-- GroundSystem : Uplink
deactivate GroundSystem
...
Satellite --> Satellite : Time-tagged command
activate Satellite
Satellite --> Satellite : Command to satellite bus
deactivate Satellite
...
Satellite --> Satellite : Time-tagged command
activate Satellite
Satellite --> Payload : Command
deactivate Satellite
...
Satellite <-- Payload : Telemetry
activate Satellite
Satellite --> Satellite : Store the telemetry data
deactivate Satellite
...
Satellite --> Satellite : Read from storage
activate Satellite
Satellite --> GroundSystem : Downlink
deactivate Satellite
rnote over GroundSystem: Create raw data set
activate GroundSystem
GroundSystem --> PayloadUser : Data product
deactivate GroundSystem
```



### Responsibility assignment (**Payload specific**)

Responsibility of participating organization for each component is listed below.

```vega-lite
{
  "$schema": "https://vega.github.io/schema/vega-lite/v4.json",
  "width": 400,
  "data": {"values":[
    {
      "Item":"Payload",
      "Organization": "ASPINA",
      "Symbol": "O"
    }, {
      "Item":"Payload harness",
      "Organization":"ASPINA",
      "Symbol": "O"
    }, {
      "Item":"Satellite",
      "Organization":"Axel",
      "Symbol": "O"
    }, {
      "Item":"GroundSystem",
      "Organization":"Axel",
      "Symbol": "O"
    }, {
      "Item":"PayloadUser",
      "Organization": "ASPINA",
      "Symbol": "O"
    }
    ]
  },
  "layer":[{
    "mark": {"type": "text", "filled": false}
  },{
    "mark": {"type": "rect", "opacity": 0}
  }],
  "encoding": {
    "y": {"field": "Item", "type": "nominal",
    "sort": "null",    
    "axis": { "tickBand": "extent"}
    },
    "x": {
      "field": "Organization", "type": "ordinal",
      "sort": "null",    
      "axis": { 
        "tickBand": "extent",
        "orient": "top",
        "labelAngle": 0
      }
    },
    "text": {"field": "Symbol"}
  },
  "config": {
    "axis": {"grid": true, "tickBand": "extent"}
  }
}
```
