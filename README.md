#Santander Dev Week 2023

## Diagrama de classes

``` mermaid
classDiagram
    class User {
        - string name
        - Account account
        - List<Feature> features
        - Card card
        - List<News> news
        + void displayUserInfo()
    }

    class Account {
        - string Number
        - string Agency
        - float Balance
        - float Limit
        + void displayAccountInfo()
    }

    class Feature {
        - string icon
        - string description
        + void displayFeatureInfo()
    }

    class Card {
        - string Number
        - float Limit
        + void displayCardInfo()
    }

    class News {
        - string icon
        - string description
        + void displayNewsInfo()
    }

    User "1"   *-- "1" Account 
    User "1 " *-- "N" Feature
    User "1 " *-- "1" Card 
    User "1 " *-- "N" News
```
