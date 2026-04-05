# Use Case Diagram: «Шрек» Миссия спасения

## Актеры

| Актер | Описание |
|-------|-------------|
| Лорд Фаркуад | Kindom |
| Шрек | Shrek |
| Фиона | Fiona |
| Дракон | Dragon |

## Варианты использования

### Пакет: «Шрек» Миссия спасения

| Вариант использования | Описание |
|----------|-------------|
| Спасти принцессу | HelpedFiona|
| Победить дракона | WictoryDragon |
| Заключить сделку| MakeDale |
| Сражение с драконом | FightDragon |
| Принцесса сопротивляется | NotProblem |
| Захват принцессы | Decision |

## Связи

### Актер к варианту использования

- **Шрек** и **Лорд Фаркуад** выполняют: Заключить сделку
- **Шрек** выполняет: Победить дракона
- **Дракон** и **Шрек** выполняют: Сражение с драконом
- **Фиона** и **Шрек** выполняют: Принцесса сопротивляется

### Отношения Extend/Include

- **Захват принцессы** ←← **Принцесса сопротивляется** (<<extend>>): если плачут
- **Сражение с драконом** →→ **Победить дракона** (<<include>>)

## Диаграмма

![Диаграмма вариантов использования](use_case.png)

```
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
```

## Описание

Эта диаграмма вариантов использования иллюстрирует сценарий сказки, связанный с историей "Курочка Ряба":

1. **Шрек** и **Лорд Фаркуад** заключают сделку,
2.  после **Шрек** сражается с **Драгоном** и побеждает,
3. затем **Шрек** захватывает **Фиону**
