# Polyglot Master

Aplicação web de prática de idiomas criada para estudar italiano, mandarim e inglês através de exercícios curtos e interativos.

## Funcionalidades

- Pares, quiz, construção de palavras, ordenação de frases, escrita e preenchimento de lacunas.
- Ditado, prática de pronúncia com reconhecimento de voz, flashcards e escrita de caracteres chineses.
- Vocabulário organizado por temas, três níveis de dificuldade, pontuação e vidas.
- Revisão de respostas falhadas através de uma folha Google Sheets ligada a um Google Apps Script.

## Utilização

A aplicação está toda em `index.html` e não precisa de instalação nem de um processo de compilação. Publica o repositório com GitHub Pages ou abre o ficheiro num servidor web local.

Para iniciar um servidor local com Python:

```bash
python -m http.server 8000
```

Depois visita `http://localhost:8000`. A prática de voz depende das APIs disponíveis no navegador e pode exigir uma ligação segura (HTTPS).

## Progresso e dados

O nome do jogador, a pontuação, as vidas e o modo de teste ficam guardados no armazenamento local do navegador. O progresso não é sincronizado entre dispositivos; usar o mesmo nome noutro navegador cria um perfil separado.

Quando a integração Google Sheets está activa, a aplicação envia para o Apps Script o nome do jogador, o idioma, a palavra, a tradução e o motivo do erro. Revê as permissões e o URL da implementação antes de partilhares a aplicação com outras pessoas.

## Vocabulário

Os conjuntos de palavras e frases estão no objeto `DB`, dentro de `index.html`. Cada entrada pode incluir o termo no idioma de estudo, a pronúncia (opcional) e a tradução em português.

## Tecnologias

HTML, CSS e JavaScript sem dependências de compilação. A aplicação usa APIs do navegador para armazenamento local, síntese de voz, reconhecimento de voz, áudio e animações.
