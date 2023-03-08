# Código y documentación M04-UF1
Cyberseguridad: Llenguatge de Marques, con el profesor Rafa Laguna

**Recordatorio** de subir las cosas al GitHub: git add -A .			git commit -m ""			git push

## Lenguaje de marcas

**Lenguaje de marcas** es un lenguaje que marca los contenidos por lo que son.

**NO** clasifica, almacena y transporta datos.

## XML

```XML 
<?xml version="1.0" enconding="UTF-8" ?>
<!-- COMENTARIO -->
<character>
	<name>Nombre</name>
	<surname>Apellido</surname>
	<age years="0" />
</character>
```

### Resumen

**XML** o **Lenguaje de Marcas Extensible**, es un lenguaje que describe y estructura super bien el contenido. 

Cuando abrimos un archivo **XML** al principio del codigo tendremos que poner → \<?xml version="1.0" enconding="UTF-8" ?>
Que básicamente dice que es un archivo *XML* con la codificación *UTF-8*.

Todo archivo XML, necesita una **etiqueta raíz**, una etiqueta donde dependen el resto de elementos, lo ideal es que represente algo y toda etiqueta raíz debe cerrarse. 

### Como usar XML

* Etiquetas pares:
	* Se abren y cierran, Cuando lo que tenemos que escribir es muy variable, puede ser par (character por ejemplo, o cuando algo vaya a contener muchos datos)
* Etiquetas impares:
	* Se cierran en sí mismas. Por ejemplo la edad, es una cosa muy concreta, entonces es recomendable hacerla impar.

Para comentar: \<!-- COMENTARIO -->

Una [WEB](https://desarrolloweb.com/manuales/18) o esta otra [WEB](https://aws.amazon.com/es/what-is/xml/) que explica todo de forma resumida.

## DTD

```DTD
<!ELEMENT character (name, surname?, age> <!-- el ? es que puede estar o no -->
<!ELEMENT name(#PCDATA)>
<!ELEMENT surname(#PCDATA)>
<!ELEMENT age EMPTY> <!-- algo o nada -->


<!ATTLIST character id_charater CDATA #REQUIRED>
<!ATTLIST age years CDATA #REQUIRED>
```

Este **DTD**, es una continuación del **XML** anterior.

### Resumen

Todo archivo DTL, necesita una **archivo XML**, ya que el DTL "clasifica" las etiquetas de XML, más bien dicho, los clasifica.

### Explicación de las etiquetas

* Primera etiqueta:
	* En esta etiqueta tenemos que poner la clasificación general de XML, que en este caso es character y poner las sub etiquetas que despues las tendremos que poner.
* Las demás etiquetas: 
	* Las subetiquetas que hemos puesto anteriormente, hay que poner cada uno de los puestos.
	
**Las demás etiquetas** se pueden clasificar en dos:

* <!ELEMENT> Es la declaración de un elemento, y puede tener las siguientes subcategorias:
	* **USO**: \<!ELEMENT nombre_elemento (modelo_contenido)>
	* (#PCDATA) → **parsed character data**, es texto plano interpretado
	* EMPTY → Es un elemento que dice que no puede tener un hijo de categoria.

	* Sufijos que pueden tener las etiquetas <!ELEMENT>:

> | sufijo | Significado |  
> | --- | --- | 
> | ? | El elemento puede tener una o ninguna subcategoria, pero nunca más de una |
> | * | El elemento puede tener cero o más subcategorias |
> | + | El elemento puede debe tener al menos una subcategoria, pero puede tener más |

* <!ATTLIST> Es la declaración de una lista de atributos. Puede contener lo siguiente:
	* **USO**: \<!ATTLIST nombre_elemento	nombre_atributo    valor_atributo    valor_defecto> Todos estos valores, pueden estar o no estar.
	* \#REQUIRED: Es obligatorio el atributo.

Para comentar: \<!-- COMENTARIO -->

Una [WEB](http://codexexempla.org/articulos/2008/index.php) de donde he sacado la información.

## HTML

**HTML** → Hyper Text Markup Language, fue creado en el 1993 (mientras que el HTTP fue creado en el 1991).

Se dice que **Tim Berners-Lee** fue el creador de HTTP y por consecuencia HTML.

HTML fue muy importante ya que antes del 1991 no havia manera de tener una comunicación estandar, y HTML es importante ya que es un estandar de comunicación y por eso fue revolucionario.

---

**Pequeño inciso**

www.google.es 

* \.es → TLD, Top Level Domain: es el dominio
* www. → World Wide Web: no es un protocolo, es la red ancha del mundo, ahora ya no hace falta poner, ya que el navegador se usa para navegar y no para otras cosas.

[comment]: <> (INTERNET no es igual a DOMINIOS, INTERNET es una multiredes y el DOMINIO es una red)

**RECOMENDACION DEL RAFA**, tener un dominio de *mierda* y luchar por hacer nuestras cosas.

## MARKDOWN
Los _apuntes_ MARKDOWN

### Estilo de carácters

Cursiva: _CORRECTA_ *OTRA FORMA CORRECTA*

Negrita: **CORRECTA** __OTRA FORMA CORRECTA__

~~TACHADO~~

~~***tachado negrita y cursiva***~~

[comment]: <> (Esto es un comentario que no saldrà)
[comment]: <> (Todo se cierra desde dentro hacia fuera)

### Carácters extendidos (emojis)

:poop: :alien: :cry: :imp:

[Emojis para poner en texto](https://gist.github.com/rxaviers/7360908)

**RECUERDA**, estos emj estan para git y en pocos sitios más.

### Listas

* lista n1
	* sub apartado de la lista 1
	* otro sub apartado
* lista n2
* lista n3

### Citas

> Para escribir una cita:
>
>> Esto es una cita dentro de una cita 
>
> Continuamos con la primera cita
>
> -Taratara 2023

### Separador

---
Acabo de poner un separador

### Enlaces

Esto es un enlace a la mejor web del mundo:

[CondorChem](https://condorchem.com)

Y [ESTO](https://enti.cat) es otro enlace.

### Imagen incrustada

![programmer](https://static.vecteezy.com/system/resources/thumbnails/011/961/865/small/programmer-icon-line-color-illustration-vector.jpg)

### Ejemplo de resaltado de sintaxis

```kotlin
fun main(args: Array<String>) {
	// imprimira un Hello World
    println("Hello World")
}
```

### Listas de tareas

- [ ] Primera tarea
- [x] Segunda tarea
- [ ] Tercera tarea 

### Tablas

| id_character | name | age | level |
| ---: | ---: | ---: | ---: |
| 1 | Eustaquio | 197 | 99 |
| 2 | Mariana | 20 | 100 |
| 3 | Mortadelo | 100 | 1 |
| 4 | Messi | 44 | 32 |

[comment]: <> (Donde esten los : los numeros se alinean donde esten puestos)

### Escapar caracters

\# ejemplo de escapado

\*que en otras cosas*