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
    Gateway((API Gateway)) --> Catalog((Catalog))
    Backoffice((Backoffice)) --> Catalog((Catalog))
    Gateway((API Gateway)) --> Orders((Orders))
    Gateway((API Gateway)) --> paymentTopic[Payment Topic]
    paymentTopic --> Payments((Payments))
    paymentTopic --> Fraud((Fraud Detection))
    
    Payments((Payments)) --> notificationTopic[Notification Topic]
    Fraud --> notificationTopic[Notification Topic]
    notificationTopic --> Notifications((Notifications))
    Shipping((Shipping)) --> notificationTopic
    
    Cart((Cart))

```