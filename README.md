# 🗳️ Algoritmo de Votação Tideman

Este programa em C implementa o sistema de votação **Tideman (Ranked Pairs)**, um método de votação preferencial que cria uma estrutura de pares ordenados para determinar um vencedor sem ciclos inconsistentes.

## 📌 Funcionalidades
- ✅ Permite que os eleitores classifiquem os candidatos por ordem de preferência.
- ✅ Calcula pares de vencedores e perdedores com base nas preferências dos eleitores.
- ✅ Ordena os pares em ordem decrescente de força de vitória.
- ✅ Usa um grafo para travar pares sem criar ciclos.
- ✅ Determina e imprime o vencedor final.

## 📥 Como Compilar e Executar

1. **Compile o código** usando o `clang` ou `gcc`:
   ```sh
   clang -o tideman tideman.c -lcs50
   ```  
   ou  
   ```sh
   gcc -o tideman tideman.c -lcs50
   ```  

2. **Execute o programa** especificando os candidatos na linha de comando:
   ```sh
   ./tideman Alice Bob Charlie  
   ```  

3. **Informe o número de eleitores** e classifique os candidatos em ordem de preferência.

4. O sistema calculará o vencedor e o exibirá na tela. 🎉

## 📖 Exemplo de Uso
```sh
$ ./tideman Alice Bob Charlie  
NÚMERO DE ELEITORES: 3  
VENCEDOR 1: Alice  
VENCEDOR 2: Bob  
VENCEDOR 3: Charlie  

VENCEDOR 1: Bob  
VENCEDOR 2: Charlie  
VENCEDOR 3: Alice  

VENCEDOR 1: Charlie  
VENCEDOR 2: Alice  
VENCEDOR 3: Bob  

RESULTADO: Alice 🎉
```

## ⚠️ Regras e Limitações
- O número máximo de candidatos é **9**.
- Se houver um empate geral, múltiplos vencedores podem ser declarados.
- O algoritmo impede ciclos na estrutura de votação para garantir a validade dos resultados.

## 🛠️ Estrutura do Código
O código contém as seguintes funções principais:

- `vote()`: Registra a ordem de preferência dos eleitores.
- `record_preferences()`: Armazena as preferências de cada eleitor.
- `add_pairs()`: Cria pares de vencedores e perdedores com base nas preferências.
- `sort_pairs()`: Ordena os pares por força da vitória.
- `lock_pairs()`: Bloqueia pares em um grafo sem formar ciclos.
- `print_winner()`: Identifica e imprime o vencedor da eleição.

## 📜 Licença
Este projeto é de código aberto e pode ser modificado e distribuído livremente.

## REDME CREADO POR IA 

