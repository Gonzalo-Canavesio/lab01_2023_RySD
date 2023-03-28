# Informe Proyecto 1
Para conectarse a un server no ASCII, el cual solo permite representar 128 caracteres, se utiliza una especificacion (encoding - unicode) la cual permite poder codificar mucho mas caracteres.
Este encoding se maneja para poder evitar problemas de codificacion y decifrado de datos. Muchos protocolos solo soportan ASCII por lo cual impide que aplicaciones de red que empleen los propios protocolos, por lo cual existe un metodo llamado *IDNA* (nternationalizing Domain Names in Applications) este permite que se intreprenten aquellos caracteres que no son ASCII.
Con *IDNA*, los nombres de dominio pueden contener caracteres no ASCII al convertir los caracteres no ASCII en una secuencia de caracteres ASCII que se puede utilizar en la web. *En IDNA, el proceso de convertir un nombre de dominio no ASCII en una secuencia de caracteres ASCII se denomina "punycode"*. El proceso de *punycode* se utiliza para codificar los caracteres no ASCII de un nombre de dominio en una secuencia de caracteres ASCII que es aceptable para los sistemas de nombres de dominio y otros protocolos de Internet.

Referencias:
https://en.wikipedia.org/wiki/Internationalized_domain_name