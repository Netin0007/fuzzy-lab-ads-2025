# Projeto de Sistema Fuzzy: Avaliação de Qualidade de Produto

## 👥 Identificação da Dupla
| Edilson Gonçalves Alves | Netin0007 |
| Paulo Cosmo | Paulo Cosmo55 |

## 🎯 Tema Escolhido
**Tema B – Avaliação de Qualidade de Produto**

## 📝 Descrição do Problema
Em uma fábrica, dizer se um produto é "Bom" ou "Ruim" nem sempre é fácil. Às vezes, o processo de fabricação variou um pouco, ou o produto tem um defeito muito pequeno. 

Nosso problema é criar um sistema que consiga dar uma **nota de 0 a 10** para a qualidade do produto, analisando duas coisas ao mesmo tempo: o quanto a produção variou e quantos defeitos foram encontrados. O objetivo é imitar a decisão de um inspetor humano.

## 📅 Planejamento Inicial

### 1. Entradas (O que o sistema vai ler)

1.  **Variabilidade do Processo**: Mede se a produção foi estável ou instável.
    * *Escala:* 0 a 100%.
    * *Categorias:* Baixa, Média, Alta.
2.  **Grau de Defeitos**: Mede a gravidade dos problemas encontrados.
    * *Escala:* 0 a 10.
    * *Categorias:* Pouco, Moderado, Muito.

### 2. Saída (O que o sistema vai responder)

1.  **Qualidade Final**: A nota final do produto.
    * *Escala:* 0 a 10.
    * *Categorias:* Ruim, Aceitável, Excelente.

### 3. Formato das Gráficos (Funções de Pertinência)
Para facilitar o início do projeto, vamos usar formas geométricas simples para definir as categorias acima:
* Usaremos **Triângulos** e **Trapézios**.
* *Motivo:* São mais fáceis de entender e de processar pelo computador do que curvas complexas.

### 4. Regras do Sistema
O sistema vai funcionar baseada em regras do tipo "SE... ENTÃO...".
* *Exemplo:* SE a Variabilidade for Alta OU tiver Muitos Defeitos, ENTÃO a Qualidade é Ruim.
* *Exemplo:* SE a Variabilidade for Baixa E tiver Poucos Defeitos, ENTÃO a Qualidade é Excelente.

### 5. Métodos Escolhidos
* **Inferência:** Mamdani (É o método mais comum e intuitivo para iniciantes).
* **Cálculo Final (Defuzzificação):** Centroide (Calcula a média para dar o número exato da nota).

### 6. Testes Planejados
Vamos testar 3 situações para ver se funciona:
1.  **Produto Perfeito:** 0% variabilidade e 0 defeitos -> Esperamos nota alta (perto de 10).
2.  **Produto Péssimo:** 100% variabilidade e muitos defeitos -> Esperamos nota baixa (perto de 0).
3.  **Produto Médio:** Um pouco de cada -> Esperamos uma nota mediana (perto de 5).
