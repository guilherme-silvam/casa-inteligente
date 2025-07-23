# 💡 Casa Inteligente

Sistema de automação residencial com interface web, backend em Node.js e controle físico via ESP32. O usuário pode acionar dispositivos remotamente como lâmpadas, ventiladores ou qualquer outro equipamento conectado.

---

## 📁 Estrutura do Projeto

casa-inteligente/
├── backend/
│ └── server.js # Servidor Express que recebe comandos e comunica com o ESP32
├── frontend/
│ ├── index.html # Interface web com botões de controle
│ ├── style.css # Estilização da página
│ └── script.js # Lógica de envio de comandos
└── dispositivos/
└── esp32/
└── esp32-control.ino # Código para ser carregado no ESP32

---

## 🚀 Tecnologias Utilizadas

- HTML, CSS e JavaScript (Frontend)
- Node.js + Express (Backend)
- ESP32 (Arduino Framework)

---

## 🧰 Pré-requisitos

- Node.js instalado
- Arduino IDE instalada
- Placa ESP32 conectada via USB
- Navegador moderno (Chrome, Firefox, etc.)
- Todas as pastas do projeto baixadas/clonadas

---

## ▶️ Passo a Passo

### 1. Subir o código para o ESP32

1. Conecte o ESP32 no seu computador.
2. Abra o arquivo `dispositivos/esp32/esp32-control.ino` na Arduino IDE.
3. Faça o upload para a placa.
4. No código `.ino`, configure sua rede Wi-Fi (SSID e senha).

---

### 2. Executar o Backend (Node.js)

cd backend
npm install         # Instala as dependências
node server.js      # Inicia o servidor
O backend estará rodando por padrão em http://localhost:3000.

3. Abrir o Frontend
Abra o arquivo frontend/index.html no seu navegador.
Você verá a interface com os botões de controle.

⚠️ Observações Importantes
O ESP32 e o servidor Node.js devem estar conectados à mesma rede Wi-Fi.

O frontend se comunica com o backend via fetch.

O backend envia comandos HTTP para o ESP32 com base na ação feita no botão.

🧠 Personalização
Adicione mais botões no index.html e configure o envio no script.js.

No ESP32, você pode controlar relés, LEDs ou motores, conforme os pinos programados.

---

## 📝 `README.md` — Projeto `casa-inteligente-tv`


# 📺 Casa Inteligente - Controle da TV Samsung

Projeto que permite controlar uma Smart TV Samsung remotamente usando uma interface web e Python. Ideal para integrar automação residencial com dispositivos já existentes na casa.

---


## 📁 Estrutura do Projeto

casa-inteligente-tv/
├── app.py # Servidor Flask que lida com os comandos enviados via navegador
├── samsung_config.json # Configurações específicas da sua TV Samsung (IP, token, ID, etc.)
├── requirements.txt # Dependências Python
└── templates/
└── index.html # Interface web com os botões de controle

---

## 🚀 Tecnologias Utilizadas

- Python 3
- Flask (servidor web)
- WebSocket + HTTP
- HTML/CSS (interface web)

---

## 🧰 Pré-requisitos

- Python 3 instalado
- A TV Samsung deve estar conectada na **mesma rede** que o computador
- Projeto clonado/baixado localmente
- TV compatível com controle via rede (Smart TV)

---

## ▶️ Passo a Passo

### 1. Instalar as dependências

Abra o terminal na pasta do projeto e execute:


pip install -r requirements.txt
2. Configurar a TV
Edite o arquivo samsung_config.json com os dados corretos da sua TV:

json
{
  "tv_ip": "192.168.0.XXX",
  "token": "SEU_TOKEN_AQUI",
  "device_id": "SeuComputador"
}
⚠️ O IP da TV pode ser encontrado nas configurações de rede dela.

3. Executar o servidor
No terminal:


python app.py
O servidor Flask estará acessível em: http://localhost:5000

4. Acessar a Interface
Abra seu navegador e digite:

arduino
Copiar
Editar
http://localhost:5000
Use os botões para enviar comandos diretamente para a TV.

🔧 Comandos disponíveis
Power On/Off (dependendo da TV)

Volume +

Volume -

Mudo

Navegação (setas, ok, voltar)

Menu

🧠 Personalização
Você pode adicionar mais botões e comandos editando:

templates/index.html (interface)

app.py (ações que os botões executam)

Com isso, é possível integrar com Alexa, Google Assistant, Node-RED, etc.

