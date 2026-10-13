# MedStudy Br — site institucional

Site de divulgação do app **MedStudy Br** (resumos, flashcards e questões de
medicina, da faculdade à residência), na mesma estrutura do site do AneStudy.

Serve para:
- Divulgar o app (botões de App Store e Google Play começam como "Em breve").
- Hospedar a **Política de Privacidade** e os **Termos de Uso** pedidos pela
  App Store Connect e pela Play Console:
  - https://drluishmg-code.github.io/medstudybr/privacy.html
  - https://drluishmg-code.github.io/medstudybr/terms.html

Esses dois endereços já estão no paywall do app (`www/index.html`).

## Estrutura

```
medstudybr/
├── index.html      → página principal
├── privacy.html    → Política de Privacidade
├── terms.html      → Termos de Uso (inclui as cláusulas de assinatura
│                     com renovação automática e o link do EULA da Apple)
├── contact.html    → Contato
├── style.css · script.js · manifest.json · sitemap.xml
├── assets/
│   ├── logo.png (512) · apple-touch-icon.png (180) · favicon.ico
│   ├── social-preview.png (1200×630, imagem de compartilhamento)
│   └── screenshots/ estudar, faculdade, leitura, flashcards,
│                    questao-detalhe, progresso, ajustes (.jpg)
└── ferramentas/publicar-lojas.py → ativa os botões das lojas
```

## Quando o app for publicado

1. Abra `ferramentas/publicar-lojas.py` e preencha `APPSTORE_URL`
   (e depois `GOOGLE_PLAY_URL`).
2. Na raiz do repositório: `python3 ferramentas/publicar-lojas.py`
3. Ajuste no `index.html` o texto do bloco final ("Em breve para iPhone…")
   e publique (commit + push).

## Números citados no site (13/10/2026)

134 temas · 21.700+ flashcards · 13.000+ questões autorais. Atualize o
`index.html` (hero, "Sobre") e o `social-preview.png` quando mudarem.

## GitHub Pages

Settings → Pages → Source: branch `main`, pasta `/ (root)`. O site fica em
https://drluishmg-code.github.io/medstudybr/
