# Grupo APS — Deploy na Vercel

## Estrutura
- `public/` → site estático (HTML/CSS/JS minificados)
- `vercel.json` → configuração (cleanUrls, headers, cache assets)

## Passos (interface web)
1. Acede a https://vercel.com/ e cria conta.
2. Clica **Add New… → Project → Import** e selecciona “**Deploy from Git**” ou “**Deploy**” (drag-and-drop).
3. Se fizeres drag-and-drop deste ZIP, a Vercel cria o projeto automaticamente.
4. Em **Project Settings → Build & Output → Output Directory**, define `public` (se não for detectado automaticamente).
5. Deploy e testa a URL gerada.
6. Em **Settings → Domains**, adiciona o teu domínio. Se o domínio estiver na Vercel, o DNS é automático; caso contrário, aponta um CNAME para `cname.vercel-dns.com`.

## Sugestões
- Mantém os links **relativos** (ex.: `contabilidade.html`) para funcionar localmente e em qualquer host.
- Usa **Headers** em `vercel.json` para cache de assets (já configurado).
- Quando mudares assets, altera o nome do ficheiro (cache-busting) ou desactiva `immutable`.

