# SHOP INVENTORY

print("="*50)
print("                 SHOP INVENTORY")
print("="*50)
products= [
    {"name": "keyboard", "price": 1200, "stock":5},
    {"name": "laptop", "price": 120000, "stock":15},
    {"name": "mouse", "price": 2000, "stock":20},
    {"name": "headphones", "price": 2500, "stock":5},
    {"name": "speaker", "price": 5000, "stock":10}
]

# LOADING DATA:

for product in products:
    print(f"\nproduct: {product['name']}")
    print(f"price: {product['price']}")
    print(f"qty: {product['stock']}")
    if product['stock']== 0:
        print("no stock")
    elif product['stock'] <= 5:
        print("low stock")
    else:
        print("stock available")

# BILL DETAILS:


print()
print("="*50)
print("                   BILL DETAILS:")
print("="*50)
name = input("please enter product name")
quantity= int(input("please enter quantity"))
found= False
for product in products:
    if name.lower()== product['name'].lower():
        found = True
        if quantity <= product["stock"]:
            product["stock"] -= quantity
            bill = quantity * product["price"]
            print(f"remainig stock: {product['stock']}")
            print(bill)
        else:
            print("something wrong")
if not found:
    print("item not exisst")

# UPDATE INVENTORY:

print("="*50)
print("                  UPDATE INVENTORY")
print("="*50)
for product in products:
    print(f"\nproduct: {product['name']}")
    print(f"price: {product['price']}")
    print(f"qty: {product['stock']}")
    
    if product['stock']== 0:
        print("no stock")
    elif product['stock'] <= 5:
        print("low stock")
    else:
        print("stock available")
print("="*50)
print("                  THANK YOU")
print("="*50)


    
    
                
            

