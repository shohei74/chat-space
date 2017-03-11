
* Ruby version

* Database creation

    1. Messagesテーブル
        * id
        * body
        * image
        * email(一意性制約)
        * user_id(外部キー制約)
        * group_id(外部キー制約)

    2. Usersテーブル
        * id
        * name(NOT NULL制約)
        * email(NOT NULL制約、一意性制約)
        * password(NOT NULL制約)

    3. Groupsテーブル
        * id
        * name(NOT NULL制約、一意性制約)

    4. Relationsテーブル
        * id
        * user_id(外部キー制約)
        * group_id(外部キー制約)

