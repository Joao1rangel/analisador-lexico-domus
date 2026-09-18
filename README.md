# Analisador Léxico — Linguagem Domus

Analisador léxico desenvolvido para a linguagem **Domus**, como parte do Trabalho 1 da disciplina de Compiladores (UVA), sob orientação do Prof. Fábio.

## 📋 Sobre o projeto

O analisador foi implementado utilizando o **Flex**, gerador automático de analisadores léxicos, que traduz um conjunto de expressões regulares em código C responsável por reconhecer os tokens da linguagem Domus (palavras-chave, identificadores, números, operadores, separadores e comentários multilinha).

## 🗂️ Estrutura do repositório

| Arquivo | Descrição |
|---|---|
| `analisador.l` | Código-fonte do Flex (regras léxicas) |
| `lex.yy.c` | Código C gerado automaticamente pelo Flex |
| `ExemploDomus.txt` | Arquivo de teste oficial, disponibilizado pelo professor |
| `Trabalho de Compiladores.pdf` | Relatório do trabalho (normas ABNT) |

## ⚙️ Como compilar e executar

### Linux / macOS
```bash
flex analisador.l
gcc lex.yy.c -o analisador
./analisador
```

### Windows (WinFlexBison + MinGW)
```bash
win_flex analisador.l
gcc lex.yy.c -o analisador.exe
analisador.exe
```

> ⚠️ O arquivo de teste (`ExemploDomus.txt`) precisa estar na mesma pasta do executável, com o nome exato esperado no código.

## 🧪 Tokens reconhecidos

O analisador reconhece: palavras-chave (`sensor`, `atuador`, `se`, `entao`, `senao`, `enquanto`, `escrever`...), identificadores, números inteiros, operadores aritméticos e relacionais (`+`, `-`, `<`, `<=`, `==`...), separadores (`.`, `:`, `(`, `)`) e comentários multilinha (`/* ... */`). Caracteres fora do alfabeto da linguagem são classificados como "Símbolo Desconhecido", sem interromper a análise.

## 👥 Autores

- João Pedro Salama Rangel
- Vinícius da Silva Nogueira
