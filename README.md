# Projeto 1 - Arena Tech: Planejador de Maratona Gamer

**Disciplina:** Algoritmos e Pensamento Computacional
**Professor:** Vinicius Alves
**Período:** 2026/2

## Integrantes do grupo

| Nome | RGM |
|------|-----|
| Gabriel Maciel | 4728638 |
| Pedro Henrique Gelli Soares | 049385992 |
| Laura Marques Ribeiro | 47228377 |

## Sobre a solução

O programa foi desenvolvido em linguagem C e tem como objetivo auxiliar na organização da Arena Tech, uma maratona gamer no campus. Ele solicita ao usuário, via teclado, oito informações sobre o evento:

1. Quantidade de participantes
2. Jogadores por time
3. Quantidade de computadores
4. Potência média de cada computador
5. Duração do evento
6. Preço do kWh de energia
7. Preço do kit de alimentação
8. Outros custos

A partir desses dados, o programa calcula a quantidade de times necessários, arredondando o resultado para cima com a função `ceil()` da biblioteca `math.h`, já que um time incompleto ainda conta como um time. Também são calculados:

- O consumo estimado de energia (kWh)
- O custo da energia
- O custo da alimentação (um kit por participante)
- O custo total do evento
- O custo médio por participante

### Recursos utilizados

- Variáveis dos tipos `int` (valores inteiros, como participantes e computadores) e `float` (valores decimais, como preços e potência)
- `scanf()` para entrada de dados
- `printf()` para exibir o relatório final formatado com duas casas decimais
- Biblioteca `math.h` (função `ceil()`)

Não foram usadas estruturas condicionais ou de repetição, conforme solicitado pelo projeto.

## Teste realizado

O programa foi testado com os dados do teste mínimo obrigatório:

| Entrada | Valor |
|---------|-------|
| Participantes | 25 |
| Jogadores por time | 3 |
| Computadores | 20 |
| Potência média | 600 W |
| Duração | 2 horas |
| Preço do kWh | R$ 1,00 |
| Kit de alimentação | R$ 25,00 |
| Outros custos | R$ 200,00 |

O resultado obtido (**CUSTO TOTAL: R$ 849,00**) bateu corretamente com o exemplo apresentado no PDF do professor.

## Como compilar e executar

```bash
gcc projeto1_arena_tech.c -o projeto1_arena_tech -lm
./projeto1_arena_tech
```
