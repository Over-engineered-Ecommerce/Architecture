# Architecture
Overengineered Ecommerce Architecture



```mermaid
graph LR;
    Frontend((Frontend)) --> Gateway((API Gateway))
    Mobile((Mobile)) --> Gateway((API Gateway))
    

    
```
```mermaid
graph LR;

    Catalog((Catalog))
    
    
    Gateway((API Gateway)) --> Auth((Authentication))
    Auth((Authentication)) --> Users((Users))
    Gateway((API Gateway)) --> Inventory((Inventory))
    Gateway((API Gateway)) --> Orders((Orders))
    Gateway((API Gateway)) --> Payments((Payments))
    Fraud((Fraud Detection))
    Notifications((Notifications))
    Shipping((Shipping))
    Cart((Cart))

```