# Escuela Colombiana de Ingeniería Julio Garavito - Arquitecturas Empresarial AREP - Cuarto Trabajo

## TALLER DE ARQUITECTURAS DE SERVIDORES DE APLICACIONES, META PROTOCOLOS DE OBJETOS, PATRÓN IOC, REFLEXIÓN
### DESCRIPCIÓN
Para este taller los estudiantes deberán construir un servidor Web (tipo Apache) en Java. El servidor debe ser capaz de entregar páginas html e imágenes tipo PNG. Igualmente el servidor debe proveer un framework IoC para la construcción de aplicaciones web a partir de POJOS. Usando el servidor se debe construir una aplicación Web de ejemplo y desplegarlo en Heroku. El servidor debe atender múltiples solicitudes no concurrentes.

Para este taller desarrolle un prototipo mínimo que demuestre capcidades reflexivas de JAVA y permita por lo menos cargar un bean (POJO) y derivar una aplicación Web a partir de él. Debe entregar su trabajo al final del laboratorio.

SUGERENCIA
1.Cargue el POJO desde la línea de comandos , de manera similar al framework de TEST. Es decir pásela como parámetro cuando invoke el framework. Ejemplo de invocación:

java -cp target/classes co.edu.escuelaing.reflexionlab.MicroSpringBoot co.edu.escuelaing.reflexionlab.FirstWebService
2. Atienda la anotación @ResuestMapping publicando el servicio en la URI indicada, limítelo a tipos de retorno String,  ejemplo:

public class HelloController {

	@RequestMapping("/")
	public String index() {
		return "Greetings from Spring Boot!";
	}
}
## Diseño

  Diseño de la aplicación
  
  ![Diseño1](https://github.com/nicolasOL/Interpretes-canales-de-comunicacion-y-memoria/blob/master/images/diagrama1.jpg)
  ![Diseño2](https://github.com/nicolasOL/Interpretes-canales-de-comunicacion-y-memoria/blob/master/images/diagrama2.jpg)
  

## Guia

## Cuenta con 
* [Heroku](https://heroku.com) - Despliegue web [![Deploy](https://www.herokucdn.com/deploy/button.png)](https://icm-arep.herokuapp.com/)
* [Circle CI]() - Integración Continua ![CircleCI](https://circleci.com/gh/nicolasOL/Interpretes-canales-de-comunicacion-y-memoria.svg?style=svg&circle-token=042c0e4d804fd47371e80dbb9853f71792a77e30)
  
  ### Requisitos
  
  Si deseas usarlo en tu maquina local, es necesario tener:
  
  * Maven 
  * Java 
  * Git
  
  

 ### Como usarlo?
  ## Localmente:
  En primer lugar vamos a descargar el repositorio en nuestra máquina local, y en la carpeta de 
nuestra preferencia. En consola vamos a digitar el siguiente comando para clonar el repositorio.

```
git clone https://github.com/nicolasOL/Interpretes-canales-de-comunicacion-y-memoria
```

Entremos a el directorio del proyecto

```
cd icm-arep
```

Debemos compilar el proyecto, que contiene las clases necesarias para poder correr la app. Por medio de maven vamos a crear todos los compilables **.class**. Desde consola, y ubicados en la carpeta donde se encuentra nuestra configuración de maven.

```
mvn compile
```

Ahora que nuestras clases etan compiladas vamos a ejecutar la clase principal para
ver el código en acción :

```
mvn exec:java -Dexec.mainClass="edu.escuelaing.arem.icm.arep.icmApp"
```
Los datos del programa se reciben por entrada en el despliegue separados por espacios.
   
## Pruebas   
Para ejecutar las pruebas es necesario ejecutar:
```
mvn test
```      
Las pruebas van a ser ejecutadas con los dos datasets adjuntos:

![test1](https://github.com/nicolasOL/Interpretes-canales-de-comunicacion-y-memoria/blob/master/images/1.JPG)

![test2](https://github.com/nicolasOL/Interpretes-canales-de-comunicacion-y-memoria/blob/master/images/2.JPG)

![test3](https://github.com/nicolasOL/Interpretes-canales-de-comunicacion-y-memoria/blob/master/images/3.JPG)

Esperamos obtener los siguientes resultados:

![test4](https://github.com/nicolasOL/Interpretes-canales-de-comunicacion-y-memoria/blob/master/images/4.JPG)    


Pruebas ejecutandose satisfactoriamente:

![test5](https://github.com/nicolasOL/Interpretes-canales-de-comunicacion-y-memoria/blob/master/images/5.JPG)

     
    
## Documentacion
  
Para encontrar toda la documentación relacionada puedes hacer click [aqui](https://github.com/nicolasOL/Interpretes-canales-de-comunicacion-y-memoria/tree/master/docs)
  
  ## Author
  
  Nicolas Ortega Limas
  
  ## License
  
  This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](https://github.com/nicolasOL/Interpretes-canales-de-comunicacion-y-memoria/blob/master/LICENSE.txt)
