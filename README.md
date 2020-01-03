## nameテーブル|Column|Type|Options|
|Column|Type|Options|
|---|------|----|-------|
|user|string|null:false|index: true|
|email|string|null: false|
|password|string|null: false｜
### Association
- has_many :groups, through: :groups_users
- has_many :messages
- has_many :groups_users

## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|image|string||
|text|text||
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user
- belongs_to :group


## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
|name_id|string|null:false|
|group_id|string|null:false|
### Association
- belongs_to :user
- belongs_to :group

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|name|string|null: false|
### Association
- has_many :users through: :groups_users
- has_many :messages
- has_many :groups_users
















