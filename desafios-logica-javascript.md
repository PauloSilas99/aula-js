# Desafios de Lógica em JavaScript
## 5 Desafios Essenciais

---

## 🟢 Desafio 1: Operadores Aritméticos - Calculadora Básica
Crie uma função que recebe dois números e realiza as quatro operações aritméticas básicas (soma, subtração, multiplicação e divisão).
Retorne um objeto com os resultados de cada operação.

**Exemplo:**
```javascript
calculadora(10, 5)
// {
//   soma: 15,
//   subtracao: 5,
//   multiplicacao: 50,
//   divisao: 2
// }

calculadora(8, 2)
// {
//   soma: 10,
//   subtracao: 6,
//   multiplicacao: 16,
//   divisao: 4
// }
```

**Solução:**
```javascript
function calculadora(a, b) {
  // Use os operadores: +, -, *, /
  // Seu código aqui
}
```

---

## 🟢 Desafio 2: If e Else - Classificar Nota
Crie uma função que recebe uma nota (de 0 a 10) e retorna a classificação usando if/else:
- "Excelente" se a nota for maior ou igual a 9
- "Bom" se a nota for maior ou igual a 7
- "Regular" se a nota for maior ou igual a 5
- "Insuficiente" se a nota for menor que 5

**Exemplo:**
```javascript
classificarNota(9.5)  // "Excelente"
classificarNota(7.0)   // "Bom"
classificarNota(6.0)   // "Regular"
classificarNota(4.0)   // "Insuficiente"
```

**Solução:**
```javascript
function classificarNota(nota) {
  // Use if e else para verificar as condições
  // Seu código aqui
}
```

---

## 🟢 Desafio 3: Operadores de Comparação - Verificar Faixa Etária
Crie uma função que recebe a idade de uma pessoa e retorna a faixa etária usando operadores de comparação (>, <, >=, <=):
- "Criança" se idade < 12
- "Adolescente" se 12 <= idade < 18
- "Adulto" se 18 <= idade < 60
- "Idoso" se idade >= 60

**Exemplo:**
```javascript
faixaEtaria(8)   // "Criança"
faixaEtaria(15)  // "Adolescente"
faixaEtaria(25)  // "Adulto"
faixaEtaria(65)  // "Idoso"
```

**Solução:**
```javascript
function faixaEtaria(idade) {
  // Use operadores de comparação: <, >, <=, >=
  // Seu código aqui
}
```

---

## 🟡 Desafio 4: Switch - Dia da Semana
Crie uma função que recebe um número (1 a 7) e retorna o nome do dia da semana usando switch.
- 1 = "Domingo"
- 2 = "Segunda-feira"
- 3 = "Terça-feira"
- 4 = "Quarta-feira"
- 5 = "Quinta-feira"
- 6 = "Sexta-feira"
- 7 = "Sábado"
- Qualquer outro número = "Dia inválido"

**Exemplo:**
```javascript
diaDaSemana(1)  // "Domingo"
diaDaSemana(3)  // "Terça-feira"
diaDaSemana(7)  // "Sábado"
diaDaSemana(10) // "Dia inválido"
```

**Solução:**
```javascript
function diaDaSemana(numero) {
  // Use switch com case e default
  // Seu código aqui
}
```

---

## 🟡 Desafio 5: For - Somar Números de 1 até N
Crie uma função que recebe um número N e usa um loop for para somar todos os números de 1 até N (inclusive).

**Exemplo:**
```javascript
somarAteN(5)   // 15 (1 + 2 + 3 + 4 + 5)
somarAteN(10)  // 55 (1 + 2 + 3 + ... + 10)
somarAteN(3)   // 6 (1 + 2 + 3)
somarAteN(1)   // 1
```

**Solução:**
```javascript
function somarAteN(n) {
  // Use um loop for para iterar de 1 até n
  // Seu código aqui
}
```

---

## 📝 Dicas para Resolver os Desafios

1. **Leia o problema cuidadosamente** - Entenda o que está sendo pedido
2. **Pense em casos extremos** - Arrays vazios, números negativos, strings vazias
3. **Teste com exemplos** - Use os exemplos fornecidos para validar sua solução
4. **Comece simples** - Resolva primeiro, otimize depois
5. **Use métodos de array** - map, filter, reduce podem simplificar muito

---

**Boa sorte com os desafios! 🚀**
