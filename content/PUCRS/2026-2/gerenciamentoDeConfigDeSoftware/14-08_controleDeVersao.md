---
title: Controle de Versão (17/08)
---
Professor: Daniel Callegari
Local: Prédio 32, sala 415
Horário: NP (17:30 -> 19:00)
## Descrição da Aula:
Começamos entendendo o histórico de ferramentas de controle de versão, e as características principais de cada evolução:
- Revision Control System: introduz o conceito de um main e do repositório central;
- Concurrent Version System Config: permite o merge e facilita o gerenciamento de configurações;
- Subversion: Integra bancos de dados e possibilita o uso de metadados;
- Git: revolucionário, possibilita criar vários repositórios, branches e essencialmente permite que uma cópia de um repositório externo no computador de cada contribuidor.

Depois, buscamos compreender um pouco sobre como funciona a função merge, essencial ao controle de versão. Ao contrário do que imaginamos, ela não lê o código, apenas compara a versão antiga e nova de um arquivo, identifica as diferenças e mescla o necessário.
No seguir da aula, exploramos mais sobre os comandos e funcionamentos básicos do Git, entendendo os comandos de bash como ```git add``` e ```git commit```, buscando compreender como que funciona o processo de controle de versão. Usando ferramentas de visualização, vimos concretamente como que o merge do Git funciona, e como as commits são salvas no sistema.
## Aspectos Importantes: 
- O Git foi criado por Linus Torvalds, o mesmo criador do Linux;
- Diferentes versões de arquivos podem ser classificadas em paralelas ou sequenciais. Sequenciais implicam uma evolução ou correção no arquivo original, enquanto paralelas indicam variações de um mesmo código.