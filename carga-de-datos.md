# Carga de datos

> **Extract, Transform and Load** \(«extraer, transformar y cargar», frecuentemente abreviado ETL\) es el proceso que permite a las organizaciones mover datos desde múltiples fuentes, reformatearlos y limpiarlos, y cargarlos en otra base de datos, data mart, o data warehouse para analizar, o en otro sistema operacional para apoyar un proceso de negocio.

Soy consciente de lo complicado que obtener en ocasiones datos de calidad, o sencillamente datos. A veces te piden analizar algo y tienes que buscar la manera de obtener la información. Y una vez conseguida empieza lo divertido.

## Nodos, aristas y atributos

Cuando abramos un archivo de datos en **Gephi**, éste va a mirar tres tipos de datos:

* Nodos: Representan los elementos analizados.
* Aristas: Representan las relaciones existentes entre los nodos.
* Atributos: Pueden referirse a los nodos, o a los atributos. Es información extra que puede servir para el análisis. Por ejemplo, en un análisis de perfiles de Twitter si tenemos su localización, su número de seguidores o el idioma que utiliza, podremos segmentar por esos atributos para hacer un análisis más profundo.

Los nodos y las aristas son imprescindibles. Componen la topología de la red, sin ellos no se puede visualizar, ni analizar. Sin embargo los atributos son datos de la red, de sus componentes. Son opcionales!

## Archivos de grafo

**Gephi** soporta muchos tipos de archivo diferentes. Esta característica lo hace compatible con gran parte del [software de _Análisis de Redes_](http://www.k-government.com/2016/06/28/100-herramientas-analisis-redes-sna-ars/).

Según la propia [página de **Gephi**](https://gephi.org/users/supported-graph-formats/) los formato de archivos soportados son:

* [GEXF](https://gephi.org/gexf/format)
* [GDF](https://gephi.org/users/supported-graph-formats/gdf-format)
* [GML](https://gephi.org/users/supported-graph-formats/gml-format)
* [GraphML](https://gephi.org/users/supported-graph-formats/graphml-format)
* [Pajek NET](https://gephi.org/users/supported-graph-formats/pajek-net-format)
* [GraphViz DOT](https://gephi.org/users/supported-graph-formats/graphviz-dot-format)
* [CSV](https://gephi.org/users/supported-graph-formats/csv-format)
* [UCINET DL](https://gephi.org/users/supported-graph-formats/ucinet-dl-format)
* [Tulip TPL](https://gephi.org/users/supported-graph-formats/tulip-tlp-format)
* [Netdraw VNA](https://gephi.org/users/supported-graph-formats/netdraw-vna-format)
* [Spreadsheet](https://gephi.org/users/supported-graph-formats/spreadsheet/)

Para trabajar con un archivo de grafo de estos formatos sólo hay que ir a `Archivo > Abrir...` , y listo.

Ahora sólo hay que hacer caso a la pantalla de información del grafo, decidir si es dirigido o no, si lo queremos en un espacio de trabajo nuevo, o si lo queremos añadir al grafo en el que estemos trabajando.

![](/assets/Captura de pantalla 2017-02-19 a las 22.57.59.png)

## Archivos de grafo con .csv

Los archivos `.csv` son los más accesibles a la hora de incorporar datos de grafo a **Gephi**.

Podemos utilizarlos de dos maneras:

* Abriendo el archivo desde menú `Archivo > Abrir...` La estructura de estos archivos es muy simple. Sólo hay que colocar en la primera columna el nodo emisor, y en las columnas siguientes los nodos a los que está enlazando. 

![](/assets/Captura de pantalla 2017-02-19 a las 23.07.47.png)

* Importando el archivo desde laboratorio de datos. En este caso podemos generar dos tipos de .csv:
  * Tabla de nodos: Una lista con los nodos del grafo con los siguientes campos: Nombre, Id, Label. Son necesarios _Nombre_ e _Id_. El campo Id servirá de identificador a efectos de **Gephi**. 
  * Tabla de aristas: Una lista de dos campos; _Source y Target. Cómo su nombre indica en la columna Source _ incluiremos el nodo de origen, y en _Target_ el nodo destino.

> **Tip:** La mejor manera es importar primero las aristas. De esta manera se genera automáticamente la lista de nodos. De esta manera con sólo subir un archivo ya dispondremos de una archivo de grafo para analizar. Posteriormente si es necesario, podemos subir la tabla de nodos con atributos si nos es necesario para analizar el grafo.

![](/assets/Captura de pantalla 2017-02-19 a las 23.12.33.png)

