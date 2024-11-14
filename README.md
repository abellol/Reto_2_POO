# Reto 2

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
