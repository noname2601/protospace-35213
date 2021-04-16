# テーブル設計

## users テーブル

| Column    | Type   | Options     |
| --------  | ------ | ----------- |
| email     | string | null: false |
| password  | string | null: false |
| name      | string | null: false |
| profile   | text   | null: false |
| occupation| text   | null: false |
| position  | text   | null: false |

### Association

- has_many :room_users
- has_many :rooms, through: room_users
- has_many :messages

## prototypes テーブル

| Column | Type   | Options     |
| ------ | ------ | ----------- |
| title   | string | null: false |
| catch_copy| text | null: false |
| concept | text | null: false |
| image   | ActiveStorageで実装 |
| user   | references型 |


### Association

## comments

| Column    | Type   | Options     |
| --------  | ------ | ----------- |
| text     | text | null: false |
| user     | references型 |
| prototype| references型 |





