# 🧠 Roonie - Assistente Pessoal por Voz em Python

**Roonie** é um assistente pessoal ativado por voz, desenvolvido em Python, com suporte para comandos em português. Ele reconhece a palavra de ativação ("acorde") e executa ações como abrir aplicativos, pesquisar na internet, registrar anotações, informar hora e data, e muito mais. Roonie também aprende com o tempo, registrando logs das ações realizadas para melhorar sua resposta aos comandos.

## 📌 Funcionalidades

- 🗣️ **Ativação por palavra-chave**: O assistente escuta o ambiente e responde quando ouve "acorde".
- 🔍 **Pesquisa na internet**: Pergunte algo e ele abre o navegador com os resultados do Google.
- 🕹️ **Abertura de jogos e aplicativos**: Detecta atalhos (.exe, .lnk, .url) na Área de Trabalho e abre pelo nome.
- 🧠 **Memória de hábitos**: Registra logs de ações para entender sua rotina e facilitar comandos futuros.
- 🗓️ **Anotações por voz**: Você pode ditar anotações e depois pedir para ele ler tudo.
- ⏰ **Informação de data e hora atual**.
- 📁 **Gerenciamento de jogos**: Utiliza um arquivo `games.json` com nomes e caminhos de jogos, incluindo links Steam e atalhos.
- ⟳ **Modo sempre acordado**: Após a primeira ativação, ele permanece ouvindo comandos sem precisar repetir a palavra-chave.

## 🛠️ Requisitos

- Python 3.7+
- `pyttsx3`
- `speechrecognition`
- `pyaudio` (ou `pywin32`, conforme o sistema)
- Navegador padrão configurado no sistema

### Instale as dependências:

```bash
pip install pyttsx3 SpeechRecognition
```

> Se estiver no Windows e tiver problemas com microfone:
```bash
pip install pyaudio
```

## 🗂️ Estrutura de Arquivos

```
roonie/
├── main.py                   # Código principal do assistente
├── tools/                    # Módulos auxiliares (abrir apps, notas, etc.)
│   ├── apps.py
│   ├── browser.py
│   ├── notes.py
│   ├── time_utils.py
│   └── wakeword.py
├── memory/
│   ├── games.json            # Lista de jogos com nomes e caminhos
│   └── log.json              # Registro de todas as ações realizadas
```

## 📋 Exemplo de `games.json`

```json
{
    "valorant": "D:\\Riot Games\\Riot Client\\RiotClientServices.exe",
    "marvel rivals": "steam://rungameid/2767030",
}
```

## 🚀 Como usar

1. Rode o `main.py`
2. Aguarde a frase: **"Roonie está pronto. Diga 'Acorde' para ativar."**
3. Diga **"acorde"** e depois o comando desejado, como:
   - "abrir valorant"
   - "pesquisar jogos novos"
   - "anotar comprar pão"
   - "ler anotações"
   - "que horas são?"
   - "qual a data de hoje?"
   - "encerrar"

## 🧠 Futuras melhorias

- Integração com APIs externas (clima, notícias, música).
- Respostas faladas mais naturais com vozes avançadas (TTS neural).
- Interface gráfica.
- Execução autônoma de tarefas rotineiras.

---

Desenvolvido com ❤️ por Thomaz
