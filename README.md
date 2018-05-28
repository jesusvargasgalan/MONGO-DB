# MONGO-DB


<h1>1. Crear una base de datos</h1>

```console
> use videojuegos
switched to db videojuegos
```
<h1>2.Tener una colección</h1>

```console
> MongoDB Enterprise > db.createCollection('biblioteca')
>{ "ok" : 1 }
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
MongoDB Enterprise > db.biblioteca.insert({nombre: "Zelda", plataforma: "Wii",pegi:3)
WriteResult({ "nInserted" : 1 })
MongoDB Enterprise > db.biblioteca.insert({nombre: "Call of Duty", plataforma: "Playstation",pegi:16)
WriteResult({ "nInserted" : 1 })
MongoDB Enterprise > db.biblioteca.insert({nombre: "Tetris", plataforma: "GameBoy",pegi:3)
WriteResult({ "nInserted" : 1 })
```
<h2>3.2 Modificar</h2>


<h2>3.3 Eliminar</h2>
```console
MongoDB Enterprise > db.biblioteca.remove({nombre: "Spyro"})
WriteResult({ "nRemoved" : 1 })
```
<h1>4 Crear un índica sobre un campo de la colección</h1>
```console
MongoDB Enterprise > db.biblioteca.createIndex({videojuego: 1})
{
        "createdCollectionAutomatically" : false,
        "numIndexesBefore" : 1,
        "numIndexesAfter" : 2,
        "ok" : 1
}
```
<h1>5. Realizar consultas en las que utilices mayor que, igual que, menor que.</h1>
<h2>5.1 </h2>
