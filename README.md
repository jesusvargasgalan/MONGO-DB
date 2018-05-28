# MONGO-DB


<h1>1. Crear una base de datos</h1>

```console
> use videojuegos
switched to db videojuegos
```
<h1>2.Tener una colección</h1>

```console
> MongoDB Enterprise > db.createCollection('biblioteca')
{ "ok" : 1 }
```
<h1>3.Insertar,modificar y borrar documentos en la colección</h1>
<h2>3.1 Insertar</h2>

```console
> MongoDB Enterprise > db.biblioteca.insert({nombre: "God of War", plataforma: "Playstation 4"})
WriteResult({ "nInserted" : 1 })
> MongoDB Enterprise > db.biblioteca.insert({nombre: "Halo", plataforma: "Xbox"})
WriteResult({ "nInserted" : 1 })
> MongoDB Enterprise > db.biblioteca.insert({nombre: "Mario", plataforma: "Wii",desarrolladora: "Nintendo")
WriteResult({ "nInserted" : 1 })
> MongoDB Enterprise > db.biblioteca.insert({nombre: "Zelda", plataforma: "Wii",pegi:3)
WriteResult({ "nInserted" : 1 })
> MongoDB Enterprise > db.biblioteca.insert({nombre: "Call of Duty", plataforma: "Playstation",pegi:16)
WriteResult({ "nInserted" : 1 })
> MongoDB Enterprise > db.biblioteca.insert({nombre: "Tetris", plataforma: "GameBoy",pegi:3)
WriteResult({ "nInserted" : 1 })
```
<h2>3.2 Modificar</h2>
<img src=./imagenes/modificar.PNG width=600px>

<h2>3.3 Eliminar</h2>

```console
> MongoDB Enterprise > db.biblioteca.remove({nombre: "Spyro"})
WriteResult({ "nRemoved" : 1 })
```
<h1>4 Crear un índicE sobre un campo de la colección</h1>

```console
> MongoDB Enterprise > db.biblioteca.createIndex({videojuego: 1})
{
        "createdCollectionAutomatically" : false,
        "numIndexesBefore" : 1,
        "numIndexesAfter" : 2,
        "ok" : 1
}
```
<h1>5. Realizar consultas en las que utilices mayor que, igual que, menor que.</h1>
<h2>5.1 Muéstrame aquellos juegos cuyo PEGI sea mayor a 3</h2>
<img src=./imagenes/mayor.PNG width=600px>
<br/>
<h2>5.2 Muéstrame aquellos juegos cuyo PEGI sea menor que 10</h2>
<img src=./imagenes/menor.PNG width=600px>
<br/>
<h2>5.3 Muéstrame aquellos juegos cuyo PEGI sea igual que 16</h2>
<img src=./imagenes/igual.PNG width=600px>
<br/>
<h1>6. Realizar una consulta en la que los documentos se muestren ordenados y se limite el número de mostrados.</h1>
<img src=./imagenes/6.PNG width=600px>
<br/>
<h1>7.Realizar una consulta con agrupamiento y una función para mostrar la media, o suma, o la que tú decidas.</h1>
Al no haber juegos que se encuentren en la misma plataforma que tengan pegi no hace la media pero la consulta está bien
<img src=./imagenes/media.PNG width=600px>
<br/>
