User ||--o{ Orders : places
User ||--o{ Address : has
Restaurant ||--o{ MenuItem : offers
Orders ||--o{ OrderItem : contains
Orders ||--|| Payment : generates
DeliveryPartner ||--o{ Orders : delivers
Restaurant ||--o{ Review : receives
User ||--o{ Review : writes
