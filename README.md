## Voices with Web Speech API :smiling_face_with_three_hearts:

Projeto simples que converte texto digitado em áudio diretamente no navegador, utilizando a **Web Speech API** (`SpeechSynthesis`).

> 🔎 A disponibilidade e a qualidade das vozes variam conforme o navegador e o sistema operacional.

---

### 🛠 Exemplos de ajustes no código

No código JavaScript (dentro do `index.html`), você pode personalizar o comportamento do leitor de texto.  
Alguns exemplos de ajustes:

- [x] **Volume da voz**  
  ```js
  toSpeak.volume = 0.9; // volume máximo entre 0.0 e 1.0
  ```

- [x] **Velocidade da fala (rate)**  
  ```js
  toSpeak.rate = 1; // velocidade padrão (0.1 até 10)
  // Exemplo: leitura mais lenta
  // toSpeak.rate = 0.8;
  // Exemplo: leitura mais rápida
  // toSpeak.rate = 1.2;
  ```

- [x] **Tom da voz (pitch)**  
  ```js
  toSpeak.pitch = 1; // tom padrão (0 a 2)
  // Exemplo: voz mais grave
  // toSpeak.pitch = 0.8;
  // Exemplo: voz mais aguda
  // toSpeak.pitch = 1.2;
  ```

- [x] **Seleção de voz por idioma/nome**  
  ```js
  const selectedVoice = listaVoz.selectedOptions[0];
  const selectedVoiceName = selectedVoice.getAttribute('data-name');

  const voiceEncontrada = voices.find((voice) => voice.name === selectedVoiceName);
  if (voiceEncontrada) {
    toSpeak.voice = voiceEncontrada;
  }
  ```

- [x] **Cancelar a fala atual antes de iniciar outra**  
  ```js
  if (synth.speaking) {
    synth.cancel(); // interrompe a fala anterior
  }
  synth.speak(toSpeak);
  ```

---

### 💻 Captura de tela

<img width="1196" height="880" alt="image" src="https://github.com/user-attachments/assets/948a92b4-a5b5-4a92-a801-03f030337911" />


---

### 🤝 Conecte-se comigo

[:thumbsup: Me siga no GitHub](https://github.com/oklebernascimento/)

