
* Ruby version
- ruby 2.3.1

* Database creation

  1. Messagesテーブル

    | Field | Type    | Null  | Unique | Foreign_key | Index|
    | :----:| :----:  | :----:| :----: | :-------:| :----:|
    | id    | integer | NO    |        |          |       |
    | body  | text    | NO    |        |          |       |
    | image | string  |       |        |          |       |
    | user_id | integer  | NO |        | YES      |       |
    | group_id | integer | NO |        | YES      |       |

  2. Usersテーブル

    | Field | Type    | Null  | Unique| Foreign_key | Index |
    | :----:| :----:  | :----:| :----:| :----------:| :----:|
    | id    | integer | NO    |       |             |       |
    | name  | string  | NO    |       |             |   YES |
    | email | string  | NO    | YES   |             |       |
    | password | string | NO  |       |             |       |

  3. Groupsテーブル

    | Field | Type    | Null  | Unique| Foreign_key | Index |
    | :----:| :----:  | :----:| :----:| :----------:| :----:|
    | id    | integer | NO    |       |             |       |
    | name  | string  | NO    |       |             |   YES |

 4. Users_Groupsテーブル

    | Field    | Type    | Null  | Unique| Foreign_key | Index |
    | :----:   | :----:  | :----:| :----:| :----------:| :----:|
    | id       | integer | NO    |       |             |       |
    | user_id  | integer | NO    |       | YES         |       |
    | group_id | integer | NO    |       | YES         |       |
