<!-- # README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ... -->

## Locations テーブル

| Column              | Type     | Options                             |
| ------------------- | -------- | ----------------------------------- |
| name                | string   | null: false                         |
| region_code         | string   | null: false, unique: true           |
| created_at          | datetime | null: false                         |
| updated_at          | datetime | null: false                         |

### Association
has_many :weather_forecasts


## WeatherForecasts テーブル

| Column              | Type     | Options                             |
| ------------------- | -------- | ----------------------------------- |
| date                | date     | null: false                         |
| location_id         | integer  | null: false                         |
| weather_status      | string   | null: false                         |
| temperature         | float    | null: false                         |
| humidity            | float    | null: false                         |
| created_at          | datetime | null: false                         |
| updated_at          | datetime | null: false                         |

### Association
belongs_to :location
