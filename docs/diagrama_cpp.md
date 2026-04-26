# Diagrama UML - Codigo C++

## 1. Arquivos analisados

- `src_cpp/main.cpp`
- `src_cpp/equipamento.hpp`
- `src_cpp/equipamento.cpp`
- `src_cpp/sensor_temperatura.hpp`
- `src_cpp/sensor_temperatura.cpp`

## 2. Link do Mermaid Live

https://mermaid.ai/app/projects/880f4207-6953-458f-b54d-636e3448b8b7/diagrams/d6701a61-0ad2-4232-ba01-f824e1f33015/share/invite/eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkb2N1bWVudElEIjoiZDY3MDFhNjEtMGFkMi00MjMyLWJhMDEtZjgyNGUxZjMzMDE1IiwiYWNjZXNzIjoiVmlldyIsImlhdCI6MTc3NzIyMjIwNH0.r9VpyhzPiW9ukhGnwVqVbpy4RzzGac0VmdXL-oT8LgQ

## 3. Diagrama final em Mermaid

```mermaid
classDiagram

class Equipamento {
  - string tag
  - string descricao
  - bool ativo
  + Equipamento(tagEquipamento : string, descricaoEquipamento : string, ativoInicial : bool)
  + ligar() void
  + desligar() void
  + getTag() string
  + estaAtivo() bool
  + exibirResumo() void
}

class SensorTemperatura {
  - double valorAtual
  + SensorTemperatura(tagSensor : string, descricaoSensor : string, ativoInicial : bool, valorInicial : double)
  + atualizarLeitura(novoValor : double) void
  + getValorAtual() double
  + exibirResumo() void
}

SensorTemperatura --|> Equipamento
```
## 4. Justificativa tecnica

Foram identificadas as classes Equipamento e SensorTemperatura, sendo a segunda uma especialização da primeira. A herança aparece na declaração SensorTemperatura : public Equipamento. As operações são ligar(), desligar(), getTag(), estaAtivo() e exibirResumo(), além de atualizarLeitura() e getValorAtual() na classe "filha". O UML está correto porque representa as classes, atributos, métodos, a herança e o polimorfismo do código.

## 5. Evidencias

[Equipamento] EQ-01 - Agitador principal - ativo=sim
[SensorTemperatura] TT-01 - valorAtual=23.5
[SensorTemperatura] TT-01 - valorAtual=24.2
