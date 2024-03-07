# Maturador de chips

![license](https://img.shields.io/badge/License-MIT-green.svg?logo=internetarchive&logoColor=white&labelColor=464646&style=for-the-badge)
![stars](https://img.shields.io/github/stars/jonasCaetanoSz/maturador-de-chips?style=for-the-badge)
![version](https://img.shields.io/github/v/release/jonasCaetanoSz/maturador-de-chips?style=for-the-badge)

**maturador-de-chips** é um pequeno programa para "esquentar" contas do WhatsApp e dessa forma, evitar banimento da rede social.

## Instalação

Se você é usuário Windows, pode [fazer download do instalador x64](https://github.com/JonasCaetanoSz/maturador-de-chips/releases/latest) ou siga as instruções abaixo para executar o código-fonte da versão de codigo aberto:

- Clone o repositório

```shell
git clone https://github.com/JonasCaetanoSz/maturador-de-chips.git
```

Crie um ambiente virtual e ative-o

```shell
python -m venv .venv
```

```shell
& .venv/scripts/activate.ps1
```

- Instale as dependências

```shell
pip install -r requirements.txt
```

- Inicie o programa

```shell
python main.py
```

## Funcionalidades

- Definir intervalo mínimo e máximo entre mensagens
- Definir troca de conta após X mensagens
- Definir máximo de mensagens
- Parar em caso de bloqueio
- Mensagens com ChatGpt
  - Sem limite de instâncias
  - Escolher nome instância
  - Remover instância

### Versões Alternativas

- [APIBrasil/maturador-de-chips](https://github.com/APIBrasil/maturador-de-chips)
- [AdrianoF0nseca/maturador-de-chips](https://github.com/AdrianoF0nseca/maturador-de-chips)

### Como gerar meu próprio executável?

Este é o comando pyinstaller para gerar o executável do maturador:

```shell
pyinstaller  --noconfirm --onedir --windowed --icon "$(pwd)/pages/assets/medias/icon.ico" --add-data "$(pwd)/pages;pages/" --add-data "$(pwd)/scripts;scripts/" --add-data "$(pwd)/LICENSE;." --add-data "$(pwd)/gpt.py;." --add-data "$(pwd)/README.MD;." --add-data "$(pwd)/user-agent;." --add-data "$(pwd)/requirements.txt;."  "$(pwd)/main.py"
```

### Encontrar o cookie de sessão para API não oficial?

- 1 ° Acesse o site [Bing](https://bing.com) e faça login usando uma conta Microsoft. Após login abra o *developer tools* presionando as teclas **CTRL + SHIFT + I** ou siga os passos na foto abaixo para realizar esta ação:

![step1](https://i.ibb.co/TTSSXm1/passo-1.png)

- 2 ° Busque no submenu que fica ao lado de *network*, a opção **Application** e clique sobre ela:

![step2](https://i.ibb.co/Q8JZpPZ/passo-2.png)

- 3 ° Por último, encontre o cookie nomeado de **_U** e copie seu valor:

![step3](https://i.ibb.co/rdBFNt4/passo-3.png)

## Licença

Distribuído sobre Licença [MIT](https://choosealicense.com/licenses/mit/)
