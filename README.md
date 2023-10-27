# DataGrokr_project
A project to run analyze large dataset, run sql queries and host flask application on local and ngrok
Dataset used is a housing dataset

Dataset example:

	id	ad_type	start_date	end_date	created_on	lat	lon	l1	l2	l3	l4	l5	l6	rooms	bedrooms	bathrooms	surface_total	surface_covered	price	currency	price_period	title	description	property_type	operation_type
107397	YhXDVa/KIlF7EjJMulHiyA==	Propiedad	26-03-2020	08-04-2020	26-03-2020	-34.562465	-58.465079	Argentina	Capital Federal	Belgrano				3	2	2			220000	USD		OPPEL | Departamento en Venta | Cod: 29583	"DEPARTAMENTO  EN VENTA / ALQUILER  | BELGRANO  - Capital Federal  |   3 AMBIENTES Semipiso al frente, en muy buen estado, excelente luz y vista abierta, gran ubicaciÃ³n prÃ³ximo a avenidas y medios de transporte.Consta de palier semiprivado, living comedor con salida a balcÃ³n al frente, dormitorio en suite con vestidor y placard, dormitorio con placard, dos baÃ±os completos, cocina abierta al living, lavadero en cocina.Cuenta con calefacciÃ³n por losa radiante, agua caliente por caldera.En edificio de 12 pisos, 2 departamentos por piso. Con terraza con parrilla. Posibilidad de alquilar cochera en el edificio.Apto Discapacitados: NO CÃ³digo OPPEL:   29583 Las especificaciones y medidas son informativas y aproximadas.No se incluyen: mobiliarios, artefactos elÃ©ctricos, luminarias o de aire OPPEL S.A. Mariano Oppel M.468 F.19 L.1 - CUCICBA

 XINTEL(OPL-OP2-3332)"	Departamento	Venta
918839	jHxD7psAg4+AC07T3sognw==	Propiedad	08-03-2020	09-03-2020	08-03-2020	-37.999235	-57.553724	Argentina	Buenos Aires Costa AtlÃ¡ntica	Mar del Plata						1			155000	USD		2 AMBIENTES A ESTRENAR CON COCHERA	2 AMBIENTES CON BALCON Y PARRILLA.  COCHERALIVING COMEDOR AL CONTRAFRENTE CON AMPLIO BALCÃ“N CON PARRILLA. COCINA INTEGRADA.  BAÃ‘O COMPLETO. CALEFACCIÃ“N POR RADIADORES. ARTEFACTOS DE PRIMERA CALIDAD.   Ref#357152.	Otro	Venta
204435	IYPdaIGi5Obo4eLzwUY+LA==	Propiedad	26-10-2020	03-02-2021	26-10-2020	-34.4533074	-58.6494098	Argentina	Bs.As. G.B.A. Zona Norte	Tigre					3	3	900	310	480000	USD	Mensual	Casa en Venta, Barrio Sta. Barbara	"Casa racionalista en tres plantas, con espacios amplios, doble altura, mucha luz natural y ventanales. DiseÃ±o de vanguardia y detalles de calidad. ConstrucciÃ³n de: pisos de porcellanato, aberturas interiores de cedro Moras de estilo italiano, exteriores de aluminio con termopanel (DVH) , vidrios interiores y panios fijos laminados , escalera y puente de madera maciza. Practicidad en la distribuciÃ³n de accesos y ambientes, con doble circulaciÃ³n por escaleras. Aire acondicionado split en todos los ambientes, calefacciÃ³n por piso radiante. Sistema de alarma con control remoto y tablero de control. Living de grandes dimensiones, comedor, placard para visitas, toilette y circulaciÃ³n desde garaje (con portÃ³n corredizo automatizado. Moderna cocina con muebles de bajo-mesada, comedor diario con salida a galerÃ­a y patio. 3 dormitorios , todos en suite. Dormitorio ppal. en planta baja, con escritorio, ante-baÃ±o (2 bachas) y baÃ±o compartimentado (baÃ±era y box de ducha) gran bajo-mesada con espacio de guardado, dormitorio con gran placard y salida al jardÃ­n.
<br>Dormitorio en suite con acceso a terraza, escritorio en puente. Oratorio original y luminoso. Tercer dormitorio: amplÃ­simo ambiente doble, con 2 ante baÃ±os y vestidores, gran ventanal vista al jardÃ­n. SalÃ³n de televisiÃ³n o family. Escritorio.
<br>
<br>La oferta del Inmueble aquÃ­ ofrecido, es a solo titulo informativo, pues la Venta de la Propiedad, estÃ¡ supeditada a que el propietario cumplimente el trÃ¡mite ante la AFIP para la obtenciÃ³n del COTI.
<br>
<br>"	Casa	Venta
699972	Cc8bVzOhRcPnAYS++8oyMg==	Propiedad	07-01-2020	07-01-2020	07-01-2020	-31.6351728	-60.7160724	Argentina	Santa Fe					4	3	4			34000	ARS	Mensual	Casa en Alquiler en Constituyentes, Santa fe $ 34000	"ALQUILER DE CASA DE 3 / 4 DORMITORIOS EN ZONA AV. FREYRE.
EXCELENTE CASA CON 4 DORMITORIOS, GRAN LIVING COMEDOR, COCINA COMEDOR, 4 BAÃ‘OS, ESCRITORIO, LAVADERO, GRAN FONDO CON PISCINA, QUINCHO COMPLETO CON BAÃ‘O Y COCINA, Y COCHERA PARA 1 AUTO.
Comercializa:
MIGONE Inmobiliaria - 1Âº de Mayo NÂº2539 Â• Santa Fe - Tel. 0342 - 4536857 // 4526317 - www.migoneinmobiliaria.com.ar

 XINTEL(MIG-MIG-3296)"	Casa	Alquiler
66130	83DDzQ7686eLxOi9sQNJVA==	Propiedad	13-05-2020	17-05-2020	13-05-2020			Argentina	Santa Fe	Rosario				9	9	2	200	200	20000	ARS		Laprida 1418	Laprida 1418 - KP27922 -  - Aviso publicado por KiteProp CRM Inmobiliario	Casa	Alquiler
83989	lA5sBjVvZbpu9tqYTRmI9Q==	Propiedad	14-01-2021	31-12-9999	14-01-2021	-31.355595	-64.3227122	Argentina	CÃ³rdoba	La Calera									72000	USD	Mensual	LA DESEADA -  LOTE 1300 Mts - IMPERDIBLE!!!	OLSEN Propiedades tiene el agrado de presentarte esta oportunidad de inversiÃ³n.<br><br>Se trata de un lote ubicado en Country LA DESEADA!!! Zona mÃ¡s cotizada en estos Ãºltimos aÃ±os - Rodeada de otros Countrys como: La Rufina - Las Delicias - Cinco Lomas - El Bosque, entre otros..<br><br>Lote de 1300 m2 <br><br>*POSESIÃ“N INMEDIATA<br><br>AdemÃ¡s posee:<br>- Calles asfaltadas y cunetas<br>- Servicios SubterrÃ¡neos<br>- Espacios verdes<br>- Ãreas deportivas y comerciales<br>- Seguridad las 24hs.<br><br>EXCELENTE OPORTUNIDAD!!!<br><br>NO DUDES EN CONSULTARNOS...<br><br>OLSEN Propiedades<br>CPI: 4732	Lote	Venta
461444	4FwVy3iWEy3R/rccYuHlYw==	Propiedad	03-11-2020	31-12-9999	03-11-2020	-34.6555008	-58.4980694	Argentina	Capital Federal	Mataderos				1		1	51	30	61900	USD	Mensual	PRE POZO 1 AMB- Mataderos	Venta de Pre-Pozo Mataderos, CABA<br><br>Monoambiente divisible en planta baja con patio<br>Cocina integrada<br>BaÃ±o completo<br>Patio amplio de 20 m2<br><br>FORMA DE PAGO: 30% CONTADO, 20% COMIENZO OBRA, SALDO 30 MESES<br>POSIBILIDAD VENTA EN PESOS: 50% BOLETO SALDO 14 MESES CON CLAUSULA<br>CAC<br><br>CIFARELLI | constructora - inmobiliaria M.N. 6199<br>Lunes a Viernes de 10 a 13 y 15 a 19 | SÃ¡bados 10 a 13<br>CÃ³digo de la propiedad: CAP3203863<br>Las medidas son aproximadas	Departamento	Venta
399905	gRldCIB6Yo0pALjex3q2YA==	Propiedad	11-03-2020	11-03-2020	11-03-2020	-37.9614098	-57.6217555	Argentina	Buenos Aires Costa AtlÃ¡ntica	Mar del Plata						1			8500	ARS	Mensual	PP  PH de un ambiente amplio con patio	Ph de un ambiente comodo, cocina semi integrada, baÃ±o con ducha, espacio para lavarropas, patio.  Sin mascotas.  Ubicado en calle San Martin 5300, valor $8500. Requisitos: Demostracion de ingresos comprobables de quien alquile, garantes con recibos de sueldo.   Ref#451020.	Otro	Alquiler
212340	2OMatxA5CX9Tf/vC5UgAvQ==	Propiedad	13-11-2020	20-11-2020	13-11-2020	-32.8580246	-60.70351791	Argentina	Santa Fe	Granadero Baigorria				2		1	400	38	15000	ARS		Calfucura   700 - $ 15.000 - Casa Alquiler	BARRIO:  Martin Fierro       â€“ Granadero Baigorria  /      UBICACIÃ“N:    CALFUCURA  NÂº 760  -    Granadero Baigorria.DESCRIPCION: LIVING â€“ COCINA COMEDOR -  DOS DORMITORIOS GRANDES, BAÃ‘O TERRENO AMPLIO â€“ INGRESO PARA VARIOS AUTOS -GAS ENVASADO -*VALOR ALQUILER  :    $    15.000    -  INCLUIDO  TGI â€“ INMOBILIARIOCONTRATO :     36 MESES 	Casa	Alquiler
557403	Fjyrj6Na/s09yGUbEpmVWg==	Propiedad	22-10-2020	31-12-9999	22-10-2020	-32.94153976	-60.64687347	Argentina	Santa Fe	Rosario				2		1	86		168541	USD		Italia   500 - U$D 168.541 - Departamento en Venta	ITALIA 519Monos, 1 y 2 dormitorios de calidadEdificio de calidad en una increÃ­ble zona de vivienda.ALFONSO IIIDepartamentos de calidad a pasos del centro y orientados hacia una buena arquitectura con ambientes amplios y funcionales, pensados para una vida activa. Unidades monoambientes, 1 y 2 dormitorios. OpciÃ³n cochera en PB. Posibilidad de ver Showroom. Calidades excelentes con pisos de primer nivel (porcelanato o madera de ingenierÃ­a), amueblamientos de cocina con alacena y bajo mesada, bacha de acero inoxidable, equipamiento elÃ©ctrico en cocina, anafe y agua caliente, aberturas de aluminio lÃ­nea MÃ³dena o similar con puertas corredizas y cortinas de enrollar de PVC, bacha de acero de inoxidable Johnson, frentes de placar colocados MDF o espejo con correderas de aluminio, instalaciÃ³n prevista para equipos de aire acondicionado frio-calor, artefactos de baÃ±o Ferrum o roca o similar, griferÃ­as de primeras marcas.ObservaciÃ³n: Showroom disponible. Edificio elÃ©ctrico. OpciÃ³n cochera.MÃ©todo de pago: Contado (10% descuento) â€“ FinanciaciÃ³n 30% mÃ¡s 30 cuotas en pesos ajustadas al ICAC.Piso 786mÂ²U$D 168.541Piso 886mÂ²U$D 173.222	Departamento	Venta
125994	+NJLrdSszAtC0y8owU4L1Q==	Propiedad	08-09-2020	09-10-2020	08-09-2020	-38.0044359	-57.549473	Argentina	Buenos Aires Costa AtlÃ¡ntica	Mar del Plata				3	2	1			130000	USD		Excelente departamento 3 Amb. Centro	"Excelente departamento 3 ambientes reciclado en zona centro, el mismo cuenta con:<br />
&bull; 2 dormitorios<br />
&bull; Ba&ntilde;o completo reciclado<br />
&bull; Cocina separada Reciclada<br />
&bull; Living-Comedor<br />
&bull; Hall<br />
&iexcl;Cabe destacar que el departamento tiene muy buena luminosidad!<br /><br />
  <br />
 Ref#369510."	Departamento	Venta
286125	MHKXmMebWltIJJEJdkJ2MQ==	Propiedad	02-01-2020	18-06-2020	02-01-2020	-34.4827631	-58.55605555	Argentina	Bs.As. G.B.A. Zona Norte	San Isidro				3		1	81	60	25000	ARS	Mensual	BUENA OFICINA PARA USO PROFESIONAL O VIVIENDA	OFICINA PARA USO PROFESIONAL O VIVIENDA.<br>PB: Cochera semi cubierta. Afuera hay otra cochera.<br>PA: Por escalera, salÃ³n central/living. Cocina con balcÃ³n. BaÃ±o completo. 1 privado con balcÃ³n y otro privado tipo sala de reuniÃ³n. Hay parrilla por escalera en terracita. 3 splits frÃ­o/calor.<br>MEDIDAS: Sup.Cub: 60 m2 - Desc: 10 m2 -  Semicub: 21 m2 - Total: 81 m2 aprox.<br><br>Martillero Responsable: Pablo Hyland C.S.I: 4799	Oficina	Alquiler
67317	TGsflWdYuPmxLqt/20Uj6g==	Propiedad	02-01-2021	04-01-2021	02-01-2021	-37.32691196	-57.03264007	Argentina	Buenos Aires Costa AtlÃ¡ntica	Mar de las Pampas				4	3	3			127000	ARS		MAR DE LAS PAMPAS - ALQUILER - Hermosa cabaÃ±a con pileta de nataciÃ³n, juegos infantiles en maravilloso entorno	"<b>MAR DE LAS PAMPAS - ALQUILER - Hermosa cabaÃ±a con pileta de nataciÃ³n, juegos infantiles en maravilloso entorno</b><br><br>En Mar de las Pampas, en calle El Lucero y Jos&eacute; M&aacute;rmol, enmarcada en un entorno de variada vegetaci&oacute;n y frondosa arboleda, que brindan gran privacidad al lugar,  en un cuidado y muy espacioso jard&iacute;n, encontramos esta c&aacute;lida caba&ntilde;a, donde cada &aacute;rea tiene su peculiar encanto... <br />
Tiene pileta de nataci&oacute;n ( 7,5 m de largo) con contenci&oacute;n de rejas, donde la familia disfruta el mayor tiempo posible... en su lateral,  una galer&iacute;a techada y con deck, con c&oacute;modos sillones y un rinc&oacute;n dedicado a los ni&ntilde;os, con casita, finamente decorada, impecable, con hamacas y juegos para colgarse...Para gozar de un verano totalmente diferente...<br />
En Planta baja, al ingresar, tenemos en un espacio apartado, un living, con c&oacute;modos sillones, plasma, ideal para pasar en compa&ntilde;&iacute;a o a solas, con la lectura o la tv.<br />
Tenemos cocina semi integrada y un comedor que pasa directamente al quincho con gran parrilla y horno de barro, con una vasta mesa con banco continuo, que brinda lugar para 20 personas, aproximadamente.<br />
Continuando con la planta baja, tenemos una habitaci&oacute;n matrimonial y 1 ba&ntilde;o completo.<br />
En planta alta, hay una habitaci&oacute;n con 2 camas y otra con tres, m&aacute;s otro ba&ntilde;o completo.<br />
En el exterior,  tambi&eacute;n hay un ba&ntilde;o para ducharse y un lavadero con lavarropas autom&aacute;tico nuevo.<br />
Es una caba&ntilde;a especialmente dise&ntilde;ada para sentirse pleno, feliz...alejado del estr&eacute;s, solo en contacto con la paz y el silencio...Ideal para que los ni&ntilde;os disfruten de la libertad!!! <br />
Los autos pueden ingresar al estacionamiento en l&iacute;nea contigua al jard&iacute;n. <br />
1&deg; QUINCENA DE ENERO: LIBRE - <br />
2&deg; QUINCENA ENERO : OCUPADA D<br />
1&deg; QUINCENA FEBRERO:   OCUPADA DEL 1 al 15 <br />
2&deg; QUINCENA FEBRERO: LIBRE <br />
VALOR SEMANAL:  $ 127.000.- VALOR QUINCENA : $ 234.000.<br />
<br /><br><br> CaracterÃ­sticas adicionales: <br> - DesagÃ¼e cloacal<br>- Luz<br>- Toilette<br>- Vajilla<br>- Deck<br>- GalerÃ­a<br>- Gas Envasado<br>- Pozo negro<br>- Agua Potable<br> <br><br> Ref#631920."	Casa	Alquiler
459884	vyK2LKZIjrQHXvVB9GFGLw==	Propiedad	03-11-2020	09-11-2020	03-11-2020	-34.6011033	-58.4177368	Argentina	Capital Federal	Almagro				1		1			24000	ARS		SALGUERO PROPIEDADES ALQUILA 1 AMB/ C BALCÃ“N EN ALMAGRO	"<b>SALGUERO PROPIEDADES ALQUILA 1 AMB/ C BALCÃ“N EN ALMAGRO</b><br><br>Se alquila monoambiente totalmente equipado en Almagro.<br />
<br />
-Cocina separada a gas.<br />
- Ba&ntilde;o completo con recept&aacute;culo.<br />
-Equipado para 1 persona.- Muebles, tv led-mesa, sillas, vajilla, ropa de cama.<br />
-Excelente ubicaci&oacute;n.<br />
-Balc&oacute;n al frente.<br />
-Excelente luminosidad.<br />
-<br />
<br />
-Contrato x 3 meses con opci&oacute;n de renovar.<br />
-Ingreso: 1 mes de adelanto, 1 mes de dep&oacute;sito, 10% del total del contrato honorarios profesionales.<br />
-Requisitos: Recibos de sueldo.<br />
-Capacidad m&aacute;xima 2 personas<br />
<br />
Vanesa Ibarra MN 5619<br />
<br />
â˜Ž 4864-2117 <br />
Celular : 1144772330<br />
<br /><br><br> CaracterÃ­sticas adicionales: <br> - Agua corriente<br>- DesagÃ¼e cloacal<br>- Luz<br>- Apto profesional<br> <br><br> Ref#477054."	Departamento	Alquiler temporal
388640	zXvfgApmjh1Bf4os5/sU/w==	Propiedad	03-07-2020	28-08-2020	03-07-2020	-34.38594055	-58.86029053	Argentina	Bs.As. G.B.A. Zona Norte	Pilar				3		3	114	114	140000	USD		San Ramiro Al Lote / NÂ° 390 - U$D 140.000 - Casa en Venta	Muy linda casa en lote interno en San Ramiro.Desarrollada en 1 planta. Living comedor  apaisado sobre gran galerÃ­a con parrillaCocina integrada con una barra.3 dormitorios1 dormitorio en suite con vestidor2 dormitorios mas un baÃ±o completoToiletteLavaderoPisos de porcelanatoMesadas de granito grisCalefacciÃ³n por radiadores con caldera dual.Aberturas Modena DVHExpensas Abril 2019 $5000Lote central con fondo a espacio comÃºn (sin vecinos en el fondo) y prÃ³ximo a la plaza central con juegos para niÃ±os.CMCPSI 6421Fotos by HOMERSPara mÃ¡s informaciÃ³n, llÃ¡manos al: 01137674766.Aviso publicado por YS your broker desde Sumaprop.	Casa	Venta
![image](https://github.com/neelamdeka20/DataGrokr_project/assets/137504853/f21b513c-103c-4e9d-9a12-c4921670baec)
