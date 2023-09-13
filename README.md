# Santander Work 2023
java restful api criada para santander dev week

##Diagrama de classes
```mermaid
classDiagram
  class User {
    - name: String
    - account: Account
    - features: Feature[]
    - card: Card
    - news: News[]
  }

  class Account {
    - number: String
    - agency: String
    - balance: Double
    - limit: Double
  }

  class Feature {
    - icon: String
    - description: String
  }

  class Card {
    - number: String
    - limit: Double
  }

  class News {
    - icon: String
    - description: String
  }

  User"1" <-- "1"Account : has
  User"1" <-- "1..N" Feature : has many
  User"1" <-- "1"Card : has one
  User"1" --> "1"News : has many
```
