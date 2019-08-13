#PRÁCTICA Nº 1

###Carrera: Ingenieria de Sistemas                        
______________________
###Materia: Tegnologías Emergentes II
______________________
###Apellidos y Nombres: Mamani Luna Ximena Belen
______________________
###C.I: 9233782L.P.
______________________

#1¿explique que son los sistemas empresariales?
Son un conjunto integrado de sistemas de información que son herramientas que unifican los procesos que se llevan a cabo de una empresa por medio de software y hardware.
Un Sistema de Información Empresarial es un sistema que tiene un
impacto muy importante en el funcionamiento de la organización o
negocio y cuya falla traería graves consecuencias.

Normalmente que ofrece alta calidad de servicio, gestiona con
grandes volúmenes de datos, disponible de forma continua y es
capaz de soportar cualquier organización grande.
#2 describa cuales son las características más importantes de una aplicación empresarial
- Tiene acceso a la base de datos 
- Operaciones transaccionales
- Escalables  (vertical y horizontal)
- Arquitectura multicapa
- Permiten integración con otras tecnologías
 Arquitectura multicapa.
#3 investigue y proponga 5 instituciones que requieran aplicación de misión critica

#4 explique cuáles son las diferencias entre la escalabilidad horizontal y escalabilidad vertical

La diferencia es que uno aumenta el número de componentes mientras que el otro actualiza y moderniza los componentes ya existentes.

**Escabilidad vertical:**

**Ventajas:**

   - No implica un gran problema para las aplicaciones, pues todo el cambio es sobre el hardware
   - Es mucho más fácil de implementar que el escalamiento horizontal.


**Desventajas:**

- El crecimiento está limitado por el hardware.
- Una falla en el servidor implica que la aplicación se detenga.
- No soporta la Alta disponibilidad.


**Escabilidad horizontal:**

**Ventajas:**


- El crecimiento es prácticamente infinito, podríamos agregar cuantos servidores sean necesarios.
- Es posible combinarse con el escalamiento vertical.
- Soporta la alta disponibilidad.


**Desventajas:**

- Requiere de mucho mantenimiento.
- Es difícil de configurar.
#5 que es un servidor web y que es un servidor de aplicaciones
Servidor web -  es una computadora que formando parte de una red provee servicios a otras computadoras denominadas clientes 
Servidor de aplicaciones-  es un dispositivo de software que proporcionan servicios de aplicaciones a las computadoras cliente
#6 con un gráfico explique cómo funciona el protocolo HTTP

![](https://huguidugui.files.wordpress.com/2013/10/peticion.png)


#7 explique los elementos importantes de RESQUEST en HTTP
HTTP Metodo la acción a reslizar
La pagina pagina para acceder a URL
Forma parámetros los argumentos del metodo

#8 explique los elementos importantes de RESPONSE en HTTP

- Codigo de estado (status code): indica si la operacion fue realizada correctamente o no .
- tipo de contenido (content type):si el contenido es HTML , una imagen,un archivo PDF, etc.
- contenido : el HTML , la imagen, etc.

#9 describa con un grafico la arquitectura de JAVA EE

![](https://image.slidesharecdn.com/jatunandjavaee-110905104600-phpapp02/95/desarrollo-de-aplicaciones-empresariales-con-java-ee-4-728.jpg?cb=1316098712)

#10 explique cuáles son los conectores, componentes y servidores de JAVA EE
- Conectores :son un torno de ejecución que provee componente una serie de servicios 

- Componentes: Son una unidad de software de la parte de aplicaciones y 
existen componentes de cliente, web y negocio.
- Servidores  ofrecen conectadores de JAVA EE. Son de directorio, despliegue, transaccionalidad, seguridad y acceso de datos.

#11 investigue los métodos mas utilizados de las clases HTTPSERVLET, HTTPSERVLETRESQUEST y httpservletresponse y para cada uno muestre un ejemplo



**public abstract interface Servlet:** Todos los servlets implementan este interfaz directamente o extendiendo una clase que lo implemente como HttpServlet. Entre sus métodos están:

- **init(ServletConfig config):** Es el método utilizado para crear una nueva instancia del servlet (análogo al constructor). Ver el ciclo de vida. Este método puede ser sobreescrito para realizar tareas como crear una conexión a una BD que se mantendrá mientras el servlet se mantenga cargado y puede ser utilizada por cada petición. ServletConfig contiene los parámetros de inicialización que entrega el servidor al servlet.
   
- **getServletConfig():** Retorna la configuración dada para la inicialización del servlet.
   
- **service(ServletRequest req, ServletResponse res):** Este método es el que se llama cuando se recibe una petición de un cliente y en su implementación normal para HTTP verifica el tipo de solicitud GET, POST, etc. y la redirige a los métodos respectivos. En general no es necesario reimplementar este método.
   
- **destroy():** Este método es llamado por el servidor para indicar que el servlet será destruido. Es llamado sólo una vez y uno debe encargarse de esperar por posibles peticiones en curso.


---------------------------------------------------------
**public abstract interface ServletRequest:** Permite obtener información del cliente que no depende del protocolo, por ejemplo:

- **getRemoteAddr():** Retorna la IP del cliente.
- **getParameter(String name):** Retorna el valor del parámetro name dado por el cliente.
- **getInputStream():** Sirve para crear un canal de comunicación para obtener dados binarios.

**public abstract interface HttpServletRequest extends ServletRequest:** Permite obtener del cliente la información que es dependiente del protocolo, en este caso HTTP. Entre sus métodos están:

- **getHeader(String name):** Permite obtener el valor de los Headers de HTTP con que fue llamado el servlet.
- **getCookies():** Retorna un arreglo que contiene todas las cookies que el cliente envía al servlet.
- **getSession():** Retorna la sesión en la cual se encuentra el cliente.

--------------------------------------------------------

**public abstract interface ServletResponse:** Define un objeto para permitir a un servlet enviar una respuesta al cliente.

- **setContentType(String type):** Permite definir el tipo de respuesta que se le dará al cliente. Si se retornará una página web deberá ser text/html.
- **getWriter():** Retorna un objeto Writer para poder enviar respuestas de texto.
- **getOutputStream():** Retorna un objeto ServletOutputStream que permite enviar respuestas binarias al cliente.

**public abstract interface HttpServletResponse extends ServletResponse:** Permite enviar al cliente respuestas específicas del protocolo HTTP.

- **addCookie(Cookie cookie):** Para definir nuevas cookies en el cliente.
- **setHeader(String name, String value):** Para definir un header HTTP a enviar al cliente.
- **sendRedirect(String location):** Envía un mensaje al cliente para redireccionar la respuesta a la dirección señalada
  
