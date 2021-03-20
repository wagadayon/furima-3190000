## users table
| Column | Type | Options |
| ------ | ---- | ------- |
|  nickname       | string     |  null: false      |
|  email  |   string   |  null: false       |
|  last_name  |  string    |  null: false       |
|  first_name     |    string  | null: false        |
|  last_name_kana  |   string   |  null: false       |
|  first_name_kana     | string     |  null: false       |
| birthday       |  data    |    null: false     |

- has_one :address
- has_one :credit
- has_many :creditcards
- has_many :items
- has_many :comments



## address table
| Column | Type | Options |
| ------ | ---- | ------- |
| postcode    |  string    |  null: false       |
| prefecture | string | null: false |
| municipality | string | null: false |
| address | swtring | null: false |
| romm_number | string | null: false |
| phone | string | null: false|

- belongs_to: user


## item table
| Column | Type | Options |
| ------ | ---- | ------- |
| name | string | null: false |
| explanation | string | null: false |
| brand | string | null: false |
| condition | string | null: false |
| postage | date| null: false |
| area | string | null: false |
| price | integer | null: false |
| days | data | null:false |
| user_id | integer | null: false, foregin_key : true |

- has_many: comments
- belongs_to: user



## credit table
| Column | Type | Options |
| ------ | ---- | ------- |
| user_id | integer | null: false, foregin_key : true |
| customer_id | integer | null: false, foregin_key : true |
| card_id | integet | null: false, foregin_key : true |

- belongs_to: user 



## commets table
| Column | Type | Options |
| ------ | ---- | ------- |
| item_id | integer | null: false, foregin_key : true |
| user_id | integer | null: false, foregin_key : true |
| comment | text | null: false |

- belongs_to: user
- belongs_to: user



