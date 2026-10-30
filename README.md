# Foto Ao Vivo — site público

Site estático com apresentação, Política de Privacidade e Termos de Uso. Sem JavaScript, cookies, analytics, formulários, API ou dependências de fontes/CDN. Suporte público: franciscoandrade.photo@gmail.com.

## Publicação inicial no GitHub Pages

1. Criar repositório **público separado** `capixabapgm-cmyk/fotoaovivo-site`. O repositório privado do aplicativo não deve ser tornado público.
2. Enviar o conteúdo desta pasta à raiz da branch `main` desse novo repositório. Não enviar APKs, código do aplicativo ou credenciais.
3. Settings → Pages → Build and deployment: Deploy from a branch → `main` → `/ (root)` → Save.
4. Aguardar o deploy e verificar as três páginas:
   - `https://capixabapgm-cmyk.github.io/fotoaovivo-site/`
   - `https://capixabapgm-cmyk.github.io/fotoaovivo-site/privacidade/`
   - `https://capixabapgm-cmyk.github.io/fotoaovivo-site/termos/`

Esses são endereços previstos; só estarão ativos após criação/publicação.

## Domínio app.interativa.top

O `www.interativa.top` continua no Google Sites.

1. Na conta GitHub, Settings → Pages → Add a domain: verificar `app.interativa.top` adicionando ao DNS o TXT gerado pelo próprio GitHub. Usar nome/valor exatos apresentados, sem inventar token. Manter esse TXT após a verificação.
2. No novo repositório, Settings → Pages → Custom domain: informar `app.interativa.top` e salvar.
3. No provedor DNS de `interativa.top`, criar registro **CNAME**, nome **app**, destino **capixabapgm-cmyk.github.io**. Não incluir https nem /fotoaovivo-site. Não alterar registros de www, e-mail ou domínio raiz. Se já houver registro para app, conferir o uso antes de substituir.
4. Aguardar propagação e certificado, habilitar Enforce HTTPS quando disponível.
5. Conferir HTTPS nas três URLs finais:
   - `https://app.interativa.top/`
   - `https://app.interativa.top/privacidade/`
   - `https://app.interativa.top/termos/`

O site usa caminhos relativos e funciona tanto no endereço GitHub Pages quanto no subdomínio. A configuração Custom domain gera o arquivo CNAME; não há esse arquivo no pacote inicial.

## Google Sites e OAuth

Google Sites → Páginas → Novo link: adicionar os três endereços finais. Em Google Auth Platform → Branding, usar os mesmos URLs públicos e domínio autorizado `interativa.top`. Confirmar propriedade do domínio no Search Console com a conta responsável pelo projeto OAuth. A hospedagem e os textos não garantem aprovação pelo Google.

## Verificação local

`python3 -m http.server 8765 --directory .`

Abrir http://127.0.0.1:8765/. Testado em Chromium com390px e1280px, três rotas, links internos e sem overflow horizontal. Os textos refletem os recursos conhecidos do app e devem ser mantidos em conformidade com o serviço realmente oferecido. Não substituem revisão jurídica.
