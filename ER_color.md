```startuml
@startuml

!define MASTER_MARK_COLOR Orange 
!define TRANSACTION_MARK_COLOR DeepSkyBlue
!define MAIN_ENTITY #MintCream-MistyRose
skinparam class {
    BackgroundColor Snow
    BorderColor Black
    ArrowColor Black
}

package "ECサイト" as target_system {
    

    entity "顧客マスタ" as customer <m_customers> <<M,MASTER_MARK_COLOR>> {
        + customer_code [PK]
        --
        pass
        name
        address
        tel
        mail
        del_flag
        reg_date
    }
    
     entity "顧客" as customer <m_customer> <<M,MASTER_MARK_COLO>> {
        + customer_code [PK]
        --
        pass
        name
        address
        tel
        mail
        del_flag
        reg_date
    }
    
  }
  
  
@enduml
```
