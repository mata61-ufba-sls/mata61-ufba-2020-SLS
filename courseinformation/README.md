# MATA61 - Compiladores
Disciplina MATA61 realizada no [SLS - Semestre Letivo Complementar da UFBA](https://ufbaemmovimento.ufba.br/)

## Informações sobre a disciplina

+ [Programa da disciplina](https://github.com/ensino-ufba/mata61_sls_public/blob/master/about/MATA61-Programa-20122.pdf)
+ AVA
  - Google Classroom, código da turma: 7y3lipq

---
## Objetivos

- Parte teórica: Entender os conceitos fundamentais envolvidos na implementação de linguagens de programação;
- Parte prática:
   - Implementar um compilador aplicando técnicas de análise e síntese/geração de código;
   - Aplicar técnicas para construção de analisadores léxicos e sintáticos;
   - Aplicar técnicas para construção de analisadores semânticos e geradores de código;
- Reconhecer a importância do trabalho colaborativo, em equipe, para a construção de um produto de software básico de relativa complexidade.

---
## Metodologia (SLS)

+ Aulas síncronas e assíncronas, com estudo dirigido e vídeo-aulas expositivas (assíncronas) e um encontro semanal, online para tirar dúvidas sobre atividades assíncronas
+ Sala de aula invertida, com vídeos, leituras recomendadas e exercícios (atividades assíncronas), e fórum de discussão/dúvidas e quiz (atividades síncronas)
+ Avaliação por meio de trabalhos de programação em equipe, provas individuais, exercícios de resolução de problemas (individuais e em equipe) e quiz.

Uso de vídeo-aula expositiva, fórum de discussão, estudo dirigido, trabalhos em grupo, quiz e lista de exercícios; uso de AVA (Moodle ou Classroom), Meet ou WebConf (RNP) e Github.

## Tópicos

1. Análise léxica e autômatos finitos (_scanning_)
2. Análise sintática (_parsing_) com abordagens _top-down_ e _bottom-up_
3. Representação de programas com árvores sintáticas abstratas (_Abstract Syntax Trees (AST)_)
4. Tabela de símbolos e regras de escopo para linguagens _C-like_
5. Verificação de tipos para linguagens _C-like_
6. Código intermediário (_intermediate code (IR)_)
7. Otimização local e global
8. Pilhas e registros de ativação
9. Geração de código
<!--10. Basic blocks, control-flow graphs, liveness analysis, register allocation -->

## Avaliação de Aprendizagem

Os seguintes dispositivos de avaliação processual ou formativa, serão utilizados:
+ individual - um trabalho prático (analisador léxico),  diário online, provas, exercícios e quiz, com avaliação do docente;
+ em equipe - três trabalhos práticos, com avaliação do docente e por pares.

A participação do estudante será aferida por meio de sua participação individual no fórum da disciplina, na realização das tarefas disponíveis no ambiente virtual de aprendizagem, exercícios, quizzes e nos trabalhos -- individuais e em equipe.

### Projeto Prático

Projetar e implementar um compilador (incluindo Analisador Léxico, Analisador Sintático, Analisador Semântico e Gerador de Código) para uma linguagem simples procedimental.

   - Trabalho 1: Analisador Léxico (individual)
   - Trabalho 2: Analisador Sintático
   - Trabalho 3: Analisador Semântico
   - Trabalho 4: Gerador de Código.

### Provas
   - Prova 1: Análise Léxica, Análise Sintática (Top-down e Bottom-up), Análise Semântica (Escopo e Tipos) - offline, múltipla escolha, correção automática, 10 questões - 24 horas no ar.
   - Prova 2: Ambiente de execução, Geração de Código, Alocação de registradores, Gerenciamento Automático de Memória -  offline, múltipla escolha, correção automática, 10 questões - 24 horas no ar.

### Fórum de Discussão

   - Discord

### Exercícios Individuais

   - Classroom - UFBA

### Pesos **(NEW)** 

+ 30% Participação em fóruns, quiz e exercícios individuais / em equipe
   - Participação em fóruns (3%)
   - Quiz(2%)
   - Exercícios individuais (10%)
   - Exercícios em equipe (15%)
+ 70% Projeto e implementação de um compilador:
   - TP1 (10%)
   - TP2 (45%)
   - TP3 (15%)

### Pesos (OLD)

+ 15% Prova 1, 15% Prova 2
+ 25% Participação em fóruns, quiz e exercícios individuais
+ 45% Projeto e implementação de um compilador, organizado em 4 trabalhos práticos, sendo o primeiro individual (analisador léxico) e os demais em equipe (com 3 ou 5 pessoas).

## Material do Curso

   - Classroom - UFBA

## Referênciais bibliográficas

### Principal

Livro do "Dragão": Aho, Lam, Sethi, and Ullman. Compiladores: princípios, técnicas e ferramentas. 2a edição, Addison-Wesley, 2008.

- Analise Léxica e Automatos Finitos.
Seções de Capítulos: 3.1, 3.3, 3.4, 3.6, 3.7, 3.8
- Analise Sintática.
Seções de Capítulos: 4.1-4.6, 4.8.1, 4.8.2
- Analise Semântica e Tipos.
Seções de Capítulos: 5.1-5.3 6.3, 6.5
- Ambiente de Execução e Geração de Código.
Seções de Capítulos: 6.2, 7.1-7.4, 8.1-8.3, 8.6
- Otimização de codigo.
Seções de Capítulos: 8.5, 8.7, 9.1-9.4
- Alocação de registradores e Gerenciamento automático de memória.
Seções de Capítulos: 8.8, e 7.5-7.7

### Outras

+ LOUDEN, K. C.. Compiladores: Princípios e Práticas. Editora Thompson Pioneira, 1a edição, 2004.
+ RICARTE, I. Introdução à Compilação, Editora Campus, 2008.
