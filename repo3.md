sequenceDiagram
    actor Usuario

    Usuario ->> Main: Inicia programa
    Main ->> Scanner: new Scanner(System.in)
    Main ->> CalculadoraIVA: new CalculadoraIVA()

    Main ->> Usuario: Solicita nombre del producto
    Usuario ->> Main: Ingresa nombre
    Main ->> Scanner: nextLine()
    Scanner -->> Main: nombre

    Main ->> Usuario: Solicita precio base
    Usuario ->> Main: Ingresa precio
    Main ->> Scanner: nextDouble()
    Scanner -->> Main: precio

    Main ->> Producto: new Producto(nombre, precio)

    Main ->> Producto: getPrecioBase()
    Producto -->> Main: precioBase

    Main ->> CalculadoraIVA: calcularPrecioFinal(precioBase)
    CalculadoraIVA -->> Main: precioFinal

    Main ->> Usuario: Muestra total con IVA
