# Código y documentación M04-UF1
Cyberseguridad: Llenguatge de Marques, con el profesor Rafa Laguna

**Recordatorio** de subir las cosas al GitHub: git add -A .			git commit -m ""			git push

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

**XML** o **Lenguaje de Marcas Extensible** permite definir y almacenar datos de forma compartible. XML admite el intercambio de información entre sistemas de computación, como sitios web, bases de datos y aplicaciones de terceros. Las reglas predefinidas facilitan la transmisión de datos como archivos XML a través de cualquier red, ya que el destinatario puede usar esas reglas para leer los datos de forma precisa y eficiente.

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
Aquí irán los apuntes de DTD

```DTD
<!ELEMENT character (name, surname?, age> <!-- el ? es que puede estar o no -->
<!ELEMENT name(#PCDATA)>
<!ELEMENT surname(#PCDATA)>
<!ELEMENT age EMPTY> <!-- algo o nada -->


<!ATTLIST character id_charater CDATA #REQUIRED>
<!ATTLIST age years CDATA #REQUIRED>
```

Este DTD, es una continuación del XML anterior.

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