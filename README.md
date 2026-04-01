@startuml

left to right direction

actor "Шрек" as Shrek
actor "Фиона" as Fiona
actor "Дракон" as Dragon
actor "Лорд Фаркуад" as Kindom


package "Спасение принцессы" {
  usecase "Спасти принцессу" as HelpedFiona
  usecase "Победить дракона" as WictoryDragon
  usecase "Заключить сделку" as MakeDale
  usecase "Сражение с драконом" as FightDragon
  usecase "Принцесса сопротивляется" as NotProblem
  usecase "Захват принцессы" as Decision
}

Shrek --> MakeDale
Kindom --> MakeDale

Shrek --> FightDragon
Dragon --> FightDragon

Shrek --> WictoryDragon

Fiona -->NotProblem
Shrek -->Decision

FightDragon ..> WictoryDragon : <<include>>
WictoryDragon ..> HelpedFiona : <<include>>
Decision <..NotProblem :<<extend>>

Shrek --> HelpedFiona

@enduml
