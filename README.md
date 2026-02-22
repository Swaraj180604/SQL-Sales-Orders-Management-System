## Data Schema
The database consists of three primary tables linked through relational keys to ensure data integrity:

# 1. AGENTS Table
Stores information about the sales force.

**AGENT_CODE**: Unique identifier for each agent (Primary Key).

**AGENT_NAME**: Full name of the agent.

**WORKING_AREA**: The geographic region assigned to the agent.

**COMMISSION**: The percentage rate earned on sales.

**PHONE_NO**: Contact information.

# 2. CUSTOMER Table
Contains detailed profiles and financial status of clients.

**CUST_CODE**: Unique identifier for each customer (Primary Key).

**CUST_NAME**: Name of the customer.

**Financial Tracking**: Includes OPENING_AMT, RECEIVE_AMT, PAYMENT_AMT, and OUTSTANDING_AMT.

**AGENT_CODE**: Links each customer to a specific agent (Foreign Key).

# 3. ORDERS Table
Records individual transaction details.

**ORD_NUM**: Unique order identification number (Primary Key).

**ORD_AMOUNT/ADVANCE_AMOUNT**: Financial breakdown of the specific sale.

**ORD_DATE**: The date the transaction occurred.

**CUST_CODE / AGENT_CODE**: Foreign keys linking the transaction to both a customer and an agent.

# Key Features
**Relational Integrity**: Uses PRIMARY KEY and REFERENCES constraints to maintain strict relationships between agents, customers, and their orders.

**Comprehensive Financial Reporting**: Includes logic to calculate total commissions, average opening amounts, and total outstanding debt across different regions.

**Geographical Analysis**: Queries allow for grouping data by city (e.g., London, Bangalore, Mumbai) to identify high-performing or high-risk areas.

Performance Benchmarking: Features queries to identify top-performing agents based on order volume and top customers based on payment history.

Multi-Level Querying: Provides a range of SQL techniques from basic filtering (WHERE) and sorting (ORDER BY) to complex multi-table JOIN operations and subqueries.
