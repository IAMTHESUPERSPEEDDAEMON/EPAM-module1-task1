# EPAM-module1-task1
Object-Oriented Thinking

**a public coffee/vending machine at a university/dormitory/hospital/street**

**1. Describe the requirements for the chosen system: functional and non-functional.**
Functional
1) System must provide a list of available drinks to the user.
2) User can select one drink from the list
3) The system must display the price of the selected drink.
4) The system must accept payment by cash or card.
5) The system must verify that the received payment is greater than or equal to the drink price.
6) After successful payment, the system must prepare and dispense the selected drink.
7) If payment was made in cash and the amount was added more than the drink price, the system must calculaate and issue the change.
8) The system must monitor and track the level of remaining ingredients.
9) An admin user (technician) must have access to refill ingredients and collect cash

Non-Functional
1) The system must be able to work 24\7
2) The system interface must be intuitive with screen hints.
3) payment data must be secure


**2. Design use cases for the system based on the requirements.**
use case 1
Description: A user selects a drink, pays for it and gets it.

Main Scenario:
1) User approaches the coffee machine
2) The system displays a list of drinks on the display.
3) User selects a drink by inputting a number.
4) The system displays the price of the drink.
5) User confirms the order.
6) System displays ways to pay
7) user selects payment method
8) User inserts payment (cash or card).
9) the system prepares and dispenses the selected drink
10) the system returns change


Use case 2
Description: An admin replenishes ingredients and collects cash from the coffee machine.

Main Scenario:
1) Admin opens the service panel.
2) The system enters serviceMode
3) Admin refills the containers
4) Admin collects cash from the coffee machine bank.
5) Admin closes the service panel.
6) The system exits service mode.


**3.Identify objects, classes, and relationships in the system.**
CoffeeMachine - main class
Composition:
CoffeeMachine owns-a: Display, ControlPanel, Dispenser, PaymentAcceptor, Bank
ControlPanel owns-a: Button

Aggregation:
CoffeeMachine has-a: Drink

Inheritance:
BillAcceptor is-a PaymentAcceptor
CardReader is-a PaymentAcceptor

Asociation:
Dispencer use: Recipe, IngredientContainer
Drink use: Recipe
BillAcceptor use: Bank


**5.Design class diagrams picturing classes, their attributes, and relations in the system.**
<img width="1217" height="857" alt="зображення" src="https://github.com/user-attachments/assets/cdd3be63-ed6f-4fb1-8b23-3b0bae13883c" />

