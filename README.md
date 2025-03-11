# Detector de Plágio com Gemini 🤖

Este projeto é um detector de plágio desenvolvido em **Python** com integração à API do **Google Gemini**. Ele compara textos de entrada com um banco de textos pré-definidos para identificar possíveis plágios, utilizando embeddings e similaridade de cosseno.

---

## Índice 📚

- [Visão Geral](#visão-geral-)
- [Objetivo](#objetivo-)
- [Tecnologias Utilizadas](#tecnologias-utilizadas-)
- [Como Executar](#como-executar-)
- [Funcionalidades](#funcionalidades-)
- [Exemplo de Uso](#exemplo-de-uso-)
- [Contribuição](#contribuição-)
- [Licença](#licença-)

---

## Visão Geral 🌟

O **Detector de Plágio com Gemini** é uma ferramenta que utiliza a API do Google Gemini para gerar embeddings de textos e calcular a similaridade entre eles. Ele foi desenvolvido durante a imersão de IA da Alura e tem como objetivo identificar possíveis plágios em textos de entrada, comparando-os com um banco de dados de textos pré-definidos.

---

## Objetivo 🎯

- Desenvolver um detector de plágio utilizando a API do Google Gemini.
- Comparar textos de entrada com um banco de textos pré-definidos.
- Identificar possíveis plágios com base na similaridade de cosseno.

---

## Tecnologias Utilizadas 🛠️

- **Python**: Linguagem de programação principal.
- **Google Gemini API**: Para geração de embeddings de textos.
- **scikit-learn**: Para cálculo de similaridade de cosseno.
- **Google Colab**: Ambiente de desenvolvimento e execução.

---

## Como Executar 🚀

1. **Importações e Configuração de API**:
   ```python
   import google.generativeai as genai
   import numpy as np
   from sklearn.metrics.pairwise import cosine_similarity
   from google.colab import userdata

   API_KEY = userdata.get('SECRET_KEY')
   genai.configure(api_key=API_KEY)
   ```

2. **Banco de Textos**:
   ```python
   # Frases para verificar plágio
   textos_banco_de_dados = [
     "A vastidão do cosmos, com suas miríades de estrelas, sempre fascinou a humanidade...",
     "Na vastidão do espaço, a Via Láctea, nossa galáxia, se destaca como um espiral de poeira...",
     "A busca por vida extraterrestre intriga cientistas e entusiastas...",
     "As estrelas, em sua dança cósmica, criam padrões complexos e fascinantes...",
     "A exploração espacial, com suas missões tripuladas e sondas robóticas, tem revelado maravilhas...",
     "Olhando para o céu noturno, somos lembrados da imensidão do universo e da nossa própria pequenez..."
   ]

   # Frase de entrada que acusarão plágio
   textos_entrada = [
     "O cosmos fascina a humanidade desde os primórdios.",
     "Nossa galáxia, a Via Láctea, é um espiral de poeira e gás.",
     "Cientistas buscam vida extraterrestre no universo.",
     "As estrelas formam padrões complexos no céu noturno.",
     "A exploração espacial expande nosso conhecimento do universo.",
     "O céu noturno nos lembra da imensidão do cosmos."
   ]
   ```

---

## Funcionalidades ✨

- **Geração de Embeddings**: Utiliza a API do Google Gemini para gerar embeddings de textos.
- **Cálculo de Similaridade**: Compara textos de entrada com um banco de textos pré-definidos usando similaridade de cosseno.
- **Detecção de Plágio**: Identifica possíveis plágios com base em um limite de similaridade.

---

## Exemplo de Uso 📝

1. Execute o código no Google Colab.
2. Insira um texto para verificar plágio:
   ```
   Digite um texto para verificar plágio: Cientistas buscam vida extraterrestre no universo.
   ```
3. O sistema retornará:
   ```
   Possível plágio detectado:
   - A busca por vida extraterrestre intriga cientistas e entusiastas. A possibilidade de encontrarmos outras formas de vida no universo levanta questões profundas sobre nossa própria existência e lugar no cosmos.
   ```
   
---

## Licença 📜

Este projeto está licenciado sob a **MIT License** - consulte o arquivo [LICENSE](LICENSE) para mais detalhes.

---

Feito com ❤️ por [João Batista](https://github.com/joaobatista235).
