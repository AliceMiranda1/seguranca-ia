# 🛡️Dynamic BioSecurity

Pesquisa aplicada sobre detecção de anomalias com redes neurais, com o objetivo de usar biometria comportamental (dinâmica de digitação) como sinal complementar de autenticação.

> **Status:** em pesquisa. O pipeline de detecção foi validado com um dataset público de demonstração. A aplicação em dados reais de digitação ainda não foi validada.
> **Aviso de confidencialidade:** este projeto foi desenvolvido em contexto profissional. Este repositório apresenta apenas a proposta e o estado da pesquisa. Não contém código-fonte, modelos treinados, dados ou resultados não validados.

## Problema

Senhas e tokens estáticos podem ser roubados ou usados por quem assume uma sessão já aberta. A proposta é observar, de forma contínua, padrões de interação do usuário e usar esse sinal para decidir se a sessão deve seguir normalmente ou pedir uma verificação adicional.

## Abordagem

- **Biometria comportamental:** características temporais de digitação, como o tempo que cada tecla fica pressionada e o intervalo entre teclas.
- **Detecção de anomalias:** um modelo aprende o padrão de referência de um usuário e mede o desvio do comportamento atual.
- **Decisão por risco:** o desvio é combinado com o contexto de acesso para escolher entre liberar, pedir verificação adicional ou bloquear.

## Estado atual

- **Validado:** pipeline de detecção de anomalias com Autoencoder (PyTorch), normalização e definição de limiar, testado em um dataset público de demonstração.
- **Em andamento:** adaptação do pipeline para dados de digitação.
- **Ainda não implementado:** coleta de dados reais de digitação, avaliação com métricas de detecção em dados de usuários e integração com um sistema de autenticação.

## Tecnologias

Python, PyTorch, Scikit-learn, Pandas, NumPy.

## Próximos passos

- Coletar e tratar dados de digitação de forma controlada.
- Avaliar o modelo com métricas de detecção (precisão, recall e curva ROC-AUC).
- Calibrar o limiar de decisão para equilibrar falsos alarmes e falsos negativos.

## 👩‍💻 Autora

**Alice Miranda** — *Estudante de Ciência da Computação na PUC Minas*

* 🌐 [LinkedIn](https://linkedin.com/in/alicemirandar) | 🐙 [GitHub](https://github.com/AliceMiranda1)
