

## Conexión a la Shell de MongoDB

Para acceder a la consola interactiva (`mongosh`) dentro del contenedor en ejecución, utiliza el siguiente comando:

```bash
docker exec -it mongodb_docencia mongosh --username admin --password admin123 --authenticationDatabase admin 
```

Para encender tambien el docker (este no lo probe)

```bash
docker start mongodb_docencia mongo_express_docencia
```

## Comandos que probablemente use
para moverse a la base de datos, si no existe crearla
```bash
show dbs
use tienda
```
para crear un documento
```bash
db.productos.insertOne({
  nombre: "Laptop Pro",
  precio: 1400,
  categoria: "computacion",
  stock: 30
})
```
para eliminar un documento
```bash
db.tienda.deleteOne({ nombre: "Laptop" })
db.tienda.deleteOne({ _id: ObjectId("65f4a1b2c3d4e5f6a7b8c9d0") })
```
para buscar un id
```bash
db.productos.find({ nombre: "Laptop Pro" })
```
