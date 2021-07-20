```uml
@startuml
start
:weather=天気情報;
if (weather==0) then(yes)
:快晴です;
elseif (weather==1) then(yes)
:曇りです;
elseif (weatehr==2) then(yes)
:雨です;
else(no)
:不明です;
endif
end

@enduml

```
