---
title: Atividade - Requisitos Não Funcionais do Uber (12/08)
---
Professor: Azriel Majdenbaum
Local: Prédio 15, sala 318
Horário: NP (21:00 -> 22:30)

Faça um levantamento dos requisitos não funcionais do Uber e associe-os às categorias vistas em aula.

| Requisitos Não Funcionais                | Uber                                                                                                                                                     |
| ---------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Confiabilidade                           | O sistema deve manter a disponibilidade do serviço mesmo durante períodos de alta demanda, minimizando falhas nas solicitações de viagens.               |
| Disponibilidade                          | Deve ser possível agendar corridas à qualquer momento do dia                                                                                             |
| Recuperabilidade                         | Ao falhar em encontrar um motorista no tempo limite, o sistema deve imediatamente voltar a procurar conexões.                                            |
| Recuperação de Desastres                 | O Uber devolve o dinheiro em caso de ocorrência de um sinistro.                                                                                          |
| Eficácia                                 | Usando algoritmos de buscas, o aplicativo consegue encontrar uma corrida de maneira rápida que seja boa tanto para o passageiro quanto para o motorista. |
| Exatidão e Precisão                      | O cálculo da rota deve ser eficiente e coerente com a realidade                                                                                          |
| Número de Defeitos                       | Deve haver um limite de 10 erros por cada 500 linhas de código (?)                                                                                       |
| Maturidade                               | Atualizações mensais devem ocorrer, corrigindo erros no sistema.                                                                                         |
| Previsão de Confiabilidade               | O usuário deve conectar com um motorista acima de 4 estrelas 95% de suas corridas.                                                                       |
| Resiliência/robustez/tolerância a falhas | As corridas devem ser registradas no servidor, impedindo que quedas de internet afetem o resultado.                                                      |
| Tempo médio entre falhas                 | No caso de manutenção de sistema, o usuário não deve ser impedido de continuar utilizando o aplicativo.                                                  |
| Frequência e gravidade de falha          | O Uber deve impedir que qualquer falha resulte no prejuízo monetário do motorista ou usuário.                                                            |
| Compatibilidade                          | Usar sistema de GPS e API do Google Maps                                                                                                                 |
| Coexistência                             | O aplicativo do Uber deve estar disponível em segundo plano.                                                                                             |
| Interoperabilidade                       | O sistema deve oferecer promoções em pedidos no aplicativo IFood                                                                                         |
| Performance / Eficiência                 | O sistema deve conectar o usuário com um motorista com 98% de eficácia                                                                                   |
| Escalabilidade                           | O sistema deve comportar mais de um milhão de motoristas.                                                                                                |
| Capacidade dinâmica                      | O sistema deve permitir o usuário a pedir mais de uma corrida por vez                                                                                    |
| Capacidade estática                      | O banco de dados do Uber deve armazenar as informações de mais de 200 milhões de usuários com segurança                                                  |
| Manutenção / Suporte                     | O sistema deve permitir atualizações e correções sem interromper o serviço.                                                                              |
| Portabilidade                            | O aplicativo do Uber deve estar disponível em dispositivos Android e IOS                                                                                 |
| Usabilidade                              | Ao abrir o aplicativo, o usuário deve imediatamente ser apresentado à função principal do aplicativo.                                                    |
| Segurança                                | Segue a Lei Geral de Proteção de Dados (LGPD) de maneira correta.                                                                                        |
| Restrições de Desenho / Projeto          | O usuário pode criar uma corrida com até 5 paradas.                                                                                                      |
| Comerciais                               | O aplicativo deve permitir pagamento por PIX, Cartão de Crédito e Dinheiro.                                                                              |
| Legais                                   | O Uber é obrigado a emitir nota fiscal após cada corrida.                                                                                                |
| Éticos                                   | Deve ser oferecida uma opção de cobrir parte do custo ao meio ambiente (Uber Planet)                                                                     |
| Acessibilidade                           | O usuário deve ter a opção de alertar o motorista de deficiências sensoriais, permitindo uma viagem melhor                                               |