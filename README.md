# Ontologie per gli Apparati IoT Urbani

Ontologie per gli Apparati IoT Urbani definite dal Comune di Milano. I vocabolari contenuti in questa repository sono stati sviluppati per supportare l'integrazione e la pubblicazione dei dati dei diversi fornitori di servizi che operano nell'ambito urbano.

_**English version** of the README available below._

## Scopo e campo di applicazione del vocabolario
Le prime due ontologie sono state sviluppate nell'ambito della Mobilità Condivisa (servizi di Car, Bike, Moto, Micro-Mobility Sharing) e delle Infrastrutture di Ricarica per la Mobilità Elettrica.

## Sviluppo del vocabolario
L’attività di Ontology Engineering ha seguito la metodologia [Linked Open Terms](https://lot.linkeddata.es/) (LOT) per lo sviluppo di ontologie e glossari. Il materiale generato nelle diverse attività svolte durante lo sviluppo del vocabolario (casi d'uso, user story,  ecc.) è disponibile nel [Vocabulary Wiki](https://github.com/Comune-Milano/ontologie-iot-urbani/wiki).

La cartella `diagrams` contiene i file sorgente (`.drawio`) dei diagrammi utilizzati nella fase di modellazione concettuale e nella documentazione dei moduli implementati.

Lo sviluppo della prima versione delle Ontologie per gli Apparati IoT Urbani è descritta nel seguente journal paper:

> Mario Scrocca, Ilaria Baroni and Irene Celino. _Urban IoT ontologies for sharing and electric mobility_, Semantic Web Journal, [https://doi.org/10.3233/SW-210445](https://doi.org/10.3233/SW-210445), 2021.

## Ontologie
Le ontologie contenute in questa repository sono associate al namespace https://w3id.org/urban-iot

La prima versione dei vocabolari si compone di tre moduli principali:
- Modulo *Core*: https://w3id.org/urban-iot/core (preferred prefix _uiot:_)
- Modulo *Sharing Mobility*: https://w3id.org/urban-iot/sharing (preferred prefix _uiots:_)
- Modulo *Electric Mobility*: https://w3id.org/urban-iot/electric (preferred prefix _uiote:_)

Le ontologie sono complementate da una serie di thesauri SKOS referenziati dai diversi moduli.

## Manutenzione
Per gestire segnalazioni o proposte di miglioramento relative al vocabolario, consigliamo di seguire le guide fornite in [Gestione Issues](https://github.com/Comune-Milano/ontologie-iot-urbani/wiki/Gestione-Issue).

## Esempi
Nella cartella `examples`: (i) alcuni esempi di utilizzo sono dettagliati per ciascun modulo per esemplificare l'utilizzo dei vocabolari, (ii) il file `queries.rq` contiente esempi di query SPARQL per ogni casi d'uso identificato.

## Changelog
- _2022-03_: Release `v1.0.1` Change namespace schema.org (https://)
- _2020-07_: Release `v1.0.0` Core, Sharing, Electric modules

## License

This work is licensed under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).

[![CC BY 4.0](https://i.creativecommons.org/l/by/4.0/88x31.png)](http://creativecommons.org/licenses/by/4.0/)


---


# Urban IoT Ontologies

Urban IoT Ontologies defined by the Milan Municipality. The vocabularies contained in this repository were developed to support the integration and publication of data from difference service provider operating in the urban area.

## Purpose and scope of the ontologies

The first two ontologies were developed in the domain of Sharing Mobility (Car, Bike, Moto, Micro-Mobility Sharing Services) and Electric Mobility.

## Ontology engineering

The ontology engineering process followed the [Linked Open Terms](https://lot.linkeddata.es/) (LOT) methodology to develop ontologies and glossaries. The material generated in the different activities of the development (use cases, user stories, etc.) is available in Italian in the [Vocabulary Wiki](https://github.com/Comune-Milano/ontologie-iot-urbani/wiki). A sample of the material generated is available in English in the Wiki.

The `diagrams` folder contains the source files (`.drawio`) of diagrams used in the conceptual modelling and in the documentation of the implemented modules.

The development of the first version of the Urban IoT Ontologies is described in the following journal paper:

> Mario Scrocca, Ilaria Baroni and Irene Celino. _Urban IoT ontologies for sharing and electric mobility_, Semantic Web Journal, [https://doi.org/10.3233/SW-210445](https://doi.org/10.3233/SW-210445), 2021.

## Ontologies
The ontologies contained in this repository are associated to the namespace https://w3id.org/urban-iot. The first version of the suite of ontologies is composed of three modules:
- *Core* Module: https://w3id.org/urban-iot/core (preferred prefix _uiot:_)
- *Sharing Mobility* Module: https://w3id.org/urban-iot/sharing (preferred prefix _uiots:_)
- *Electric Mobility* Module: https://w3id.org/urban-iot/electric (preferred prefix _uiote:_)

The ontologies are complemented by a set of SKOS thesauri referenced by the different modules.

## Maintenance
To manage reports or suggested improvements with respect to the ontologies, we recommend to follow the guides provided in [Issues Management](https://github.com/Comune-Milano/ontologie-iot-urbani/wiki/Gestione-Issue).

## Examples
In the `examples` folder: (i) examples are provided for each module to exemplify the intended usage, (ii) the `queries.rq` file contains examples of SPARQL queries for every use case identified.

## Changelog
- _2022-03_: Release `v1.0.1` Change namespace schema.org (https://)
- _2020-07_: Release `v1.0.0` Core, Sharing, Electric modules

## License

This work is licensed under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).

[![CC BY 4.0](https://i.creativecommons.org/l/by/4.0/88x31.png)](http://creativecommons.org/licenses/by/4.0/)