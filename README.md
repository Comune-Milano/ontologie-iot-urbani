# ontologie-iot-urbani

Ontologie per gli Apparati IoT Urbani definite dal Comune di Milano. I vocabolari contenuti in questa repository sono stati sviluppati per supportare l'integrazione e la pubblicazione dei dati dei diversi fornitori di servizi che operano nell'ambito urbano.

_English_: Urban IoT Ontologies defined by the Milan Municipality. The vocabularies contained in this repository were developed to support the integration and publication of data from difference service provider operating in the urban area.

## Scopo e campo di applicazione del vocabolario
Le prime due ontologie sono state sviluppate nell'ambito della Mobilità Condivisa (servizi di Car, Bike, Moto, Micro-Mobility Sharing) e delle Infrastrutture di Ricarica per la Mobilità Elettrica. 

_English_: The first two ontologies were developed in the domain of Sharing Mobility (Car, Bike, Moto, Micro-Mobility Sharing Services) and Electric Mobility.

## Sviluppo del vocabolario
L’attività di Ontology Engineering ha seguito la metodologia [Linked Open Terms](https://lot.linkeddata.es/) (LOT) per lo sviluppo di ontologie e glossari. Il materiale generato nelle diverse attività svolte durante lo sviluppo del vocabolario (casi d'uso, user story,  ecc.) è disponibile nel [Vocabulary Wiki](https://github.com/Comune-Milano/ontologie-iot-urbani/wiki).

_English_: The Ontology Engineering process followed the [Linked Open Terms](https://lot.linkeddata.es/) (LOT) methodology to develop ontologies and glossaries. The material generated in the different activities of the development (use cases, user stories, etc.) is available in Italian in the [Vocabulary Wiki](https://github.com/Comune-Milano/ontologie-iot-urbani/wiki).

## Ontologie
Le ontologie contenute in questa repository sono associate al namespace https://w3id.org/urban-iot

La prima versione dei vocabolari si compone di tre moduli principali:
- Modulo *Core*: https://w3id.org/urban-iot/core (preferred prefix _uiot:_)
- Modulo *Sharing Mobility*: https://w3id.org/urban-iot/sharing (preferred prefix _uiots:_)
- Modulo *Electric Mobility*: https://w3id.org/urban-iot/electric (preferred prefix _uiote:_)

Le ontologie sono complementate da una serie di thesauri SKOS referenziati dai diversi moduli.

_English_: The ontologies contained in this repository are associated to the namespace https://w3id.org/urban-iot. The first version of the suite of ontologies is composed of three modules: Core, Sharing Mobility and Electric Mobility (linked above). The ontologies are complemented by a set of SKOS thesauri referenced by the different modules.

## Manutenzione
Per gestire segnalazioni o proposte di miglioramento relative al vocabolario, consigliamo di seguire le guide fornite in [Gestione Issues](https://github.com/Comune-Milano/ontologie-iot-urbani/wiki/Gestione-Issue).

_English_: To manage reports or suggested improvements with respect to the ontologies, we recommend to follow the guides provided in [Issues Management](https://github.com/Comune-Milano/ontologie-iot-urbani/wiki/Gestione-Issue).

## Esempi
Alcuni esempi di utilizzo sono dettagliati nella documentazione per esemplificare l'utilizzo del vocabolario. Nella cartella `examples` il file `queries.rq` contiente esempi di query SPARQL per ogni casi d'uso identificato.

_English_: Usage examples of the different modules are detailed in the documentation. In the `examples` folder the `queries.rq` file contains examples of SPARQL queries for every use case identified.

## Changelog
- _07-2020_: Release v1.0.0 Core, Sharing, Electric modules

## License

This work is licensed under a [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).

[![CC BY 4.0](https://i.creativecommons.org/l/by/4.0/88x31.png)](http://creativecommons.org/licenses/by/4.0/)