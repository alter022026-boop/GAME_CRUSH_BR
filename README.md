# Crush BR — publicar como site/PWA no GitHub Pages

## Arquivos
- `index.html` — o jogo (já com manifest e service worker)
- `manifest.webmanifest` — dados do app instalável
- `sw.js` — funcionamento offline e cache
- `icons/` — ícones 180, 192, 512 e maskable

## Publicar (repositório alter022026-boop/GAME_CRUSH_BR)
1. Copie todo o conteúdo desta pasta para a raiz do repositório (mantenha a pasta `icons`).
2. Faça commit e push na branch principal.
3. No GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch**, escolha `main` e a pasta `/ (root)`, e salve.
4. Em 1 a 2 minutos o jogo abre em `https://alter022026-boop.github.io/GAME_CRUSH_BR/`.

## Testar a instalação
- **Android (Chrome):** menu ⋮ → "Instalar app" / "Adicionar à tela inicial".
- **iPhone (Safari):** Compartilhar → "Adicionar à Tela de Início".
- **Offline:** abra uma vez com internet, ative o modo avião e abra de novo.

## Atualizar o jogo
Edite `index.html`, troque `VERSION` em `sw.js` (ex.: `crush-br-v2`) e envie. Os jogadores recebem a nova versão ao reabrir.

## Anúncios
Antes do `<script>` principal do `index.html`, defina `window.CRUSH_ADS = { banner(el){}, interstitial(){}, rewarded(){} }` com o código da sua rede. Veja o comentário "ANÚNCIOS" no jogo. Sem isso, aparecem os espaços de demonstração.
Atenção: o save fica no navegador de cada pessoa (localStorage). Limpar dados do site apaga o progresso.
