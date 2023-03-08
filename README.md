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

En esta asignatura aprenderemos HTML5, que es html Life Scheme.

``` HTML
<html>
<head>
	<title>Martí Tarrasón</title>
	
	
<style>
html{
padding:0;
margin:0;
}
body{
padding:0;
margin:0;
background-color:#ffffff;
font-family:Arial;
}
h1{
background-color:#4EA8DE;
color:#000000;
font-size:20px;
border-left:4px solid #6930C3;
/*margin-top:0;
margin-right:32px;
margin-bottom:64px;
margin-left:32px;
margin:0 32px 64px 32px;*/
}

form{
margin: 8px 32px 8 px 32px;
border: 1px solid red;
background-color:#ccc;
font-family:Courier;
color:#0f0;
/*border:1px dotted #ffffff*/
}
/*solid/dotted/dasehd/etc*/

img{
width:100px;
}

#comoarruinartuvida{
width:150px;
border:3px solid black;
}

fieldset{
border:2px solid #444;
background-color: #ddd;
font-family:Verdana;
}

legend{
background-color:#444;
color:#fff;
padding:0 2px 0 2px;
}

input, textarea, select{
color:#0f0;
font-size:24px;
}

</style>
	
</head>
<!--ESTO ES UN COMENTARIO SECRETO-->
<body>
<h1>Página "oficial" de Martí Tarrasón</h1>
<h2>Aquí voy a hablar un poco de mí, de donde vengo y que cosas me gustan:</h2>
<p>Yo vengo de hacer un bachillerato <strong>tecnológico</strong></p>
<p>Ahora mismo estudio un ciclo de ENTI, especialmente en <strong><a href="https://enti.cat/es/">DAM VIOD</a></strong>. Me apunté; en este ciclo porque desde pequeño siempre he tenido la idea de que cuando sea mayor,
sería un programador profesional de videojuegos. Y desde pequeño intenté; cosas de programación,
por ejemplo en primero de la ESO hice tres "virus" para que los ordenadores del instituto se apagasen, ese "virus" funciono, pero al momento de poner y que funcionara,
lo saque para no meterme en problemas. Esto lo hice con <em>C++</em>, pero si me preguntas algo de este lenguaje, no te sabré responder, ya que hace mucho tiempo que no lo toco.</p>
<p>Después intenté hacer un mod de Minecraft con JavaScript, pero al hacerlo con un amigo que tenía mucha idea y que yo no, al final no compaginamos bien y nos separamos a la semana.</p>
<p>Cambiando de tema, las aficiones que tengo son: <strong>esgrima</strong>, pádel, ver anime, ver Twitch y por último jugar a juegos sin sonido, ya que soy <em>sordo</em>,
 estoy acostumbrado a jugar sin sonido y si juego con, me es muy difícil estar por el juego, y por eso un proyecto que quiero hacer, <strong>es un videojuego sin sonido.</strong></p>
<p>Y por último, los juegos que me gustan son varios:</p>
 <ol>
 <li><a href="https://www.minecraft.net/es-es">Minecraft</a></li>
 <li><a href="https://store.steampowered.com/app/413150/Stardew_Valley/">Stardew Valley</a></li>
 <li><a href="https://play.google.com/store/apps/details?id=com.supercell.clashofclans&hl=es&gl=US">Clash of Clans</a></li>
 <li><a href="https://www.smashbros.com/es_ES/">Super Smash Bros Ultimate</a></li>
 <li><a href="https://es.wikipedia.org/wiki/Super_Mario_64">Mario 64</a></li> 
 </ol>
<p>Pero últimamente solo juego los juegos gratis de Epic Games.</p>
<p>Y esto es todo de mi parte</p> 

<p><a href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"><img src="happy.jpg"/></a></p>
<p><a href="https://www.leagueoflegends.com/es-es/"><img src="Troll.jpg" id="comoarruinartuvida" /></a></p>

<hr/> <!-- ja no es fa servir -->

<h2>Tabla v.1</h2>

<table>
<tr>
<th>Tabla A</th>
<td>1</td>
<td>2</td>
<td>3</td>
</tr>
	
<tr>
<th>Tabla B</th>
<td>4</td>
<td>5</td>
<td>6</td>
</tr>
</table>

<h2>Tablas v.2</h2>

<table>
<tr>
<th>Tabla A</th><th>Tabla B</th>
</tr>
<tr>
<td>1</td><td>4</td>
</tr>
<tr>
<td>2</td><td>5</td>
</tr>
<tr>
<td>3</td><td>6</td>
</tr>
</table>

<h2>Formulario demostrativo</h2>

<form>

<p>Usuario: <input type="text" /></p>
<p>Password: <input type="password" /></p>
<p>Radio: <input type="radio"/></p>
<p>Checkbox: <input type="checkbox"/></p>
<p>Button: <input type="button"/></p>
<p>Número: <input type="number"/></p>
<p>Fecha: <input type="date"/></p>
<p>Color: <input type="color"/></p>

<p>Texto largo: <textarea></textarea></p>

<p>Selector: 
<select>
<option>Uno</option>
<option>Dos</option>
<option>Tres</option>
<option>Quatro</option>
</select></p>

<p>Enviar: <input type="submit"/></p>

</form>

<h2>Formulario</h2>

<form>
<p>Usuario: <input type="text" name="user" value="Taratara"/></p>
<p>Password: <input type="password" name="pass"/></p>
<select name="selector">
<option value="1">Uno</option>
<option value="2">Dos dos dos</option> <!-- els espais no sons bons, posar el value -->
<option value="3">Tres</option>
<option value="4">Quatro</option>
</select>
<p><input type="button" value="esto es un boton"/></p>
<p><input type="submit" value="Enviar"/></p>
</form>

<marquee>- - - - - - - - -</marquee>
<marquee> C R I N G E </marquee>
<marquee>- - - - - - - - -</marquee>

<hr/> <!-- ja no es fa servir -->

</form>

<form>
<fieldset>
<legend>Formulario de login</legend>
<p><label for="login-user">Usuario: </label><input type="text" name="user" id="login-user"/></p>
<p><label for ="login-pass">Contraseña: </label><input type="password" name="pass" id="login-pass"/></p>
</fieldset>

</form>

</body>
</html>
```

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