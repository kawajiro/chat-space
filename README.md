## usersテーブル|Column|Type|Options|
|Column|Type|Options|
|---|------|----|-------|
|user|string|null:false|
|email|string|null: false|
|password|string|null: false｜
### Association
- has_many :users_groups

## photos&messageテーブル
|Column|Type|Options|
|------|----|-------|
|photo|text||
|text|text||
|user_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :users

## groups_usersテーブル

|Column|Type|Options|
|------|----|-------|
|user_id|integer|null: false, foreign_key: true|
|group_id|integer|null: false, foreign_key: true|
|comment_id|text|null: false, foreign_key: true|
|photo_id|integer|null:false, foreign_key: true|

### Association
- has_many :users_group

## groupsテーブル
|Column|Type|Options|
|------|----|-------|
|integer|integer|null: false|
|comment_id|text|null: false, foreign_key: true|
|photo_id|integer|null: false, foreign_key: true|
|user_id|integer|null: false, foreign_key: true|
### Association
- belongs_to :user















