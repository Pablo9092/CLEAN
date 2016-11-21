## ARQUITECTURA CLEAN ##

Esta arquitectura surge por el problema al ver que se implementaba mas codigo para la representación de un  
fragment, que para su función. El autor de esta arquitectura esel Tio Bob y el nos nos dice, que mas que una  
arquitectura es un conjunto de condisiones que se deben cumplir, para poder considerar una arquitectura limpia.  
Alfinal estas condisiones dividiran el software en capas.  

![](clean-architecture-diagram.png "Arquitectura CLEAN")

####Definicion de las capas en el proyecto####

**Capa del domino:** Esta capa no tiene acceso al fragment del android, esta enfocada al codigo java solamente.
Esta capa es la capa mas importante, ya que es la encargada de hacer los casos de usos(interacciones) y las  
entidades.  
**Capa de presentación:** Es la encargada de conectar el dominio con el UI. No depende del fragment de android  
y solo contiene java puro. Ademas contendra mappers que permita adaptar modelos de datos a la capa que los reciba.  
**Capa Framework:** Esta capa depende del framework de android y se divide en dos modulos:  
1. **android** donde estara el código de las vistas, fragments o cualquier librería que dependa del framework.  
2. **data** es la fuente de datos, donde optiene la información.  




