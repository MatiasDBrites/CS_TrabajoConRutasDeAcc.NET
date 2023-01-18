# CS_TrabajoConRutasDeAcc.NET
Trabajo con rutas de acceso de archivo en .NET

En el editor, inserte el código siguiente encima de la primera línea del archivo `Program.cs`
. Este código usa el método `Directory.GetCurrentDirectory`
 para obtener la ruta del directorio actual y almacenarla en una nueva variable `currentDirectory`
:

```csharp
var currentDirectory = Directory.GetCurrentDirectory();
```

Inserte el código siguiente después del que acaba de agregar. Este código usa el método `Path.Combine`
 para crear la ruta de acceso completa al directorio de *almacenes*
 y almacenarla en una nueva variable `storesDirectory`
:

```csharp
var storesDirectory = Path.Combine(currentDirectory, "stores");
```

Reemplace la variable `stores`
 de la función `FindFiles`
 con la nueva variable `storesDirectory`
:

```csharp
var salesFiles = FindFiles(storesDirectory);
```

Ahora la parte superior del archivo debe tener un aspecto similar al siguiente fragmento de código:

```csharp
var currentDirectory = Directory.GetCurrentDirectory();
var storesDirectory = Path.Combine(currentDirectory, "stores");
var salesFiles = FindFiles(storesDirectory);

foreach (var file in salesFiles)
{
    Console.WriteLine(file);
}
```

Guardar, Ejecute el programa desde la línea de comandos:

```csharp
dotnet run
```

El programa debe mostrar la salida siguiente:

Resultado

```
/home/username/dotnet-files/stores/sales.json
/home/username/dotnet-files/stores/201/sales.json
/home/username/dotnet-files/stores/202/sales.json
/home/username/dotnet-files/stores/203/sales.json
/home/username/dotnet-files/stores/204/sales.json
```
[![rutasdearchivo-net.png](https://i.postimg.cc/SsZ5xRNj/rutasdearchivo-net.png)](https://postimg.cc/qh3QmkKd)
