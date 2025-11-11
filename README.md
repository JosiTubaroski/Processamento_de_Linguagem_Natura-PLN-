
<div> 
<p><a href="https://github.com/JosiTubaroski/DataScience/blob/main/README.md">Inteligencia Artificial</a></p>
</div> 

# Processamento de Linguagem Natural (PLN)
(em inglês, NLP - Natural Language Processing)

É o <b>campo da inteligência artificial que ensina os computaodres a entender, interpretar e gerar linguagem humana</b> - tanto escrita quanto falada.

Em outras palavras:

 É o que permite que uma máquina <b>entenda o que você diz em palavras</b>, e não apenas comandos de código.

### 💬 Exemplo prático

Quando você digita:

 "Me lembre de pagar o boleto amanhã"

 O sistema precisa:

<b>1. Ler o texto</b> (entrada linguística)
<b>2. Entender o significado</b> ("lembrar de pagar algo", "amanhã")
<b>3. Executar uma ação coerente</b> (criar um lembrete para o dia seguinte)

Tudo isso é <b>processamento de linguagem natural.</p>

## ⚙️ As principais etapas do PLN

### 1. Tokenização

Dividir a frase em partes menores (palavras, expressões).

- "Eu gosto de café"→ [“Eu”, “gosto”, “de”, “café”] 

### 2. Análise semântica

Identicar a estrutura gramatical da frase.

- "Eu" = sujeito | "gosto" = verbo | "de café" = complemento

### 3. Análise semântica

Compreender o <b>significado</b> das palavras e suas relações.

- "gostar de café" significa uma preferência.

### 4. Análise de sentimento (opcional)

Descobrir a <b>emoção</b> por trás da fase.

- "O serviço foi horrível" → sentimento negativo.

### 5. Geração de linguagem natural (NLG)

Fazer o caminho inverso: a máquina <b>cria frases novas e coerentes.</b>

- "Você quer que eu te lembre de pagar o boleto amanhã?"

## 🧩 Onde o PLN é usado hoje

- <b>Chatbots e assistentes virtuais</b> (ChatGPT, Alexa, Siri, Google Assistant)
- <b>Tradução automática</b> (Google Tradutor, DeepL)
- <b>Correção e sugestão de texto</b> (Grammarly, autocorretores)
- <b>Análise de sentimentos</b> em redes sociais e atendimento ao cliente
- <b>Resumo automático</b> de textos longos
- <b>Pesquisa inteligente</b> (quando você faz perguntas em vez de palavras-chave)

## 💡 Em resumo

| Aspecto      | O que o PLN faz                                             |
| ------------ | ----------------------------------------------------------- |
| Entendimento | Faz a máquina compreender o que você escreve ou fala        |
| Geração      | Faz a máquina responder de forma natural e coerente         |
| Base         | Linguística + estatística + aprendizado de máquina          |
| Objetivo     | Aproximar a linguagem das pessoas da linguagem das máquinas |

#

# Mini Exemplo

Vamos usar a biblioteca <b>spaCy</b>, uma das mais modernas de Processamento de Linguagem Natural (PLN) em Phython.

### 🧠 Exemplo prático em Python (usando spaCy)

    # 1️⃣ Instalar a biblioteca e o modelo de linguagem
    # pip install spacy
    # python -m spacy download pt_core_news_sm

    import spacy

    # 2️⃣ Carregar o modelo de linguagem em português
    nlp = spacy.load("pt_core_news_sm")

    # 3️⃣ Processar uma frase
    texto = "O cientista analisou os dados com atenção."
    doc = nlp(texto)

    # 4️⃣ Exibir análise sintática
    print("=== Análise Sintática ===")
    for token in doc:
        print(f"{token.text:<12} -> {token.dep_:<15} ({token.head.text})")

    # 5️⃣ Exibir entidades semânticas reconhecidas
    print("\n=== Entidades Reconhecidas ===")
    for ent in doc.ents:
        print(f"{ent.text:<12} -> {ent.label_}")

    # 6️⃣ Vetor semântico da frase (representação numérica do sentido)
    print("\n=== Vetor Semântico ===")
    print(doc.vector[:10])  # mostra só os 10 primeiros valores

