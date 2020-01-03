## usersテーブル|Column|Type|Options|
|Column|Type|Options|
|---|------|----|-------|
|user|string|null:false|
|email|string|null: false|
|password|string|null: false｜
### Association
- has_many :groups, through: :groups_users
- has_many :messages


## messagesテーブル
|Column|Type|Options|
|------|----|-------|
|image|string||
|text|text||
|user_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user
- belongs_to :message

## groups_usersテーブル
|Column|Type|Options|
|------|----|-------|
### Association
- belongs_to :user
- belongs_to :group
- has_many :groups_users



## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|group|integer|null: false|
### Association
- has_many :users through: :groups_users
- has_many :messages
















