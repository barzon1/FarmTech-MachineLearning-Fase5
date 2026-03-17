# 🌾 FarmTech Solutions - Previsão de Safra e Arquitetura em Nuvem

**Aluno:** Lucas Barzon
**RM:** RM567914

## 📌 Sobre o Projeto
Este repositório contém as Entregas 1 e 2 do projeto FarmTech Solutions. O objetivo é utilizar Inteligência Artificial para prever o rendimento (Yield) de diferentes culturas agrícolas com base em dados climáticos, além de planejar a infraestrutura em nuvem necessária para hospedar a solução em produção.

---

## 🤖 Entrega 1: Modelos de Inteligência Artificial

Foram desenvolvidos, treinados e testados 5 algoritmos preditivos diferentes para entender o padrão matemático de colheita da fazenda. 

**Resultados dos Modelos Testados:**
1. **Linear Regression:** R² de 99.50% | Erro Médio (MAE): 3.132 t
2. **Decision Tree Regressor:** R² de 99.18% | Erro Médio (MAE): 3.440 t
3. **Random Forest:** R² de 99.42% | Erro Médio (MAE): 2.739 t 🏆 **VENCEDOR**
4. **SVR:** R² de -30.51% | Erro Médio (MAE): 38.804 t
5. **Gradient Boosting:** R² de 99.05% | Erro Médio (MAE): 3.066 t

**conclusão:**
O modelo escolhido para ser implementado na fazenda é o **Random Forest Regressor**. 
Embora a Regressão Linear tenha obtido uma nota R² marginalmente superior, o modelo de Floresta Aleatória provou ser muito mais preciso na predição de valores absolutos, entregando o menor Erro Médio Absoluto (MAE) de todos os testes. Em logística agrícola, errar a estimativa por volumes menores (quase 400 toneladas de diferença para o segundo colocado) impacta positivamente a economia no aluguel de caminhões e silos de armazenamento. A inteligência coletiva de múltiplas árvores de decisão lidou perfeitamente com a diferença de escala de produção entre culturas como o Cacau e o Dendê.

🎥 **Vídeo de Demonstração (Código e Execução):** [COLE O SEU LINK DO YOUTUBE AQUI]

---

## ☁️ Entrega 2: Arquitetura em Nuvem (AWS)

Para que a Inteligência Artificial fique disponível 24/7 para os agrônomos, foi realizado um orçamento comparativo utilizando a calculadora oficial da AWS com as seguintes observações: **Amazon EC2 (t3.micro | 2 vCPUs | 1 GB RAM | 50 GB EBS de armazenamento)**.

**Orçamento Comparativo:**
* 🇺🇸 **Região Leste dos EUA (Norte da Virgínia):** $ 7.80 USD / mês
* 🇧🇷 **Região América do Sul (São Paulo):** $ 13.73 USD / mês

**Justificativa:**
Para hospedar o modelo de Inteligência Artificial da FarmTech, a decisão técnica e financeira correta é alugar o servidor nos **Estados Unidos**.

Na Arquitetura de Nuvem, a escolha do local do servidor depende principalmente de quão importante é a velocidade de resposta (o famoso “ping”). Em alguns casos, como operações de day trade no mercado financeiro ou equipamentos de UTI em hospitais, qualquer pequeno atraso pode causar problemas. Por isso, nesses casos o servidor precisa estar no Brasil para que a informação chegue o mais rápido possível.

Já no nosso caso é diferente. O modelo que estamos usando analisa ciclos de colheita que levam meses para acontecer. Então, se a previsão demorar cerca de 100 milissegundos a mais para aparecer no tablet do funcionário no campo, isso não faz diferença na prática e não prejudica o trabalho. 

Portanto, pagar quase 80% a mais (aumento de $7.80 para $13.73) por uma máquina no Brasil não se justifica tecnicamente para este escopo. A hospedagem nos EUA entrega a mesma capacidade computacional, gerando uma grande redução de custos (Cost Optimization) para a fazenda.

🎥 **Vídeo de Demonstração (AWS Calculator):** [COLE O SEU LINK DO YOUTUBE AQUI]
