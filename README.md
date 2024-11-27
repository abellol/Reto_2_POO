# Reto 2
Hola, soy }**Alejandro Bello** y pertenezco al grupo fenomenoides, a continuación nuestro logo:

<details><summary>Preparense para ver el grandioso logo: </summary><p>
<div align='center'>
<figure> <img src="https://i.postimg.cc/NFbwf57S/logo-def.png" alt="Logo fenomenoides" width="400" height="auto"/></br>
<figcaption><b> "somos programadores, no diseñadores" </b></figcaption></figure>
</div>
</p></details><br>

Para este reto, decidí plantar las relaciones que pueden haber a nivel general en una tienda online de flores, allí esta toda la interacción del cliente con la tienda y también, hay empleados que deben mantener en orden el inventario de la tienda. A continuación se muestra el diagrama de clases con sus relaciones:

```mermaid
classDiagram

    Customer : + str name
    Customer : + str direction
    Customer : + str phone_number
    Customer : + buy()

    Flower : + list color
    Flower : + int price
    Flower : + update_price()

    Shop : +  list flowers
    Shop : +  list employees
    Shop : +  str website
    Shop : +  consult_ inventory()
    Shop : +  add_flower()
    Shop : +  remove_flower()

    Employee : + str name
    Employee : + str identification
    Employee : + str job
    Employee : + update_inventory()

    ShopCar : + float total
    ShopCar : + list flowers
    ShopCar : + str date
    ShopCar : + calculate_total()
    ShopCar : + add_flower()
    ShopCar : + remove_flower()

    Shop *-- Flower
    Shop *-- Employee
    Shop *-- ShopCar
    Customer --> ShopCar : buy(ShopCar)
```
