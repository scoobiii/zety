# zety


🧑‍💻 Zety 🐍
Zety is a modular, multi-platform compiler aiming to support multiple languages and promote green computing!


Creators 👨‍👩‍👧‍👦
Zeh Sobrinho (Vision)
TutorC Team (Inspiration)
BARD Assistant (Design)
Anthropic (AI Support)


🎯 Objectives
Modular architecture
Interactive development workflow
Support for OOP, functional and mixed paradigms
Performance metrics and optimization guidance
Compatibility with energy efficiency standards
Open source collaboration


🗺 Roadmap
v1.0 with C compiler (Q1 2023)
Python compiler integration (Q2 2023)
Internationalization (Q3 2023)
JavaScript, Rust support (2024)


⚙️ Team
Product Manager: Zeh Sobrinho
Lead Architect: TutorC
Developers: 5 contributors
Designer: Poe
Testing: Community


📅 Milestones
Jan: Basic compiler structure
Feb: Testing framework
Mar: C compilation
Apr: v1.0 release!
:octocat: Contributing
Get involved on GitHub or join our community forums!

# Para adicionar o C, pra começar o rolê, (assembler hein...?) 

Incluir representações para os mesmos tipos de dados encontrados nos outros idiomas, como inteiros, strings, booleans, etc. Mas, devido à sua natureza de programação, podemos incluir elementos específicos do C, como tipos de dados (int, float, char, etc.) e operadores (+, -, *, /, etc.).

**Exemplo:**

data["c"] = {
    "inteiro": "int",
    "string": "char*",
    "verdadeiro": "true",
    "falso": "false",
    "soma": "+",
    "multiplicação": "*",
}

**2. Adicionando a Língua de Sinais:**

A inclusão da Língua de Sinais requer uma abordagem diferente, pois a representação textual direta nem sempre é precisa ou suficiente. Podemos considerar duas opções:

Representação visual: Utilize imagens ou vídeos que representem os sinais da Língua de Sinais para cada palavra-chave. Isso requer um conjunto de dados de imagens/vídeos anotados para cada idioma.
Representação simbólica: Utilize um sistema de codificação simbólica, como o SignWriting, para representar os sinais. Isso requer codificar as palavras-chave na Língua de Sinais usando o sistema simbólico escolhido.

**3. Considerações multidimensionais:**

Para tornar o modelo multidimensional, além da representação textual, podemos incorporar a dimensão visual para a Língua de Sinais (opção 1) ou uma dimensão simbólica para a representação simbólica (opção 2). Isso permitirá ao modelo aprender as relações entre as palavras-chave em diferentes dimensões e idiomas.

**4. Exemplo multidimensional:**

Imagine que sua rede neural tem uma entrada para o texto e outra para a representação visual/simbólica da Língua de Sinais. Ao treinar o modelo com esta arquitetura, ele poderá aprender a associar as palavras-chave em todos os idiomas, considerando tanto a sua forma textual quanto a sua representação visual/simbólica.

Lembre-se que construir um conjunto de dados multidimensional robusto com a Língua de Sinais pode ser um desafio devido à complexidade da sua representação. Porém, ao explorar abordagens como as mencionadas acima, você pode capacitar o modelo a traduzir de forma mais completa e precisa entre um maior número de idiomas.

É importante ressaltar que esta é apenas uma abordagem possível, e outras opções de representação e arquitetura multidimensional podem ser exploradas dependendo das suas necessidades e recursos.

Opção 2: Criar um sub-dicionário para cada linguagem dentro de cada idioma existente:

Adicione um sub-dicionário para C dentro de cada idioma existente:
Python
data["brasiles"].update({
    "c": {
        "int": "int",
        "string": "char*",
        "true": "1",
        "false": "0",
    },
})
data["ingles"].update({
    "c": {
        "int": "int",
        "string": "char*",
        "true": "1",
        "false": "0",
    },
})
# ... e assim para tupi-guarani e grego

2. Adicione um sub-dicionário para a linguagem de sinais dentro de cada idioma existente:

data["brasiles"].update({
    "linguagem-de-sinais": {
        "inteiro": "sinal de inteiro",
        "string": "sinal de sequência",
        "verdadeiro": "sinal de verdadeiro",
        "falso": "sinal de falso",
    },
})
data["ingles"].update({
    "linguagem-de-sinais": {
        "inteiro": "sinal de inteiro",
        "string": "sinal de sequência",
        "verdadeiro": "sinal de verdadeiro",
        "falso": "sinal de falso",
    },
})

# ... e assim para tupi-guarani e grego e porra toda


A melhor opção para você depende de como você deseja que o modelo use as diferentes linguagens. A Opção 1 trata C e a linguagem de sinais como linguagens independentes, enquanto a Opção 2 as trata como subconjuntos de cada idioma existente. 

Lembre-se de que você precisará obter as traduções corretas para as palavras-chave em C e na linguagem de sinais para adicionar ao seu conjunto de dados. 

Além disso, considere a complexidade da linguagem de sinais.  Pode ser necessário representar as traduções usando descrições detalhadas dos sinais ou um formato de vídeo para o modelo entender corretamente.

Crie um dicionário com as quatro línguas existentes como chaves de primeiro nível.
Dentro de cada chave de língua, crie um dicionário com as palavras-chave em português como chaves de segundo nível.
Dentro de cada chave de palavra-chave, adicione as equivalentes em cada língua como valores. Exemplo:
Python
data = {
    "brasiles": {
        "inteiro": "inteiro",
        "string": "string",
        # ...
    },
    "ingles": {
        "inteiro": "integer",
        "string": "string",
        # ...
    },
    "tupi-guarani": {
        "inteiro": "tupỹ",
        "string": "ñe'ẽ",
        # ...
    },
    "grego": {
        "αριθμός": "αριθμός",
        "σειρά χαρακτήρων": "σειρά χαρακτήρων",
        # ...
    },
    "c": {
        "inteiro": "int",
        "string": "char*",
        # ...
    },
    "linguagem-de-sinais": {
        "inteiro": [sinal de número],
        "string": [sinal de letra],
        # ...
    },
}


 **Criar um conjunto de dados separado para C e linguagem de sinais:**

Opção 3: Mantenha o conjunto de dados existente com as quatro línguas originais.

**Crie dois novos conjuntos de dados:**
Um conjunto de dados para C, contendo pares de palavras-chave em português e C.
Um conjunto de dados para a linguagem de sinais, contendo pares de palavras-chave em português e a representação correspondente em sinais (descrição, imagem, etc.).
Qual opção escolher depende de suas necessidades e do tipo de modelo que você pretende treinar. A opção 1 é mais simples, mas pode não ser tão eficiente para modelos complexos. A opção 2 é mais flexível, mas pode ser mais complexa de implementar. 

**A opção 3** é mais modular, mas requer a criação e manutenção de conjuntos de dados separados.

Tenha em mente que, ao adicionar C e a linguagem de sinais, você precisará de um conjunto de dados suficientemente grande para cada língua para que o modelo aprenda as relações entre as palavras-chave com precisão.

**The project is progressing well thanks to community support. Let me know if you have any other questions!**



