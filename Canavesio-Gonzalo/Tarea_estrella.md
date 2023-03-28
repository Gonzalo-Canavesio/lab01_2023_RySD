Primero hay que explicar porque los nombres de dominio como los dados en el enunciado generarían algún problema y necesitan de nuevos mecanismos para funcionar.

Los Sistemas de Nombres de Dominio (DNS, siglas en inglés) son los encargados de traducir las direcciones web y direcciones IP, para que se visualicen en un navegador. Para ello utilizan código ASCII, por lo tanto los dominios solo pueden contener carácteres ASCII.

Pero estos dominios contienen carácteres no ASCII, como 文 o 💩. Para esos casos se generó el protocolo de "Nombre de dominio internacionalizado", que se basa en normalizar el dominio a uno codificado en ASCII que si pueda ser manejado por la existente infraestructura de resolución de nombres y DNS.

La conversión entre las formas ASCII y no-ASCII de un nombre de dominio se realiza mediante algoritmos llamados ToASCII y ToUnicode. ToASCII aplicará el algoritmo Nameprep y entonces se traducirá el resultado a ASCII usando Punycode antes de anteponer la cadena de cuatro caracteres "xn--". Esta cadena de cuatro caracteres se llama el prefijo ACE y se utiliza para distinguir las etiquetas codificadas en Punycode de las etiquetas ASCII ordinarias. 

Además de el uso del protocolo anterior, existe otro mecanismo más para tener en cuenta, que es el "codigo porciento" o el "url encode". Algunos carácteres ASCII están reservados porque tienen un significado especial y si los utilizaramos en la URL generaría ambiguedades. 

La codificación mediante "codigo prociento" consiste habitualmente en el signo "%" seguido del número hexadecimal ASCII correspondiente al carácter codificado. Esa combinación de 3 caracteres (%XX, donde X es un caracter hexadecimal). Los únicos caracteres ASCII que no generan problema y que no tienen significado especial son las letras mayúsculas y minúsculas del alfabeto sin signos diacríticos, los números de 0 a 9, más los signos "-", "_", "." y "~".

Referencias:
- https://es.wikipedia.org/wiki/C%C3%B3digo_porciento
- https://es.wikipedia.org/wiki/Nombre_de_dominio_internacionalizado
- https://www.w3schools.com/tags/ref_urlencode.ASP
- https://www.ionos.es/digitalguide/dominios/gestion-de-dominios/idn-que-es-un-nombre-de-dominio-internacionalizado
- https://bunny.net/academy/http/what-is-url-uniform-resource-identifier-and-percent-encoding