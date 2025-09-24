
# Função `calcularRank`

## 📌 Objetivo  
A função **`calcularRank`** tem como finalidade calcular o **saldo de vitórias** de um jogador e classificá-lo em um **nível de ranqueamento** com base na quantidade total de vitórias.

---

## ⚙️ Estrutura da Função  

```javascript
function calcularRank(vitorias, derrotas) {
  let saldoVitorias = vitorias - derrotas;
  let nivel = "";

  if (vitorias < 10) {
    nivel = "Ferro";
  } else if (vitorias >= 11 && vitorias <= 20) {
    nivel = "Bronze";
  } else if (vitorias >= 21 && vitorias <= 50) {
    nivel = "Prata";
  } else if (vitorias >= 51 && vitorias <= 80) {
    nivel = "Ouro";
  } else if (vitorias >= 81 && vitorias <= 90) {
    nivel = "Diamante";
  } else if (vitorias >= 91 && vitorias <= 100) {
    nivel = "Lendário";
  } else if (vitorias >= 101) {
    nivel = "Imortal";
  }

  return `O Herói tem de saldo de **${saldoVitorias}** está no nível de **${nivel}**`;
}

```

---

## 📥 Parâmetros

vitorias (number) → Quantidade de partidas vencidas.

derrotas (number) → Quantidade de partidas perdidas.



---

## 🧮 Regras de Negócio

1. O saldo de vitórias é calculado pela fórmula:

saldoVitorias = vitorias - derrotas


2. O nível do jogador é determinado pelo número total de vitórias, de acordo com as faixas abaixo:



# Faixa de Vitórias	Nível

## Menos de 10	Ferro
11 – 20	Bronze
21 – 50	Prata
51 – 80	Ouro
81 – 90	Diamante
91 – 100	Lendário
101 ou mais	Imortal



---

## 📤 Retorno

A função retorna uma string formatada no seguinte padrão:

"O Herói tem de saldo de X está no nível de Y"

Onde:

X = saldo de vitórias.

Y = nível correspondente.



---

## 🚀 Exemplo de Uso

let resultado = calcularRank(85, 20);
console.log(resultado);

### ✅ Saída Esperada:

O Herói tem de saldo de **65** está no nível de **Diamante**


---

## 💻 Instalação e Execução

### Pré-requisitos

Ter o Node.js instalado


### Passo a passo

1. Clone este repositório ou copie o código para um arquivo chamado index.js.


2. Abra o terminal na pasta onde o arquivo está salvo.


3. Execute o comando:



node index.js

4. O resultado será exibido no console.
