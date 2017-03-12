
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

    belongs_to :user
    belongs_to :group

  2. Usersテーブル

    | Field | Type    | Null  | Unique| Foreign_key | Index |
    | :----:| :----:  | :----:| :----:| :----------:| :----:|
    | id    | integer | NO    |       |             |       |
    | name  | string  | NO    |       |             |   YES |
    | email | string  | NO    | YES   |             |       |
    | password | string | NO  |       |             |       |

    has_many :messages
    has_many :groups, through: :users_gruops

  3. Groupsテーブル

    | Field | Type    | Null  | Unique| Foreign_key | Index |
    | :----:| :----:  | :----:| :----:| :----------:| :----:|
    | id    | integer | NO    |       |             |       |
    | name  | string  | NO    |       |             |   YES |

    has_many :messages
    has_many :users,  through: :users_gruops

 4. Users_Groupsテーブル

    | Field    | Type    | Null  | Unique| Foreign_key | Index |
    | :----:   | :----:  | :----:| :----:| :----------:| :----:|
    | id       | integer | NO    |       |             |       |
    | user_id  | integer | NO    |       | YES         |       |
    | group_id | integer | NO    |       | YES         |       |

    belongs_to :user
    belongs_to :group
