# Projeto 2 - Missão Orbital: Simulador de Treinamento Espacial

**Disciplina:** Algoritmos e Pensamento Computacional
**Professor:** Vinicius Alves
**Período:** 2026/2

## Integrantes do grupo

| Nome | RGM |
|------|-----|
| Laura Marques Ribeiro | 47228377 |
| Pedro Henrique Gelli Soares | 049385992 |
| Gabril Macio Emidio | 47280638 |

## Sobre a solução

O programa foi desenvolvido em linguagem C e simula o treinamento de cadetes espaciais na Missão Orbital. Para cada cadete avaliado, o usuário informa o código do cadete e a pontuação obtida em 3 etapas do treinamento. Ao final, o programa exibe um relatório com a pontuação total, a média e a classificação do cadete.

### Como funciona

1. O usuário digita o **código do cadete**.
2. O programa pede a **pontuação de cada uma das 3 etapas** (valores de 0 a 100).
3. Se a pontuação for inválida (menor que 0 ou maior que 100), o programa pede o valor novamente até que seja válido.
4. São calculados o **total de pontos** e a **média** (`total / 3.0`).
5. O cadete recebe uma classificação conforme a média.
6. O usuário escolhe se deseja avaliar outro cadete (`1` para sim, `0` para não).

### Classificação

| Média | Classificação | Mensagem |
|-------|---------------|----------|
| 85 ou mais | COMANDANTE DA MISSÃO | Treinamento concluído com excelência |
| 70 a 84,99 | PILOTO APROVADO | Cadete autorizado para a missão |
| 50 a 69,99 | CADETE EM RECUPERAÇÃO | Novo treinamento recomendado |
| Menos de 50 | TREINAMENTO REINICIADO | Cadete ainda não autorizado |

Se o cadete obtiver o total de **300 pontos** (100 em todas as etapas), o programa também exibe a mensagem **PONTUAÇÃO MÁXIMA!**.

### Recursos utilizados

- Variáveis dos tipos `int` (código, etapa, pontos, total e controle do laço) e `float` (média)
- `scanf()` para entrada de dados e `printf()` para exibir o relatório com a média em duas casas decimais
- Estrutura de repetição `for` para percorrer as 3 etapas
- Estrutura de repetição `while` para validar a pontuação digitada
- Estrutura de repetição `do...while` para avaliar vários cadetes na mesma execução
- Estruturas condicionais `if`, `else if` e `else` para definir a classificação

## Como compilar e executar

```bash
gcc projeto2_missao_orbital.c -o projeto2_missao_orbital
./projeto2_missao_orbital
```

## Exemplo de execução

```
===== MISSAO ORBITAL =====
Codigo do cadete: 101
Pontuacao da etapa 1: 90
Pontuacao da etapa 2: 80
Pontuacao da etapa 3: 85

---------- RESULTADO ----------
Cadete: 101
Pontuacao total: 255 pontos
Media: 85.00
Classificacao: COMANDANTE DA MISSAO
Treinamento concluido com excelencia.
-------------------------------
Avaliar outro cadete? 1-Sim | 0-Nao: 0
Sistema encerrado.
```
