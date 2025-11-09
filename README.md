# 🚗 Car Booking System ER Diagram

```mermaid
erDiagram
    User ||--o{ Booking : "places"
    Car ||--o{ Booking : "is assigned to"
    Car ||--|{ Driver : "has"
    Booking ||--|| Payment : "generates"

    User {
        string User_ID PK
        string Name
        string Email
        string Phone
        string Address
        string Password
    }

    Booking {
        string Booking_ID PK
        date Booking_Date
        string Pickup_Location
        string Dropoff_Location
        time Start_Time
        time End_Time
        float Total_Amount
        string User_ID FK
        string Car_ID FK
    }

    Payment {
        string Payment_ID PK
        date Payment_Date
        float Amount
        string Payment_Method
        string Payment_Status
        string Booking_ID FK
    }

    Car {
        string Car_ID PK
        string Model
        string Brand
        string Registration_Number
        string Type
        float Price_per_km
        string Availability_Status
    }

    Driver {
        string Driver_ID PK
        string Name
        string License_Number
        string Phone
        string Address
        string Experience
    }
