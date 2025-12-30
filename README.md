manu = {"Coffee" :50,
        "Tea" :20,
        "Water" :20,
        "Sandwich" :40,
        "Burger" :120,
        "Cake" :60,
        "Cupcake" :70,
        "Noodles" :20}

GST_Rate=0.05
Orders={}
Subtotal=0

print("Welcome to the Cafe of Royal Baker \u2615")
print("\nManu:")
for item, price in manu.items():
    print(f"{item:<10}: Rs {price}")
# Taking Order
while True:
    item = input("\nEnter item name (or type 'Done' to finish): ").title()
    if item == "Done":
        break
    elif item in manu:
        qty=int(input(f"Enter quantity of {item}: "))
        Orders[item]=Orders.get(item,0)+qty
        cost=manu[item]*qty
        Subtotal+=cost
        print(f"✅ added {item} x {qty} (Rs {cost})")
    else:
        print("❌ item not available")

#Bill Summary
gst_amount=Subtotal*GST_Rate
final_total=Subtotal+gst_amount

print("\n"+ "=" *30)
print("Bill Summary")
print("="*30)

for item, qty in Orders.items():
    price=manu[item]
    print(f"{item:<10} X {qty:<2} = Rs {price* qty}")

print("-" *30)
print(f"Total cost: {Subtotal}")
print(f"Total gst: {gst_amount:.2f}")
print("-" *30)
print(f"Final total: {final_total:.2f}")
print("-" *30)
print("🙏 Thank you! Visit again ☕")
