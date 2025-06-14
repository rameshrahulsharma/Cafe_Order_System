# Cafe_Order_System
#Cafe Order and total bill automatic calculation

#Define the manu of restaurant
manu={
    'Pizza':40,
    'Pasta':50,
    'Burger':60,
    'Salad':70,
    'Coffee':80
}

#Greet
print("Welcome to Python restaurant")
print("Pizza : Rs40\nPasta : Rs50\nBurger: Rs60\nSalad : Rs70\nCoffee: Rs80")

Order_total=0
#80+70=150

item_1=input("Enter the name of item you want to order = ")
if item_1 in manu:
    Order_total+=manu[item_1]  #0+50
    print(f" Your item{item_1} has been added to your order")
else:
    print(f"Order item {item_1} is not avaialable yet")

Another_order1= input("Do you want to add another item? (Yes/No) ")
if Another_order1 =='Yes':
    item_2 =input("Enter the name of second item :")
    if item_2 in manu:
        Order_total=Order_total+manu[item_2]
        print(f"Item {item_2} has been added to order")
    else:
        print(f"Order item{ item_2} is not available!")
Another_order2=input("Do you want to add another itme? (Yes/No) ")
if Another_order2 =='Yes' :
    item_3=input("Enter the name of third item:")
    if item_3 in manu:
        Order_total += manu[item_3]
        print(f"item {item_3} has been added to order")
    else:
        print(f"Order item {item_3} is not available:")
Another_order3= input("Do you want to add another item? (Yes/No)")
if Another_order3=='Yes':
    item_4=input("Enter the name of 4th order:")
    if item_4 in manu:
        Order_total += manu[item_4]
        print(f"Order item {item_4} has been added to order")
    else:
        print(f"Order item{item_4} is not available:")
Another_order4= input("Do you want to add another item? (Yes/No)")
if Another_order4 =='Yes':
    item_5= input("Enter the name of 5th order: ")
    if item_5 in manu:
        Order_total += manu[item_5]
        print(f"Order  item {item_5} has been added to order:")
    else:
        print(f"Order item{item_5} is not available")
print(f"The total amount of item to pay is {Order_total}")
