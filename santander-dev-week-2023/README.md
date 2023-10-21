# Santander Dev Week 2023
JAVA RESTfull API criada para a Santander Dev Week


## Diagrama de Classes

```mermaid
classDiagram
  class User {
    - name: String
    - account: Account
    - features: Features
    - card: Card
    - news: News
  }
  class Account {
    - Number: String
    - Agency: String
    - Balance: String
    - Limit: String
  }
  class Features {
    - pix: Feature
    - pagar: Feature
    - transfer: Feature
  }
  class Feature {
    - Icon: String
    - Description: String
  }
  class Card {
    - Number: String
    - Limit: String
  }
  class News {
    - Icon: String
    - Description: String
  }

  User "1" *-- "1" Account
  User "1" *-- "N" Features
  User "1" *-- "1" Card
  User "1" *-- "N" News
  Features -- Feature
  ```
