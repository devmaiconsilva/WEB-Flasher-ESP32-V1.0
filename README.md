# WEB-Flasher ESP32 V1.0 🚀

Uma ferramenta web moderna, elegante e de alto desempenho para gravação (flash) de firmwares em microcontroladores da família ESP32 diretamente através do navegador. O projeto utiliza a **Web Serial API** e a biblioteca **esptool-js** para realizar gravações diretas via porta USB (COM) sem necessidade de instalações adicionais no computador do usuário.

---

## ✨ Recursos Principais

### 1. 🎨 Layout Premium Dark Mode
*   Visual escuro futurista com elementos translúcidos (Glassmorphism) e tipografia moderna (**Outfit** para a interface e **JetBrains Mono** para os logs).
*   **LED de Status Inteligente:** Indicador visual que sinaliza o estado atual da gravação:
    *   🔴 **Vermelho estático:** Dispositivo desconectado.
    *   🟢 **Verde pulsante:** Dispositivo conectado e pronto.
    *   🟡 **Amarelo pulsante rápido:** Processo de gravação (flashing) em andamento.

### 🔌 2. Seletor Dinâmico de Biblioteca (Online / Offline)
*   **Offline-first:** Por padrão, a aplicação carrega o bundle local `esptool-bundle.js` para funcionar em locais sem conectividade.
*   **Online Fallback:** Permite alternar dinamicamente para carregar a biblioteca diretamente do CDN unpkg (`https://unpkg.com/esptool-js`), servindo como redundância caso o arquivo local falhe ou precise ser depurado.

### 📁 3. Gerenciador Dinâmico de Múltiplos Arquivos
*   **Gravação Combinada:** Permite adicionar múltiplas linhas de arquivos binários e definir offsets específicos para cada um (ex: bootloader em `0x1000`, tabela de partição em `0x8000` e firmware principal em `0x10000`).
*   **Offsets Customizados:** Além dos endereços comuns predefinidos, conta com campo de entrada para offsets em hexadecimal personalizados.
*   **Detecção de Metadados:** Exibe dinamicamente o nome, tamanho formatado (Bytes, KB ou MB) e a última modificação de cada arquivo selecionado.
*   **Progresso Unificado:** A barra de progresso e o log calculam a taxa geral de transferência com base na soma do tamanho total de todos os arquivos ativos.

### 🖥️ 4. Console de Logs Avançado
*   Logs detalhados de comunicação serial direto na tela com scroll automático.
*   **Ações Rápidas:**
    *   *Limpar Logs:* Limpa a tela de terminal para uma nova depuração.
    *   *Exportar Logs:* Gera e baixa um arquivo `.txt` contendo todo o histórico do console com timestamp atual no nome do arquivo.

---

## 🛠️ Requisitos de Execução

1.  **Navegador Compatível:** Chrome, Edge ou Opera (navegadores com suporte à **Web Serial API**).
2.  **Ambiente Seguro (HTTPS ou Localhost):** Por restrições de segurança do navegador, a API só funciona sob o protocolo seguro `https:` ou em servidores de desenvolvimento local (`http://localhost` ou `http://127.0.0.1`).

---

## 🚀 Como Executar Localmente

### Opção A: Servidor Python (Fácil)
Se você tiver o Python instalado, abra o terminal na pasta do projeto e execute:
```bash
python -m http.server 8000
```
Depois, acesse no navegador: [http://localhost:8000](http://localhost:8000)

### Opção B: Extensão VS Code (Live Server)
1. Instale a extensão **Live Server** no VS Code.
2. Abra a pasta do projeto no VS Code.
3. Clique no botão **"Go Live"** na barra de status inferior para iniciar o servidor automaticamente.

---

## 🛠️ Tecnologias Utilizadas
*   HTML5 & Javascript (ES6 Modules)
*   Vanilla CSS (Modern Custom Properties)
*   [esptool-js](https://github.com/espressif/esptool-js) (Biblioteca Oficial da Espressif)
*   Web Serial API

---

## 👤 Desenvolvedor
*   **Maicon Silva**
*   **GitHub:** [@devmaiconsilva](https://github.com/devmaiconsilva)
*   **E-mail:** [dev.maiconsilva@gmail.com](mailto:dev.maiconsilva@gmail.com)
