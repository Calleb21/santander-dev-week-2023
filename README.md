# Santander-Dev-Week-2023
Repositório para armazenar o projeto do curso Backend Java Dio 2023

## Diagrama de Classes

```mermaid
classDiagram
class User {
  - name: String
  - account: Account
  - features: List<Feature>
  - card: Card
  - news: List<News>
}

class Account {
  - accountNumber: String
  - accountAgency: String
  - accountBalance: Double
  - accountLimit: Double
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

User "1" *-- "1" Account
User "1" *-- "N" Feature
User "1" *-- "1" Card
User "1" *-- "N" News

