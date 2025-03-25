erDiagram
    Rampa {
      int id_rampa PK
      int id_peca FK
      int qtde_r1
      int qtde_r2
      int qtde_descartada
    }

    Peca {
      int id_peca PK
      varchar tipo_peca
    }

    Monitoramento {
      int id_monitoramento PK
      int id_peca FK
      boolean esteira_on_off
      boolean atuador_on_off
      timestamp data_hora_monitoramento
      int erros
    }

    Peca ||--o{ Rampa : "possui"
    Peca ||--o{ Monitoramento : "gera"
