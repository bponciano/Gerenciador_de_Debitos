📒 Gerenciador de Debitos – Sistema em Python com Interface Gráfica (Tkinter)
----------------------------------------------------------------------------------------------------------------------------------------------
O controle de fiados em pequenos comércios sempre foi feito no caderninho tradicional, mas agora isso pode ser feito de forma digital, organizada e automática.
Este projeto oferece uma solução simples, intuitiva e eficiente para registrar compras, pagamentos, consultar extratos, listar clientes e acompanhar o total devido — tudo com uma interface amigável construída em Tkinter.

🚀 Sobre o Projeto
----------------------------------------------------------------------------------------------------------------------------------------------
O gerenciador de debitos é um sistema desktop desenvolvido em Python, pensado para pequenos estabelecimentos, autônomos e qualquer pessoa que precise controlar fiados de maneira prática.

A aplicação permite:
- Registrar novos clientes
- Registrar compras e pagamentos
- Consultar extrato individual
- Exportar extrato completo em arquivo .txt
- Listar todos os clientes com seus saldos
- Calcular o saldo total devido
- Excluir clientes do registro
- Armazenar tudo automaticamente em dados.json
Mesmo sendo simples de usar, o sistema foi estruturado com cuidado para manter clareza, organização e escalabilidade.

🎨 Interface Intuitiva e Direta
----------------------------------------------------------------------------------------------------------------------------------------------

A interface foi construída com Tkinter e componentes visuais do ttk, incluindo:
- Campos padronizados para Nome, Data e Valor
- Botões separados por ação (compra, pagamento, consulta, etc.)
- DataPicker automático usando tkcalendar
- Janela dedicada para listar clientes com tabela estilizada
- Janelas de diálogo com mensagens claras de erro ou sucesso

Toda ação é confirmada com avisos amigáveis para o usuário, tornando o sistema fácil de usar até para quem não entende nada de programação.

🧠 Como Funciona a Lógica Interna
----------------------------------------------------------------------------------------------------------------------------------------------

A base do sistema utiliza:
✔ Dicionário de clientes
Cada cliente é armazenado usando o nome como chave:

```python
clientes[nome_chave] = {
    "nome_exibicao": nome_cliente,
    "saldo_devedor": 0.0,
    "transacoes": []}
```

✔ Sistema de transações
----------------------------------------------------------------------------------------------------------------------------------------------

Cada compra ou pagamento vira um registro com:
- tipo (compra ou pagamento)
- data
- valor

✔ Armazenamento automático (JSON)
----------------------------------------------------------------------------------------------------------------------------------------------
Tudo é salvo e carregado via:

```python
dados.json
```

Isso permite que o usuário feche o programa e retorne exatamente de onde parou.

📁 Estrutura do Projeto
----------------------------------------------------------------------------------------------------------------------------------------------
```python
📂 CadernoFiados
├── caderno_fiados.py     # Código principal
├── dados.json            # Banco de dados local (gerado automaticamente)
├── extrato_nome.txt      # Arquivos de extrato exportados
└── CadernoFiados.exe     # Executável (opcional)
```

🛠 Tecnologias Utilizadas
----------------------------------------------------------------------------------------------------------------------------------------------

- Python 3.10+
- Tkinter (Interface gráfica)
- tkcalendar (DateEntry)
- JSON (Armazenamento local)

📦 Como Executar o Código
----------------------------------------------------------------------------------------------------------------------------------------------

1. Requisitos
Para rodar o código, é necessário:
- Sistema Windows
- Python instalado (3.10 ou superior)
- Biblioteca tkcalendar instalada:

```python
pip install tkcalendar
```
2. Executar diretamente o script
Abra o terminal na pasta do projeto e rode:

```python
python caderno_fiados.py
```
💻 Versão .EXE (Pronto para Uso)
----------------------------------------------------------------------------------------------------------------------------------------------

O repositório também disponibiliza o arquivo .exe, permitindo que você use o programa sem precisar instalar Python ou pacotes.
Ideal para usuários finais que só querem utilizar o sistema.

🔓 Código Aberto
----------------------------------------------------------------------------------------------------------------------------------------------

O código-fonte está disponível integralmente para estudo, melhorias e personalizações.
Fique à vontade para abrir Issues, sugerir melhorias ou enviar PRs.

📝 Observação Importante
----------------------------------------------------------------------------------------------------------------------------------------------

- O código só funciona no Windows e exige a biblioteca tkcalendar instalada.
- Além disso, tanto o código completo quanto o arquivo .exe estão disponibilizados neste repositório.
