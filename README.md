# README

## usersテーブル

|colum|Type|Options|
|-----|----|-------|
|name|string|null: false|
|email|string|null: false|
|passward|string|null: false|

### Assosiation
- has_many :messages
- has_many :groups_users
- has_many :groups through :groups_users

## groupsテーブル

|colum|Type|Options|
|-----|----|-------|
|name|string|null: false|
||||
||||

### Assosiation
- has_many :messages
- has_many :groups_users
- has_many :groups through :groups_users


## groups_usersテーブル

|colum|Type|Options|
|-----|----|-------|
|user_id|references|null: false, foreign_key: true|
|group_id|references|null: false, foreign_key: true|
||||

### Assosiation
- belongs_to :group
- belongs_to :user


## messagesテーブル

|colum|Type|Options|
|-----|----|-------|
|content|text||
|image|string||
|user_id|references|null: false, foreign_key :true|
|group_id|references|null] false, foreign_key :true|

### Assosiation
- belongs_to :user
- belongs_to :group



