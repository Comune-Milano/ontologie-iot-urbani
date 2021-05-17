### Electric module - Usage Examples

The following example describes an Electric Mobility service provider that performs both the role of [uiote:ChargePointOperator](http://www.w3id.org/urban-iot/electric#ChargePointOperator) as it operates a network of [uiote:ChargingStation](http://www.w3id.org/urban-iot/electric#ChargingStation), and the role of [uiote:eMobilityServiceProvider](http://www.w3id.org/urban-iot/electric#eMobilityServiceProvider) making a charging service is available for users ([uiote:ChargingService](http://www.w3id.org/urban-iot/electric#ChargingService)) on a network of Electric Vehicle Supply Equipment (EVSE). The example shows the case in which the charging stations offered by the service are greater than those operated directly by the supplier.
```json
{
  "@context": "https://comune-milano.github.io/ontologie-iot-urbani/docs/urban-iot-context.jsonld",
  "@id": "http://www.example.com/org/ElectricMilanoProvider",
  "@type": ["uiote:ChargePointOperator", "uiote:eMobilityServiceProvider"],
  "schema:name": "Electric Milano",
  "uiote:providesChargingService": {
    "@id": "http://www.example.com/service/ElectricMilanoChargingService",
    "schema:name": "Electric Milano Charging Service",
    "schema:description": [{
      "@value":"Servizio Electric Milano di accesso alla ricarica per veicoli elettrici.",
      "@language": "it"
    },{
    "@value":"Electric Milano charging service for electric vehicles.",
    "@language": "en"
    }],
    "schema:areaServed": {
      "@id": "http://dbpedia.org/page/Milan"
    },
    "uiote:makesStationAvailable": [{
    "@id": "http://www.example.com/charging-station/ChargingStation7"
    },{
    "@id": "http://www.example.com/charging-station/ChargingStation8"
    },{
    "@id": "http://www.example.com/charging-station/ChargingStation9"
    }],
    "schema:offers": {
      "@id": "http://www.example.com/charging-service-offer/ElectricMilanoBase",
      "@type": "uiote:ChargingServiceOffer",
      "schema:name": "Base Electric Milano",
      "schema:priceCurrency": "EUR",
      "uiote:pricePerKwhCharge": {
        "@value" : "0.40",
        "@type": "xsd:double"
      },
      "uiote:pricePerMinuteParking": {
        "@value" : "0.02",
        "@type": "xsd:double"
      }
    }
  },
  "uiote:operates": [{
    "@id": "http://www.example.com/charging-station/ChargingStation7"
  },{
    "@id": "http://www.example.com/charging-station/ChargingStation8"
  }]
}
```
The following example describes a charging station ([uiote:ChargingStation](http://www.w3id.org/urban-iot/electric#ChargingStation)) operated by the operator described in the previous example ([http://www.example.com/org/ElectricMilanoProvider](http://www.example.com/org/ElectricMilanoProvider)).
```json
{
  "@context": "https://comune-milano.github.io/ontologie-iot-urbani/docs/urban-iot-context.jsonld",
  "@id": "http://www.example.com/charging-station/ChargingStation7",
  "@type": ["uiote:ChargingStation"],
  "dct:identifier": "cs7",
  "schema:name": "Charging Station Electric Milano Stazione Centrale",
  "uiot:includedInMobilityStation": {
      "@id": "http://www.example.com/mobility-station/MobilityStation13"
  },
  "uiote:operatedBy": {
    "@id": "http://www.example.com/org/ElectricMilanoProvider"
  },
  "uiote:hasChargingServiceOffer": {
    "@id": "http://www.example.com/charging-service-offer/ElectricMilanoBase"
  },
  "locn:location": {
    "@type": "dct:Location",
    "locn:address" : {
      "@type": "locn:Address",
      "locn:fullAddress": "Piazza Duca d'Aosta, 1, 20124 Milano MI" 
    }
  },
  "uiote:isPrivate": false,
  "uiote:chargingDuringClosure": true,
  "uiote:renewableSources": true,
  "schema:image": {
    "@id": "http://www.example.com/charging-station/cs7image.png"
  },
  "uiote:hasFacilityNearBy": {
    "@id": "http://dbpedia.org/page/Stazione_di_Milano_Centrale"
  },
  "uiote:hasEVSE": [{
    "@id": "http://www.example.com/charging-station/EVSE7-1"
  },{
    "@id": "http://www.example.com/charging-station/EVSE7-2"
  }]
}
```
The following example describes an Electric Vehicle Supply ([uiote:EVSE](http://www.w3id.org/urban-iot/electric#EVSE)) positioned in the charging station described in the previous example ([http://www.example.com/charging-station/ChargingStation7](http://www.example.com/charging-station/ChargingStation7)).
```json
{
  "@context": "https://comune-milano.github.io/ontologie-iot-urbani/docs/urban-iot-context.jsonld",
  "@id": "http://www.example.com/charging-station/EVSE7-1",
  "@type": "uiote:EVSE",
  "uiote:isEVSEof": {
    "@id": "http://www.example.com/charging-station/ChargingStation7"
  },
  "dct:identifier": "EVSE7-1",
  "uiote:serialNumber": "0001-5245-0007",
  "uiote:floorLevel": 0,
  "uiote:hasParkingRestriction": {
    "@id": "el-kos:parking-restriction#TimeLimited"
  },
  "uiote:hasChargeAccessMethod": [{
    "@id": "el-kos:charge-access-method#RemotePayment"
  },{
    "@id": "el-kos:charge-access-method#DirectPaymentTerminal"
  }],
  "uiote:hasEVSEChargeCategory": {
    "@id": "el-kos:EVSE-charge-category#Quick"
  },
  "uiote:hasConnector": {
    "@id": "http://www.example.com/charging-station/Connector7-1-1",
    "@type": "uiote:Connector",
    "uiote:providesCable": false,
    "uiote:hasStandard": {
      "@id": "http://schema.mobivoc.org/#Mennekes_Type_2"
    },
    "uiote:maxAmperageInA":64,
    "uiote:maxPowerInKW":22,
    "uiote:hasPowerSupply": {
      "@id": "el-kos:power-supply#AC"
    }
  }
}

```
The following example describes an occasional recharging session ([uiote: ChargingSession](http://www.w3id.org/urban-iot/electric#ChargingSession)), described as carried out by an unregistered user with payment directly on the column (EVSE). The reloading session is carried out using the column (EVSE) of the previous example ([http://www.example.com/charging-station/EVSE7-1](http://www.example.com/charging-station/EVSE7-1)).
```json
{
  "@context": "https://comune-milano.github.io/ontologie-iot-urbani/docs/urban-iot-context.jsonld",
  "@id": "http://www.example.com/charging/session0034234243",
  "@type": "uiote:ChargingSession",
  "dct:identifier": "session0034234243",
  "uiote:sessionOperatedBy": {
    "@id": "http://www.example.com/org/ElectricMilanoProvider"
  },
  "uiote:usesChargingStation": {
    "@id": "http://www.example.com/charging-station/ChargingStation7"
  },
  "uiote:usedEVSE": {
    "@id": "http://www.example.com/charging-station/EVSE7-1"
  },
  "uiote:usedConnector": {
    "@id": "http://www.example.com/charging-station/Connector7-1-1"
  },
  "uiot:reservationUsed": false,
  "uiot:registeredUser": false,
  "schema:startDate": {
    "@value" : "2020-08-01T10:20:15",
    "@type": "xsd:dateTime"
  },
  "schema:endDate": {
    "@value" : "2020-08-01T11:05:42",
    "@type": "xsd:dateTime"
  },
  "uiote:chargingSessionDuration": {
    "@value" : "PT45M27S",
    "@type": "xsd:duration"
  },
  "uiote:rechargeTimeMinutes": 34,
  "uiote:totalEnergy": {
    "@value" : "11.45",
    "@type": "xsd:double"
  }
}
```
The following example describes the records of two charging columns ([uiote: EVSERecord](http://www.w3id.org/urban-iot/electric#EVSERecord)) relating to the Electric Vehicle Supply Equipment (EVSE) in the charging station described in a previous example ([http://www.example.com/charging-station/ChargingStation7](http://www.example.com/charging-station/ChargingStation7)).
```json
{
  "@context": "https://comune-milano.github.io/ontologie-iot-urbani/docs/urban-iot-context.jsonld",
  "@id": "http://www.example.com/charging-station/ChargingStation7",
  "@type": "uiote:ChargingStation",
  "uiote:hasEVSE" : [{
    "@id": "http://www.example.com/charging-station/EVSE7-1",
    "uiot:latestRecord": {
      "@type": "uiote:EVSERecord",
      "uiot:recordTimestamp": {
        "@value": "2020-08-01T11:00:32",
        "@type": "xsd:dateTime"
      }, 
      "uiote:EVSEState": {
        "@id": "el-kos:EVSE-state#InCharge"
      }
    }
  }, {
    "@id": "http://www.example.com/charging-station/EVSE7-2",
    "uiot:latestRecord": {
      "@type": "uiote:EVSERecord",
      "uiot:recordTimestamp": {
        "@value": "2020-08-01T11:00:32",
        "@type": "xsd:dateTime"
      }, 
      "uiote:EVSEState": {
        "@id": "el-kos:EVSE-state#Available"
      }
    }
  }]
}
```
