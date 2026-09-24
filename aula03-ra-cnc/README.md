# Manual Interativo do Torno CNC (Realidade Aumentada)

Grupo: Rafael Paiutto e Victor Hugo Dos Santos.

Aplicação WebAR (A-Frame + MindAR) que reconhece a imagem do torno CNC via câmera
e exibe 5 pontos interativos (hotspots) com informações sobre a máquina.

## Estrutura (agora na raiz do repositório)

```
Manual-TornoCNC/
├── index.html
├── css/
│   └── style.css
├── js/
│   └── app.js
├── assets/
│   ├── images/torno.png
│   └── targets/
│       ├── torno.png
│       └── targets.mind
└── README.md
```

`index.html` foi movido para a **raiz** do repositório (antes estava dentro de
`aula03-ra-cnc/`). Isso é essencial para o GitHub Pages: ele só serve
automaticamente o arquivo que estiver em `index.html` na raiz da branch
publicada. Com o arquivo dentro de uma subpasta, a URL principal do site
(`https://v1cta0.github.io/Manual-TornoCNC/`) não encontrava nada.

## Como publicar

1. Substitua **todo o conteúdo** do repositório `Manual-TornoCNC` (na branch
   `main`) pelos arquivos desta pasta — mantendo essa estrutura na raiz.
2. Faça commit e push.
3. Em Settings → Pages, confirme que a publicação é a partir da branch `main`,
   pasta `/ (root)`.
4. Acesse pelo celular:
   ```
   https://v1cta0.github.io/Manual-TornoCNC/
   ```
   (precisa ser HTTPS para o navegador liberar a câmera).
5. Aponte a câmera para a imagem do torno (a mesma usada para gerar
   `targets.mind`). O badge deve mudar para "● RA ATIVA" e os 5 hotspots
   aparecem sobre a máquina.

## Se ainda não reconhecer o alvo

- Confira no console do navegador (F12 no desktop, ou `chrome://inspect` a
  partir de um PC conectado ao celular) se há erro 404 carregando
  `assets/targets/targets.mind` — indicaria caminho errado.
- Teste com boa iluminação e a câmera relativamente próxima e de frente para
  a imagem impressa/tela usada como alvo.
- Confirme que `targets.mind` foi gerado a partir da **mesma imagem**
  (`torno.png`) que está sendo apontada pela câmera.
