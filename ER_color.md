```startuml
@startuml

!define MASTER_MARK_COLOR Orange 
!define TRANSACTION_MARK_COLOR DeepSkyBlue
!define MAIN_ENTITY #MintCream-MistyRose

skinparam class {
    '図の背景
    BackgroundColor Snow
    '図の枠
    BorderColor Black
    'リレーションの色
    ArrowColor Black
}


package "ECサイト" as target_system {

entity "顧客マスタ" as customer<m_customers>
<<M,MASTER_MARK_COLOR>> {
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

entity "購入テーブル" as customer<d_purchase>
<<M,MASTER_MARK_COLOR>> {
+order_id[PK]
--
customer_code
purchase_date
total_price
}

}
  
@enduml
```
