# Understanding Microservices

## What Is Monolithic Architecture
Over a decade ago, a software application was typically designed with a **monolithic architecture**. The term "monolithic" comes from "mono," meaning single. A monolithic application is built as a single, unified codebase, where all functionalities are implemented in a single project or repository. The architecture includes the following key components:
1. **Front-End(User Interface)**
- The frontend or user interface was the part of the application that users interacted with.
- For example, when accessing a platform like Flipkart, the interface you see and interact with is the front-end.
2. **Back-End(Business Logic)**
- The backend handles all the application's business logic, processing and communication with the database.
- It was tightly coupled with the front-end, making updates or scaling specific components challenging.
3. **Database**
- The database stored all the data for the application, such as user information, orders and other transactional data.

![Monolithic Architecture](https://github.com/KalyaniGunnam/backend-learnings/blob/main/notes/images/monolithic%20architecture.webp)

# Example: To better understand the need for Microservices
let’s consider the design of a modern e-commerce application like Flipkart. Such an application can be divided into distinct functional modules, each addressing a specific area of functionality.

##### User Management
One of the core modules is **User Management**, which handles all interactions related to user accounts. This includes enabling users to sign up by providing basic details such as email and phone number, facilitating secure logins and offering features for profile management. Users can update their personal details, manage their saved payment methods and view their order history. This module forms the foundation of user interactions with the application.

##### Product Management
Another crucial module is **Product Management**, which governs the handling of products on the platform. Vendors, who are individuals or businesses selling their products on the platform, can use this module to add new products by specifying details such as the product name, description, images, pricing and specifications. They can also update existing products to reflect changes in pricing, stock availability or promotional offers. If a product is discontinued or out of stock, vendors can remove it from the platform. On the other hand, customers use this module to browse through available products, search for specific items, add products to their cart, place orders and even leave reviews after purchasing.

##### Order Management
Once products are added to the cart, the **Order Management** Module takes over. This module handles the process of validating and applying discounts, calculating the total amount—including taxes and discounts—and finalizing the order. It ensures a seamless transition from selection to payment.

##### Payment Module
After order confirmation, the **Payment Module** facilitates secure payment processing. It integrates with multiple payment gateways to allow customers to pay using methods like credit cards, debit cards, net banking and digital wallets. This module also manages payment success and failure cases and maintains a history of all transactions for future reference.

##### Delivery Management
The next step is handled by the **Delivery Management** Module, which oversees the logistics of delivering the products to customers. This module allows delivery personnel to log in, view customer addresses and product details, and can also update the delivery status. Customers are notified of the progress through updates like "Out for delivery" or "Delivered."

##### Returns and Refunds
Finally, the **Returns and Refunds** Module addresses customer dissatisfaction by facilitating product returns, refunds and replacements. Customers can initiate a return request and this module processes refunds or handles replacement requests as needed.

So in this case, a monolithic design means all functionalities of an application—whether related to user management, product handling, orders, payments, delivery, or returns and refunds—were implemented as part of a single codebase. This unified approach meant that everything was contained within a single project and all components were tightly integrated.

# Why To Use Microservices?
Microservices are **distributed systems**, designed to overcome monolithic architecture's limitations. Let’s understand the need for Microservices with an example. 

Consider a typical e-commerce application like Flipkart. On a normal day, assume that around **1 lakh customers** use the platform daily. Now, imagine Flipkart announces its **Big Billion Day Sale**, offering discounts of up to **80%**.

On that day, do you think only **1 lakh customers** will use the app? Certainly not! The traffic is bound to increase significantly. For simplicity, let’s assume 10 lakh customers log into the application on that day.

Now, let’s think about what users typically do on such platforms. The most common activity is exploring products. As a single user, if you browse through **100 products**, you are effectively sending **100 requests** to the server and receiving **100 responses**. This works fine on a normal day with 1 lakh users, resulting in:
- 100 requests per user × 1 lakh users = 10 crore requests.

Now, consider the same scenario on Big Billion Day with 10 lakh users:
- 100 requests per user × 10 lakh users = 100 crore requests.

Clearly, the system needs to handle a massive load during such peak times. If the system cannot manage this load properly, it will crash. 

To address the limitations of monolithic architecture, Microservices architecture divides the application into smaller, independent services. Each service is responsible for a specific functionality (e.g., user management, product management) and can be developed, deployed and scaled independently. Let's see how

**Example: Product Browsing on Flipkart**
Let’s continue with the Flipkart example. Imagine users are exploring products during the Big Billion Day sale. In a monolithic architecture, the products-related functionality is deployed as a single instance on a server. Now, let’s analyze what happens:

##### 1. Monolithic Perspective:
- Assume that 1 instance of the product service can handle up to 10 lakh requests. On Big Billion Day, with 10 lakh users, the number of requests and responses can quickly reach billions. Then the Problem is a single server cannot handle this overwhelming volume of traffic. As a result, the application crashes under the load, leading to downtime.
- Then the Consequences is customers become frustrated, unable to access the application. Negative reviews and complaints flood social media platforms like Facebook, with users creating memes mocking the situation. Over time, users lose trust in the application, thinking that Flipkart deliberately brings the system down during sales. While this might not be Flipkart’s fault, customers don’t see the technical challenges. Instead, they form a negative perception, impacting the company’s reputation.

##### 2. How Microservices Help:
In a Microservices architecture, traffic management becomes more flexible and scalable. Here’s how, 
Instead of deploying the entire application as one instance, the product service is deployed as multiple, independent instances. For example, during peak traffic, you can scale up by deploying 10 instances of the product service across different servers. Hence  Traffic is dynamically distributed across these instances. If more requests are anticipated, additional instances can be deployed quickly to handle the load. Microservices architecture ensures that only the necessary components (like the product service) are scaled, optimizing resource usage. Even if one instance fails, others continue to handle requests, minimizing downtime and ensuring a smoother user experience.

# Key Features of Microservices
- **Independence**: Each microservice operates independently and communicates with others via APIs.
- **Scalability**: Services can be scaled individually based on their specific requirements, optimizing resource usage.
- **Technology Diversity**: Teams can choose the best-suited technology stack for each service without affecting the rest of the application.
- **Faster Development**: Teams can work on different services simultaneously, leading to quicker development and deployment cycles.
