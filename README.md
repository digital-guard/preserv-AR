# preserv-AR
[Preservación digital](https://en.wikipedia.org/wiki/Digital_preservation) de las principales fuentes de la **base de datos AddressForAll-Argentina**, mantenida por el [Instituto AddressForAll](http://addressforall.org/).

A Argentina se le asignó: en el contexto [ISO&nbsp;3166](https://en.wikipedia.org/wiki/ISO_3166) el geocódigo [**AR**](https://en.wikipedia.org/wiki/ISO_3166-2:AR) y el número [**32**](https://en.wikipedia.org/wiki/ISO_3166-1_numeric); en [Wikidata](https://wikidata.org) el identificador [Q414](http://wikidata.org/entity/Q414); en [OpenStreetMap](https://osm.org) el identificador de [*relación* 286393](http://osm.org/relation/286393).


## Organización territorial

El territorio nacional y sus subdivisiones representan jurisdicciones:

- El país está dividido en **23 provincias**, administrados por un gobernador electo, **y la Ciudad Autónoma de Buenos Aires** (Capital y sede del Gobierno federal).
  - Las provincias tienen autonomía plena, forman parte de la Nación y son jurídicamente preexistentes a ella, según los principios del federalismo establecidos en la Constitución Nacional. Jurídicamente Argentina se constituyó como una federación de provincias y mantiene por mandato constitucional los nombres históricos de Provincias Unidas del Río de la Plata y Confederación Argentina, además de República Argentina (el único usual).
  - El gobierno provincial tiene un poder ejecutivo encabezado por el gobernador, un poder legislativo conformado por la legislatura provincial y un poder judicial.
- Las provincias se subdividen en **529 departamentos/partidos/comunas** (379 departamentos + 135 partidos + 15 comunas), que contienen 2.278 municipios.
  - Cada municipio está compuesto por un *departamento ejecutivo*, encabezado por un intendente municipal y un *departamento deliberativo* o *concejo deliberativo*, formado por concejales. El intendente y los concejales son elegidos por un período de 4 años. 
  - Corresponde al departamento deliberativo de las municipalidades nombrar las calles.
  - Cumplen una función de división catastral y estadística, y en algunas provincias también son utilizadas como distritos electorales para determinar representantes a las legislaturas provinciales y nacional o como unidades de descentralización de diversos órganos provinciales como la policía y el Poder Judicial. 
  - Fueron creadas por los gobiernos provinciales, por el gobierno nacional, al momento de ser las provincias territorios nacionales o, en algunos casos, por el gobierno virreinal en épocas anteriores a la independencia nacional. Actualmente la creación de nuevas subdivisiones corresponde a cada gobierno provincial, variando en metodología y complejidad.
  - En general, dentro de un departamento hay una o varias localidades pobladas que tienen su propio gobierno sea este municipal, comisión de fomento, etc. Una de ellas es denominada cabecera del departamento que, llegado el caso, sirve de asiento a las dependencias administrativas correspondientes.
  - En las provincias de Mendoza, San Juan y La Rioja los municipios tiene sus límites coincidentes con los departamentos. La cabecera del departamento es la localidad donde se ubica la sede del gobierno municipal.
  - La Provincia de Buenos Aires, se divide administrativamente en 135 partidos. De manera similar a las provincias de La Rioja, Mendoza y San Juan, cada partido contiene a un solo municipio. La denominación surge porque entre 1821 y 1854 el territorio bonaerense estuvo administrado por jueces de paz y su jurisdicción se correspondía con un partido judicial.
  - Las comunas son las unidades de gestión política y administrativa descentralizada de la ciudad, tienen competencia territorial, del patrimonio de su territorio y con personería jurídica propia. Cumplen además, una función electoral al momento de elegir funcionarios comunales y nacionales, reemplazando a las antiguas secciones electorales. Agrupan también a los barrios oficiales de la ciudad. Fueron establecidas en 1996, al sancionarse la Constitución de la Ciudad de Buenos Aires, reglamentadas en 2005 a través de la Ley 1777 y sus límites fijados en 2008 por la Ley 2650. Las juntas comunales deben ser integradas por siete miembros cada una y sus elecciones se llevan a cabo cada 4 años desde 2011.
- **Las entidades de tercer nivel son los municipios** (1793).
  - Las provincias de Entre Ríos y Santa Fe, dividen sus departamentos en distritos y la de Córdoba en pedanías.
  - El municipio es la entidad administrativa generalmente asociada a una ciudad. Está compuesto por un territorio claramente definido denominado ejido municipal y la población que lo habita. Su gobierno se denomina municipalidad cuyo poder ejecutivo es el intendente y el legislativo, el concejo deliberante.
  - Si bien las relaciones de inclusión entre departamentos y provincias es perfecto (no hay un departamento que se desarrollen en más de una provincia) esta relación entre municipio y departamentos no lo es. Existiendo unos pocos municipios que se desarrollan en más de un departamento.
  - Actualmente las pautas generales para la divisiones del territorio de las provincias y la fijación de los límites de los municipios está establecida en las constituciones provinciales y se delega al Poder Legislativo la fijación definitiva de límites.
 - Argentina cuenta con el **Código Postal Argentino (CPA)**, que es un sistema alfanumérico compuesto por: 1 letra que identifica la provincia (ISO 3166-2:AR.); 4 dígitos que identifican localidad, ciudad o distrito; y 3 letras que identifican la cara de manzana.
	 - El CPA es mantenido por la empresa pública *Correo Oficial de la República Argentina* (también denominada Correo Argentino), dependiente de la Secretaría de Innovación Pública, bajo la Jefatura de Gabinete de la Nación. 

## Organización de este repositorio

En este *git*, **solo se guardan los metadatos**, es decir, descriptores de entidad, como nombres y códigos geográficos &mdash; mapas y otros datos brutos, almacenados externamente porque son muy grandes.  Posteriormente, los "datos en bruto", no estandarizados, se convierten en "datos filtrados" y se conservan en lo [*git* preservCutGeo‑AR2021](http://git.digital-guard.org/preservCutGeo-AR2021).

Los metadatos se organizaron de la siguiente manera, en la carpeta [`/data`](./data):

* [`/data`](./data): "datos", todos los metadatos originales de **entrada**, es decir, metadatos proporcionados para el sistema.
   * `jurisdictionLevel*.csv`:  jurisdicciones (en todos los niveles) y sus geocódigos. La primera subdivisión es [jurisdictionLevel4.csv](./data/jurisdictionLevel4.csv).
   * [`donor.csv`](./data/donor.csv): donantes de paquetes de datos. Metadatos de las instituciones que brindan datos oficiales. (pendente)
   * [`donatedPack.csv`](./data/donatedPack.csv): descriptores de los archivos donados. (pendente)
   * *paquetes* (carpetas `_packXX`): *hash*  y otros descriptores de archivos almacenados externamente, así como `makefile` y otros descriptores de proceso para descomprimir estos archivos y llevarlos a la base de datos (PostregSQL)... 

* [`/src`](./src#readme): reservado a código fuente de algoritmos SQL, *makefile* y otros de uso local. Ver código fuente general em [Preserv](http://git.digital-guard.org/preserv).

## Licencia
[Licencia CC0](https://creativecommons.org/publicdomain/zero/1.0/deed.es).
