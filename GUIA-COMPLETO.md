# 🎬❤️ NetLove — Guia Completo de Deploy

---

## 📁 ESTRUTURA DO PROJETO

```
netlove/
├── index.html          ← o site inteiro (arquivo único!)
└── GUIA-COMPLETO.md    ← este guia
```

---

## 🗂️ PARTE 1 — Supabase (armazenar vídeos e fotos, GRÁTIS)

### 1.1 Criar conta
1. Acesse https://supabase.com
2. Clique em **Start for free**
3. Crie conta com Google ou e-mail

### 1.2 Criar projeto
1. Clique em **New Project**
2. Dê um nome: `netlove`
3. Escolha uma senha forte (guarde!)
4. Selecione **South America (São Paulo)** — mais rápido pro Brasil
5. Clique em **Create new project** e aguarde ~2 minutos

### 1.3 Criar Storage (onde ficam os arquivos)
1. No menu esquerdo, clique em **Storage**
2. Clique em **New bucket**
3. Nome: `midia`
4. Marque **Public bucket** ✅ (para os vídeos serem acessíveis)
5. Clique em **Save**

### 1.4 Fazer upload das fotos e vídeos
1. Clique no bucket `midia`
2. Clique em **Upload files**
3. Suba seus vídeos (mp4, máx 50MB cada no plano grátis) e fotos
4. Após o upload, clique no arquivo e copie a **URL pública**

> A URL terá esse formato:
> `https://SEU-ID.supabase.co/storage/v1/object/public/midia/video1.mp4`

---

## 🐙 PARTE 2 — GitHub (guardar o código)

### 2.1 Criar conta
1. Acesse https://github.com
2. Crie uma conta gratuita

### 2.2 Criar repositório
1. Clique no **+** no canto superior direito → **New repository**
2. Nome: `netlove`
3. Marque **Public** (necessário para Vercel grátis)
4. Clique em **Create repository**

### 2.3 Subir o arquivo
**Opção A — Pelo próprio site do GitHub (mais fácil):**
1. Na página do repositório, clique em **uploading an existing file**
2. Arraste o `index.html`
3. Clique em **Commit changes**

**Opção B — Pelo terminal (se tiver Git instalado):**
```bash
git init
git add index.html
git commit -m "primeiro commit do netlove"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/netlove.git
git push -u origin main
```

---

## 🚀 PARTE 3 — Vercel (hospedar o site, GRÁTIS)

### 3.1 Criar conta
1. Acesse https://vercel.com
2. Clique em **Sign Up** → escolha **Continue with GitHub**
3. Autorize o acesso

### 3.2 Conectar com o GitHub e fazer deploy
1. Na dashboard da Vercel, clique em **Add New → Project**
2. Vai aparecer seus repositórios do GitHub
3. Encontre `netlove` e clique em **Import**
4. Deixe todas as configurações padrão
5. Clique em **Deploy**

> ⏳ Aguarde ~1 minuto. Quando terminar, seu site estará no ar!

### 3.3 URL do site
Após o deploy, a Vercel te dá uma URL assim:
```
https://netlove-seuusuario.vercel.app
```

Qualquer mudança que você fizer no GitHub é atualizada automaticamente na Vercel! ✨

---

## 🌐 PARTE 4 — Domínio Personalizado (opcional, barato)

Se quiser uma URL mais bonita tipo `nossoamor.com.br`:

### 4.1 Comprar domínio
- **Registro.br** — .com.br por ~R$40/ano → https://registro.br
- **Namecheap** — .com por ~$10/ano → https://namecheap.com (paga em USD)
- **Hostinger** — promoções frequentes → https://hostinger.com.br

### 4.2 Apontar para a Vercel
1. Na Vercel, entre no projeto → **Settings → Domains**
2. Clique em **Add Domain**
3. Digite seu domínio: `nossoamor.com.br`
4. A Vercel vai mostrar um código DNS (ex: `cname.vercel-dns.com`)
5. No painel do Registro.br (ou onde comprou), adicione esse registro DNS
6. Aguarde até 24h para propagar (geralmente é rápido, 30min)

---

## 🔗 PARTE 5 — QR Code (para colocar no quadro)

### Gerar QR Code grátis:
1. Acesse https://qr-code-styling.com ou https://www.qrcode-monkey.com
2. Cole a URL do seu site (ex: `https://netlove-seuusuario.vercel.app`)
3. Personalize: escolha cor vermelha (#E50914) para combinar com o tema Netflix
4. Tamanho: 500x500px mínimo para imprimir nítido
5. Baixe em PNG ou SVG

### Onde colocar o QR Code:
- ✅ **Atrás do quadro** — ótima ideia! A pessoa vira e se surpreende
- ✅ Numa cartinha junto ao quadro
- ✅ Num envelope lacrado

---

## ✏️ PARTE 6 — Editar o site com suas informações

Abra o `index.html` num editor de texto (Notepad, VSCode, etc.).

### 6.1 Mudar nomes/textos
Procure por `Flávio & Gabrielly` e troque pelo nome de vocês.
Procure por `Nossa história` e edite a descrição.

### 6.2 Adicionar seus vídeos e fotos (do Supabase)
No arquivo, procure a seção que começa com `const videos = [`.

Para cada vídeo, edite:
```js
{
  title: "Nosso Primeiro Encontro",   // ← nome que aparece no card
  desc: "Aquele dia especial...",      // ← descrição
  videoUrl: "https://SEU-ID.supabase.co/.../video1.mp4",  // ← cole aqui
  thumbUrl: "https://SEU-ID.supabase.co/.../foto1.jpg",   // ← cole aqui
}
```

### 6.3 Mudar nomes dos perfis
Procure por `Eu 💙` e `Meu amor ❤️` e coloque os nomes de vocês.

---

## 📱 PARTE 7 — Print para o quadro

O site já é responsivo (se adapta ao celular e ao computador automaticamente — isso se chama **design responsivo**).

### Para tirar o print para o quadro:
1. Abra o site no celular dela (ou simule no PC)
2. Para simular celular no PC: abra o Chrome, pressione F12 → clique no ícone de celular no topo
3. Selecione `iPhone 14 Pro` ou similar
4. Tire o print da tela inicial (com o hero e a tela de escolha de perfis)

### Dimensões para o quadro 13x18cm:
- Peça a impressão em **13x18cm** ou **5x7 polegadas**
- Resolução: 300 DPI
- Use um aplicativo como Canva ou Photoshop para ajustar o print antes de imprimir

---

## 💰 Resumo de custos

| Serviço | Custo |
|---------|-------|
| Supabase (Storage + DB) | GRÁTIS (até 1GB) |
| GitHub | GRÁTIS |
| Vercel | GRÁTIS |
| QR Code | GRÁTIS |
| Domínio .com.br | ~R$40/ano (opcional) |
| Impressão do quadro | ~R$15-30 (gráfica) |

**Total mínimo: R$0 + impressão do quadro** 🎉

---

## ❓ Dúvidas frequentes

**Q: Precisa de banco de dados?**
R: Não! Como seus vídeos são pequenos (até 40 seg) e poucos, o Storage do Supabase já basta. Sem necessidade de PostgreSQL/pgAdmin.

**Q: O site funciona no celular?**
R: Sim! Ele é 100% responsivo — se adapta automaticamente a qualquer tela (celular, tablet, PC).

**Q: E se ela ficar sem internet?**
R: O site precisa de internet para carregar os vídeos. Para ver offline, seria necessário um app nativo (muito mais complexo).

**Q: Posso adicionar mais vídeos depois?**
R: Sim! Basta subir o vídeo no Supabase, copiar a URL, editar o `index.html` e enviar para o GitHub. A Vercel atualiza automaticamente.

---

Feito com ❤️ — Bom Dia dos Namorados!