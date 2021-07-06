```startuml
@startuml

package "ECサイト" as target_system {

entity "顧客マスタ" as customer<m_customers>{
+customer_code[PK]
--
pass
name
address
tel
mail
del-flag
reg_date
}

entity "購入テーブル" as customer<d_purchase>{
+order_id[PK]
--
customer_code
purchase_date
total_price
}

}
  
@enduml
```
