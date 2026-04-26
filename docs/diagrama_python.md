# Diagrama UML - Codigo Python

## 1. Arquivos analisados

- `src_python/main.py`
- `src_python/equipamento.py`
- `src_python/sensor_temperatura.py`

## 2. Link do Mermaid Live

https://mermaid.ai/app/projects/0d31456e-f592-406b-a6fe-709bc045fe34/diagrams/46c6797f-cecd-498c-934a-4a09828183c5/share/invite/eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJkb2N1bWVudElEIjoiNDZjNjc5N2YtY2VjZC00OThjLTkzNGEtNGEwOTgyODE4M2M1IiwiYWNjZXNzIjoiVmlldyIsImlhdCI6MTc3NzIyNjU3M30.NzK7I9D0X9F73mwGSfKIr-9DB4BOcccuHQz6TSL8k4Q

## 3. Diagrama final em Mermaid

```mermaid
classDiagram

class Equipamento {
  -_tag: str
  -_descricao: str
  -_ativo: bool
  +ligar(): void
  +desligar(): void
  +tag: str
  +exibir_resumo(): void
}

class SensorTemperatura {
  -_valor_atual: float
  +atualizar_leitura(novo_valor: float): void
  +exibir_resumo(): void
}

Equipamento <|-- SensorTemperatura
```

## 4. Justificativa tecnica

Foram identificadas as classes Equipamento, que é a base do sistema, e SensorTemperatura, que é uma especialização. A relação entre elas é de herança no código, já que SensorTemperatura estende Equipamento e utiliza super() para reaproveitar o construtor. No diagrama, destacam-se as operações ligar() e desligar() da classe base, além de exibir_resumo(), que é sobrescrita (polimorfismo), e atualizar_leitura(), específica do sensor, bem como a propriedade tag, que evidencia encapsulamento. O UML representa corretamente o código em Python porque mostra a herança, os atributos internos, os métodos definidos e a sobrescrita de comportamento, mantendo a mesma estrutura lógica.

## 5. Evidencias

[Equipamento] EQ-01 - Agitador principal - ativo=True
[SensorTemperatura] TT-01 - valorAtual=23.5
[SensorTemperatura] TT-01 - valorAtual=24.2 aqui a saida do terminal, prints ou observacoes da execucao do codigo em `Python`.
