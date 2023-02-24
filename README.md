<Directory /usr/share/phpMyAdmin/>
  AddDefaultCharset UTF-8

  <IfModule mod_authz_core.c>
    # Apache 2.4
    <RequireAny>
#       Require ip 127.0.0.1
#       Require ip ::1
       Require all granted
    </RequireAny>
  </IfModule>
  <IfModule !mod_authz_core.c>
    # Apache 2.2
    Order Deny,Allow
    Deny from All
    Allow from 127.0.0.1
    Allow from ::1
  </IfModule>
</Directory>





lovely_loveseat_description = ("Lovely Loveseat" ' ')
lovely_loveseat_description += ("Tufted polyester blend on wood" ' ')
lovely_loveseat_description += ("32 inches high x 40 inches wide x 3 inches deep" ' ')
lovely_loveseat_description += ("Red or white")
print(lovely_loveseat_description)

# creating price for loveseat
lovely_loveseat_price = 254.00
print(lovely_loveseat_price)

# extending our inventory
stylish_settee_description = ("Stylish settee" ' ')
stylish_settee_description += ("Faux leather on birch" ' ')
stylish_settee_description += ("29.50 inches high x 54.75 inches wide x 28 inches deep" ' ')
stylish_settee_description += ("Black")
print(stylish_settee_description)

# Setting price for Stylish Settee
stylish_settee_price = 180.50
print(stylish_settee_price)

# creating Luxurious Lamp
luxurious_lamp_description = ("Luxurious Lamp" ' ')
luxurious_lamp_description += ("Glass and iron" ' ')
luxurious_lamp_description += ("36 inches tall" ' ')
luxurious_lamp_description += ("Brown with cream shade")
print(luxurious_lamp_description)

# Setting price for Luxurious Lamp
luxurious_lamp_description = 52.15
print(luxurious_lamp_description)

# Calculating sales tax
sales_tax = .088
print(sales_tax)

# First Customer Purchase
customer_one_total = 0
print(customer_one_total)

# Customer Purchase List
customer_one_itemization = ("")
print(customer_one_itemization)

#  Customer bought Lovely Loveseat
customer_one_total += lovely_loveseat_price
print(customer_one_total)

# Keeping track of Customer Purchase
customer_one_itemization += ("lovely_loveseat_price")
print(customer_one_itemization)

# Customer Purchase Luxurious Lamp
customer_one_total += luxurious_lamp_description
print(customer_one_total)

# Adding itemization to Luxurious Lamp
customer_one_total += luxurious_lamp_description
print(luxurious_lamp_description)

# Calculating Sales Tax
customer_one_tax = customer_one_total * sales_tax
print(customer_one_tax)

# Add Sales tax to Customer's total cost
customer_one_total += customer_one_tax
print(customer_one_total)

# Start Printing out receipt
print("Customer One Items")

# Print Customer itemization
print("customer_one_itemization")

# Heading for total cost
print("Customer One Total")


