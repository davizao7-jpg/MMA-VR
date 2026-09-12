# MMA VR - Octógono

Jogo de luta em WebXR para Meta Quest 2. Um único arquivo HTML, sem dependências de build.

## Como publicar no GitHub Pages

1. Coloque o arquivo **`index.html`** na raiz do repositório (não dentro de nenhuma pasta), substituindo qualquer outro HTML que já esteja lá.
2. No repositório no GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, branch `main` (ou `master`), pasta `/ (root)`. Salve.
3. Aguarde 1-2 minutos. O site fica disponível em:
   `https://davizao7-jpg.github.io/MMA-VR/`
4. Abra esse link no **Navegador do Meta Quest 2** (Oculus Browser) e toque em "Entrar no Octógono (VR)".

GitHub Pages já serve tudo em HTTPS, que é obrigatório para WebXR funcionar — não precisa configurar nada extra de certificado.

## Ajustando ao tamanho da sua sala

Dentro do `index.html`, na função `buildArena()`, existe:

```js
const R = 3.2; // raio do octógono em metros
```

Diminua esse valor se seu limite de área (guardian) do Quest 2 for menor que ~6,5m x 6,5m.

## Arquivos

- `index.html` — o jogo completo (HTML + CSS + JS embutidos, carrega Three.js via CDN).
