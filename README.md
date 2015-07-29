<b>Problem:</b>
As a customer shops an insurance policy, he/she will receive a number of quotes with different coverage options before purchasing a plan. This is represented in this challenge as a series of rows that include a customer ID, information about the customer, information about the quoted policy, and the cost. Your task is to predict the purchased coverage options using a limited subset of the total interaction history. If the eventual purchase can be predicted sooner in the shopping window, the quoting process is shortened and the issuer is less likely to lose the customer's business. Using a customer’s shopping history, can you predict what policy they will end up choosing?

<br>The training and test sets contain transaction history for customers that ended up purchasing a policy. For each customer_ID, you are given their quote history. In the training set you have the entire quote history, the last row of which contains the coverage options they purchased. In the test set, you have only a partial history of the quotes and do not have the purchased coverage options. These are truncated to certain lengths to simulate making predictions with less history (higher uncertainty) or more history (lower uncertainty). For each customer_ID in the test set, you must predict the seven coverage options they end up purchasing.

<b>What is a customer?</b> Each customer has many shopping points, where a shopping point is defined by a customer with certain characteristics viewing a product and its associated cost at a particular time.
<br>•	Some customer characteristics may change over time (e.g. as the customer changes or provides new information), and the cost depends on both the product and the customer characteristics.
<br>•	A customer may represent a collection of people, as policies can cover more than one person.
<br>•	A customer may purchase a product that was not viewed!

<b>Product Options:</b>
Each product has 7 customizable options selected by customers, each with 2, 3, or 4 ordinal values possible: A product is simply a vector with length 7 whose values are chosen from each of the options listed above. The cost of a product is a function of both the product options and customer characteristics.
<br><b>Variable Descriptions:</b>
    <br>customer_ID - A unique identifier for the customer
    <br>shopping_pt - Unique identifier for the shopping point of a given customer
    <br>record_type - 0=shopping point, 1=purchase point
    <br>day - Day of the week (0-6, 0=Monday)
    <br>time - Time of day (HH:MM)
    <br>state - State where shopping point occurred
    <br>location - Location ID where shopping point occurred
    <br>group_size - How many people will be covered under the policy (1, 2, 3 or 4)
    <br>homeowner - Whether the customer owns a home or not (0=no, 1=yes)
    <br>car_age - Age of the customer’s car
    <br>car_value - How valuable was the customer’s car when new
    <br>risk_factor - An ordinal assessment of how risky the customer is (1, 2, 3, 4)
    <br>age_oldest - Age of the oldest person in customer's group
    <br>age_youngest - Age of the youngest person in customer’s group
    <br>married_couple - Does the customer group contain a married couple (0=no, 1=yes)
    <br>C_previous - What the customer formerly had or currently has for product option C (0=nothing, 1, 2, 3,4)
    <br>duration_previous -  how long (in years) the customer was covered by their previous issuer
    <br>A,B,C,D,E,F,G - the coverage options
    <br>cost - cost of the quoted coverage options
    
