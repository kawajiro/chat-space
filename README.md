## usersテーブル|Column|Type|Options|
|Column|Type|Options|
|---|------|----|-------|
|user|string|null:false|
|email|string|null: false|
|password|string|null: false｜
### Association
- has_many :groups, through: :users_groups

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|image|string||
|text|text||
|user_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :users
- belongs_to :messages

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
### Association
- belongs_to :users
- belongs_to :groups


## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|group|integer|null: false|
### Association
- belongs_to :users
- has_many_messages















