# Problem5
# Problem 5: Income Tax Calculation

# Get user input for last name, number of dependents, and gross income
last_name = input("Enter last name: ")
num_dependents = int(input("Enter number of dependents: "))
gross_income = float(input("Enter gross income: "))

# Calculate adjusted gross income
adjusted_gross_income = gross_income - num_dependents * 12000

# Determine tax rate
if adjusted_gross_income > 50000:
    tax_rate = 0.20
else:
    tax_rate = 0.10

# Calculate income tax
income_tax = adjusted_gross_income * tax_rate

# Ensure income tax is not less than 0
if income_tax < 0:
    income_tax = 100

# Display results
print(f"\nLast Name: {last_name}")
print(f"Gross Income: ${gross_income:.2f}")
print(f"Number of Dependents: {num_dependents}")
print(f"Adjusted Gross Income: ${adjusted_gross_income:.2f}")
print(f"Income Tax: ${income_tax:.2f}")
