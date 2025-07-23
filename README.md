📁 Projeto: casa-inteligente
Cole este conteúdo no arquivo README.md dentro da pasta casa-inteligente:


# 💡 Projeto Casa Inteligente

Este projeto simula um sistema de automação residencial com controle via interface web, backend em Node.js e integração com um ESP32.

---

## 📁 Estrutura

casa-inteligente/
├── frontend/
│ ├── index.html # Página principal com botões de controle
│ ├── style.css # Estilo da página
│ └── script.js # Lógica para interação com o backend
├── backend/
│ └── server.js # Servidor Node.js que recebe os comandos e interage com o ESP32
├── dispositivos/
│ └── esp32/
│ └── esp32-control.ino # Código Arduino para o ESP32


---

## 🚀 Tecnologias Utilizadas

- HTML, CSS e JavaScript (Frontend)
- Node.js e Express (Backend)
- ESP32 com Arduino (Microcontrolador)

---

## ▶️ Como Executar

### 1. Backend (Node.js)
- Certifique-se de ter o Node.js instalado.
- Navegue até a pasta `backend`:
```bash
cd backend
npm install
node server.js
2. Frontend
Basta abrir o arquivo frontend/index.html no navegador.

3. ESP32
Abra o arquivo esp32-control.ino na IDE do Arduino.

Conecte seu ESP32 e faça o upload do código.

⚠️ Observações
O ESP32 precisa estar na mesma rede que o servidor Node.js para funcionar corretamente.

Você pode adaptar os comandos para controlar relés, LEDs, etc.


---

## 📁 Projeto: **casa-inteligente-tv**  
**Cole este conteúdo no arquivo `README.md` dentro da pasta `casa-inteligente-tv`:**


# 📺 Casa Inteligente - Controle da TV

Este projeto permite controlar uma TV Samsung remotamente via interface web, utilizando Python e o protocolo de controle remoto da própria TV.

---

## 📁 Estrutura

casa-inteligente-tv/
├── app.py # Servidor Flask responsável por lidar com comandos
├── templates/
│ └── index.html # Interface web com botões para controlar a TV
├── samsung_config.json # Arquivo de configuração da TV Samsung
└── requirements.txt # Dependências Python do projeto


---

## 🚀 Tecnologias Utilizadas

- Python 3
- Flask (para servidor web)
- WebSocket e HTTP (para comunicação com a TV Samsung)

---

## ▶️ Como Executar

### 1. Instale as dependências

Com Python 3 instalado, execute:
pip install -r requirements.txt

###2. Execute o servidor

python app.py

### 3. Acesse no navegador
Abra http://localhost:5000 para acessar a interface de controle.

⚙️ Configuração da TV
Certifique-se de que a TV Samsung esteja na mesma rede do computador.

Edite o arquivo samsung_config.json com o IP da sua TV e os dados de pareamento.









