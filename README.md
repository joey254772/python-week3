# python-week3
def calculate_discount(price, discount_percent):
    """
    Calculates the final price after applying a discount if it's 20% or higher.
    
    :param price: Original price of the item
    :param discount_percent: Discount percentage
    :return: Final price after applying discount (or original price if discount < 20%)
    """
    if discount_percent >= 20:
        discount_amount = price * (discount_percent / 100)
        final_price = price - discount_amount
        return final_price
    else:
        return price

# Prompting the user for input
price = float(input("Enter the original price of the item: "))
discount_percent = float(input("Enter the discount percentage: "))

# Calculating the final price
final_price = calculate_discount(price, discount_percent)

# Printing the final result
if discount_percent >= 20:
    print(f"The final price after applying a {discount_percent}% discount is: {final_price:.2f}")
else:
    print(f"No discount applied. The original price remains: {price:.2f}")
