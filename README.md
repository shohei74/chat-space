== README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

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
        * user_id(外部キー制約)

    4. Relationsテーブル
        * id
        * user_id(外部キー制約)
        * group_id(外部キー制約)

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


Please feel free to use a different markup language if you do not plan to run
<tt>rake doc:app</tt>.
