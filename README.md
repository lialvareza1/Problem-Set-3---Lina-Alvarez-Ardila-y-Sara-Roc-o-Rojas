# Problem-Set-3---Lina-Alvarez-Ardila-y-Sara-Roc-o-Rojas
Universidad de Los Andes - Big Data y Machine Learning - Lina Maria Alvarez y Sara Rocío Rojas

Los archivos presentados están referenciados en Google Colab para poder generar un codigo reproducible y público.

## Archivos principales

- Notebook 1: Estadísticas descriptivas.
- Notebook 2: Stacking y validación cruzada con Random Forest
- Notebook 3: Stacking Logit y CART.
- Notebook 4: Stacking con Super Learner Manual y Validación Cruzada Espacial. 
- Notebook 5: Modelo de Redes Neuronales Simples.
- Notebook 6: Modelo ganador de Random Forest

## Cargar los datos 

     ```r
     test <- read_csv("https://www.dropbox.com/scl/fi/seif0x3qoy95gh0s2nw0u/test.csv?rlkey=lqzviqjqxwatlt708bzoezsnc&st=csqy50ti&dl=1")
     train <- read_csv("https://www.dropbox.com/scl/fi/pnw43edk4uewsd13g1oxj/train.csv?rlkey=vxuc9vej4ruom9dg0y5b2zh0c&st=1zp7ez1e&dl=1")

     ```

## Especificación de las variables

| Variable                  | Tipo    | Descripción breve                                                    |
| ------------------------- | ------- | -------------------------------------------------------------------- |
| ...1                      | Integer | Índice o identificador auxiliar generado automáticamente.            |
| property\_id              | String  | Identificador único de la propiedad.                                 |
| city                      | String  | Ciudad donde está ubicada la propiedad.                              |
| price                     | Numeric | Precio de publicación de la propiedad (COP).                         |
| month                     | Integer | Mes de la publicación del anuncio.                                   |
| year                      | Integer | Año de la publicación del anuncio.                                   |
| surface\_total            | Numeric | Superficie total del inmueble (m²).                                  |
| surface\_covered          | Numeric | Superficie cubierta del inmueble (m²).                               |
| rooms                     | Integer | Número total de habitaciones (incluye dormitorios, salas, etc.).     |
| bedrooms                  | Integer | Número de dormitorios.                                               |
| bathrooms                 | Integer | Número de baños.                                                     |
| property\_type            | String  | Tipo de propiedad (ej: apartamento, casa, oficina, etc.).            |
| operation\_type           | String  | Tipo de operación (ej: venta, arriendo).                             |
| lat                       | Numeric | Latitud geográfica de la propiedad.                                  |
| lon                       | Numeric | Longitud geográfica de la propiedad.                                 |
| title                     | String  | Título del anuncio (texto libre).                                    |
| description               | String  | Descripción del anuncio (texto libre).                               |
| surface\_total\_imputed   | Numeric | Superficie total imputada (cuando falta el dato original).           |
| surface\_covered\_imputed | Numeric | Superficie cubierta imputada.                                        |
| rooms\_imputed            | Integer | Número de habitaciones imputado.                                     |
| bathrooms\_imputed        | Integer | Número de baños imputado.                                            |
| dist\_colegio             | Numeric | Distancia al colegio más cercano (metros).                           |
| dist\_parque              | Numeric | Distancia al parque más cercano (metros).                            |
| estrato\_manzana          | Integer | Estrato socioeconómico de la manzana.                                |
| num\_gastrobares\_500m    | Integer | Número de gastrobares a 500 metros.                                  |
| dummy\_remodelado         | Integer | Dummy: 1 si el inmueble dice estár remodelado en el anuncio, 0 si no.|
| dummy\_lujoso             | Integer | Dummy: 1 si el inmueble es “lujoso”, 0 si no.                        |
| dummy\_vista              | Integer | Dummy: 1 si el inmueble tiene “vista”, 0 si no.                      |
| dummy\_amoblado           | Integer | Dummy: 1 si el inmueble está amoblado, 0 si no.                      |
| longitud\_texto           | Integer | Longitud del texto del anuncio (número de caracteres).               |
| num\_palabras             | Integer | Número de palabras en el anuncio.                                    |
| num\_airbnb\_1500m        | Integer | Número de anuncios tipo Airbnb a 1500 metros.                        |
| date                      | Date    | Fecha de publicación del anuncio (combinación de año y mes).         |
| celda\_lat                | Numeric | Coordenada latitud discretizada para agrupación espacial (“celda”).  |
| celda\_lon                | Numeric | Coordenada longitud discretizada para agrupación espacial (“celda”). |
| celda                     | String  | Identificador único de celda espacial (lat\_lon concatenado).        |


## Autores

- Sara Rocio Rojas Goméz
- Lina María Álvarez Ardila


## Cita y referencias

Los métodos y parte del material están basados en:
- Sarmiento-Barbieri, I. (2025). Material de clase BDML, Universidad de los Andes.


---

