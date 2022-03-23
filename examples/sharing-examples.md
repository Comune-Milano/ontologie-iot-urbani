### Sharing module - Usage Examples

The following example describes a resource usage session ([uiot:UsageSession](http://www.w3id.org/urban-iot/core#UsageSession)) made available by a service ([schema:Service](https://schema.org/Service)).
```json
{
  "@context": "https://comune-milano.github.io/ontologie-iot-urbani/docs/urban-iot-context.jsonld",
  "@id": "http://www.example.com/sessions/session0034234269",
  "@type": "uiot:UsageSession",
  "schema:startDate": {
    "@value" : "2020-08-01T10:20:15",
    "@type": "xsd:dateTime"
  },
  "schema:endDate": {
    "@value" : "2020-08-01T11:05:42",
    "@type": "xsd:dateTime"
  },
  "schema:duration": {
    "@value" : "PT45M27S",
    "@type": "xsd:duration"
  },
  "uiot:reservationUsed": true,
  "uiot:usesResource": {
    "@id": "http://www.example.com/resources/r118"
  },
  "uiot:sessionEnabledBy": {
    "@id": "http://www.example.com/service/BikeMilano"
  },
  "uiot:sessionPerformedBy": {
    "@id": "http://www.example.com/users/U89343984"
  },
  "uiot:associatedBusiness": {
    "@id": "http://www.example.com/users/B115"
  }
}
```
The following example describes a private user subscribed to a service ([uiot:ServicePrivateUser](http://www.w3id.org/urban-iot/core#ServicePrivateUser)) and enabled by a business user ([uiot:ServiceBusinessUser](http://www.w3id.org/urban-iot/core#ServiceBusinessUser)).
```json
{
  "@context": "https://comune-milano.github.io/ontologie-iot-urbani/docs/urban-iot-context.jsonld",
  "@id": "http://www.example.com/users/U89343984",
  "@type": "uiot:ServicePrivateUser",
  "dct:identifier": "U89343984",
  "uiot:birthYear": 1994,
  "uiot:registrationDate": {
    "@value" : "2010-05-29",
    "@type": "xsd:date"
  },
  "uiot:userEnabledBy": {
    "@id": "http://www.example.com/users/B115"
  },
  "uiot:registeredTo": {
    "@id": "http://www.example.com/service/BikeMilano"
  }
}
```
The following example describes an IoT device ([sosa:Sensor](http://www.w3.org/ns/sosa/Sensor)) which is made available for the users as a resource in a service ([uiot:ServiceResource](http://www.w3id.org/urban-iot/core#ServiceResource)), and its last record ([uiot:SensorRecord](http://www.w3id.org/urban-iot/core#SensorRecord)).
```json
{
  "@context": "https://comune-milano.github.io/ontologie-iot-urbani/docs/urban-iot-context.jsonld",
  "@id": "http://www.example.com/r118",
  "@type": ["uiot:ServiceResource", "sosa:Sensor"],
  "uiot:madeAvailableBy": {
    "@id": "http://www.example.com/service/BikeMilano"
  },
  "uiot:latestRecord": {
    "@type": "uiot:SensorRecord",
    "uiot:recordTimestamp": {
      "@value" : "2020-08-01T11:00:42",
      "@type": "xsd:dateTime"
    },
    "uiot:containsObservation": [{
      "@type": "sosa:Observation",
      "sosa:observedProperty" : {
        "@id": "http://www.example.com/properties/speedInKmPerH"
      },
      "sosa:hasSimpleResult" : 23
    },{
    "@type": "sosa:Observation",
      "sosa:observedProperty" : {
        "@id": "http://www.example.com/properties/location"
      },
      "sosa:hasResult" : {
        "@type" : "geo:Point",
        "geo:lat" : {
          "@value" : "51.5",
          "@type": "xsd:decimal"
        },
        "geo:long" : {
          "@value" : "-0.12",
          "@type": "xsd:decimal"
        }
      }
    }]
  }
}
```
The following exemple describes a [uiot:MobilityStation](http://www.w3id.org/urban-iot/core#MobilityStation).
```json
{
  "@context": "https://comune-milano.github.io/ontologie-iot-urbani/docs/urban-iot-context.jsonld",
  "@id": "http://www.example.com/mobility-station/MobilityStation13",
  "@type": "uiot:MobilityStation",
  "dct:identifier": "MobilityStation13",
  "schema:name": "Mobility Station Stazione Centrale",
  "locn:location": {
    "@type": "dct:Location",
    "locn:geometry" : {
      "@value": "POLYGON ((9.202862726524472 45.48577466479756, 9.20265887863934 45.48560166220557, 9.203227506950498 45.48531959162287, 9.20343135483563 45.48549635601992, 9.202862726524472 45.48577466479756))",
      "@type": "geosparql:wktLiteral"
    },
    "locn:address" : {
      "@type": "locn:Address",
      "locn:fullAddress": "Piazza Duca d'Aosta, 1, 20124 Milano MI" 
    }
  }
}

```