# Diccionario de Datos

Para el desarrollo del análisis se proporcionaron los siguientes dataset para la realizacion del proyecto:

- Indicadores_del_desarrollo_humano_mundial: Banco Mundial Indicadores de desarrollo humano.
- Console_sales: Reporte de ventas anuales de consolas. por marca y modelo.
- Juegos en steam: Reporte con estadísticas de uso de juegos en Steam. Incluye recomendaciones tiempo de uso, etc.
- Video Games Sales: Reporte de ventas por Video Juego y Plataforma. Incluye ranking y apertura por mercados (NA, EU, Japón y Global)

Sin embargo, no se proporcionó un diccionario de datos con el cual trabajar, por lo que me tomé la labor de redactar este documento con una breve descripción de cada Dataset y de los datos que incluyen.

## Índice de Desarrollo Humano

Este dataset contiene una extración de datos del Índice de Desarrollo Humano (IDH). El IDH es un indicador creado por el Programa de las Naciones Unidas para el Desarrollo (PNUD) que, desde hace tres décadas, da a conocer el grado de progreso de cada país. En este caso, el dataset esta compuesto por 237 columnas, 24 filas y contiene información respecto a 58 indicadores, y por cada indicador, hay cuatro filas, cada una reflejando información de una determianda región: Estados unidos, Japón, Unión Europea y el resto del Mundo.

Por cada registro se describe lo siguiente:

- **Series Name**: Nombre de la Serie o indicador.
- **Series Code**: Código de la Serie o indicador.
- **Country Name**: Nombre del País o Región, a los cuales hace referencia los datos de la fila.
- **Country Code**: Código del País o Región.
- **2000 [YR2000] - 2019 [YR2019]**: 19 columnas con los datos obtenidos en cada año. Una columna por cada año desde el 2000 hasta el 2019.

### Ejemplo de los datos

|index|Series Name|Series Code|Country Name|Country Code|2000 \[YR2000\]| ... |2019 \[YR2019\] |
|---|---|---|---|---|---|---|---|
|0|Superficie \(kilómetros cuadrados\)|AG\.SRF\.TOTL\.K2|Estados Unidos|USA|9632030|...|
|1|Superficie \(kilómetros cuadrados\)|AG\.SRF\.TOTL\.K2|Unión Europea|EUU|4384964\.9951171875|...|
|2|Superficie \(kilómetros cuadrados\)|AG\.SRF\.TOTL\.K2|Japón|JPN|377800|...|

<br />

## Videojuegos de Steam

Este dataset proporciona información sobre el mercado de videojuegos dentro de la plataforma de ventas Steam. Esta es la plataforma de venta de videojuegos de PC más importante del mundo, por lo que toda la información provista está relacionada con el mercado de videojuegos para PC. El Dataset posee un total de 27075 filas, 18 columnas y cada registro proporciona la siguiente información:

- **appid**: ID del título en el conjunto de datos.
- **name**: Nombre del videojuego.
- **release_date**: Fecha de lanzamiento.
- **publisher**: Distribuidora.
- **english**: Indica si el título está disponible en inglés. 1 si es sí, 0 si no.
- **categories**: Categorías a las que pertenece el videojuego.
- **genres**: Género del videojuego.
- **steamspy_tags**: Etiquetas de Steam.
- **achievements**: Número de logros que tiene el juego.
- **positive_ratings**: Valoraciones positivas.
- **negative_ratings**: Valoraciones negativas.
- **average_playtime**: Promedio de horas totales jugadas por los usuarios.
- **median_playtime**: Mediana de horas totales jugadas por los usuarios.
- **owners**: Rango categórico de usuarios que han comprado el juego.
- **price**: Precio de venta.

### Ejemplo de los datos

|index|appid|name|release\_date|english|developer|publisher|platforms|required\_age|categories|genres|steamspy\_tags|achievements|positive\_ratings|negative\_ratings|average\_playtime|median\_playtime|owners|price|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|0|10|Counter-Strike|2000-11-01|1|Valve|Valve|windows;mac;linux|0|Multi-player;Online Multi-Player;Local Multi-Player;Valve Anti-Cheat enabled|Action|Action;FPS;Multiplayer|0|124534|3339|17612|317|10000000-20000000|7\.19|
|1|20|Team Fortress Classic|1999-04-01|1|Valve|Valve|windows;mac;linux|0|Multi-player;Online Multi-Player;Local Multi-Player;Valve Anti-Cheat enabled|Action|Action;FPS;Multiplayer|0|3318|633|277|62|5000000-10000000|3\.99|
|2|30|Day of Defeat|2003-05-01|1|Valve|Valve|windows;mac;linux|0|Multi-player;Valve Anti-Cheat enabled|Action|FPS;World War II;Multiplayer|0|3416|398|187|34|5000000-10000000|3\.99|

<br />

## Venta de Videojuegos

Este dataset incluye información referente a la ventas de los titulos lanzados desde 1985 hasta la actualidad. El dataset está compuesto por 16719 filas, 16 columnas y cada registro describe los siguientes siguientes:

- **Name**: Nombre del videojuego.
- **Platform**: Plataforma en la cual se publicó el videojuego. Incluye portátiles, consolas de sobremesa y PC.
- **Year_of_Release**: Año de lanzamiento.
- **Genre**: Género del videojuego.
- **Publisher**: Distribuidora.
- **NA_Sales**: Ventas en América del Norte en milllones (NA).
- **EU_Sales**: Ventas en la Unión Europea en milllones (EU).
- **JP_Sales**: Ventas en Japón en milllones (JP).
- **Other_Sales**: Ventas en el resto del mundo en milllones.
- **Global_Sales**: Ventas globales en milllones.
- **Critic_Score**: Puntuación promedio de la crítica.
- **Critic_Count**: Cantidad de críticos que han dado puntuación.
- **User_Score**: Puntuación promedio de los usuarios.
- **User_Count**: Cantidad de usuarios que han votado.
- **Developer**: Desarrolladora del videojuego.
- **Rating**: Clasificación por edad del videojuego. El rating provisto se basa en el sistema de clasificación estadounidense de contenido de videojuegos ESRB (Entertainment Software Rating Board).

### Ejemplo de los datos

|index|Name|Platform|Year\_of\_Release|Genre|Publisher|NA\_Sales|EU\_Sales|JP\_Sales|Other\_Sales|Global\_Sales|Critic\_Score|Critic\_Count|User\_Score|User\_Count|Developer|Rating|
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
|0|Wii Sports|Wii|2006\.0|Sports|Nintendo|41\.36|28\.96|3\.77|NaN|82\.53|76\.0|51\.0|8|322\.0|Nintendo|E|
|1|Super Mario Bros\.|NES|1985\.0|Platform|Nintendo|29\.08|3\.58|6\.81|0\.77|40\.24|NaN|NaN|NaN|NaN|NaN|NaN|
|2|Mario Kart Wii|Wii|2008\.0|Racing|Nintendo|15\.68|12\.76|3\.79|3\.29|35\.52|82\.0|73\.0|8\.3|709\.0|Nintendo|E|

<br />

## Venta de Consolas

Este dataset proporciona información sobre el mercado de consolas de sobremesa y portátiles, por marca y modelo. Está compuesto por 85 filas y 5 columnas, y cada registro describe los siguiente aspectos:

- **Year**: año en el que se realizaron las ventas.
- **Dato**: "Anual" si el registro representa el número de ventas anuales del producto o "Out_of_use" si el producto ya no se encuentra en venta.
- **Console**: nombre de la consola.
- **Company**: compañía propietaria del producto.
- **Sales**: número total de ventas realizadas. En caso de que el campo Dato sea "Out_of_use", este campo representa el total de ingresos generados a lo largo de la historia del producto, expresado de forma negativa.

Los datos proporcionados abarcan desde el año 2008 hasta 2020, lo que los hace relativamente actuales. No se descartaron datos debido a su antigüedad, y todas las columnas se consideraron relevantes para el análisis, por lo que no se eliminó ninguna.

### Ejemplo de los datos

|index|Year|Dato|Console|Company|Sales|
|---|---|---|---|---|---|
|0|2011|anual|Nintendo 3DS|Nintendo|12560000\.0|
|1|2012|anual|Nintendo 3DS|Nintendo|13480000\.0|
|2|2013|anual|Nintendo 3DS|Nintendo|14310000\.0|
|3|2014|anual|Nintendo 3DS|Nintendo|9740000\.0|
|4|2015|anual|Nintendo 3DS|Nintendo|7330000\.0|
