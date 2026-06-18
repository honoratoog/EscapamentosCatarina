# 🔧 Landing Page — Escapamentos Catarina

> Projeto desenvolvido com o método **Spec-Driven Development (SDD)**, utilizando **Antigravity IDE (AI for Code)** e protótipo de alta fidelidade no **Stitch (Google)**.

---

## 📋 Sobre o projeto

Landing page moderna e responsiva para a **Escapamentos Catarina**, auto center com mais de 30 anos de experiência em Joinville-SC. O objetivo da página é apresentar os serviços da empresa e converter visitantes em clientes via WhatsApp ou ligação telefônica.

---

## 🗂️ Estrutura do repositório

```
.
├── index.html                          # Landing page (arquivo único, sem dependências)
└── SDD_Spec_Escapamentos_Catarina.md   # Documento de especificação (SDD)
```

---

## ⚙️ Metodologia: SDD (Spec-Driven Development)

O projeto seguiu o fluxo do **Spec-Driven Development**, onde a especificação é escrita *antes* do código:

```
1. Vision Statement   →   O que a página precisa fazer
2. User Stories       →   Para quem e por quê
3. Functional Spec    →   O que cada seção contém
4. Design Tokens      →   Cores, tipografia, espaçamento
5. Acceptance Criteria →   Como validar que está correto
6. Implementação      →   Código gerado a partir do spec
```

O spec completo está em [`SDD_Spec_Escapamentos_Catarina.md`](./SDD_Spec_Escapamentos_Catarina.md).

---

## 🤖 AI for Code — Antigravity IDE

O spec foi usado como prompt estruturado para geração de código no **Antigravity (Google IDE)**. O documento define contexto, regras e entregável esperado, permitindo que a IA produza código alinhado à intenção original sem ambiguidades.

---

## 🎨 Protótipo — Stitch (Google)

O protótipo de alta fidelidade foi criado no **Stitch** seguindo os design tokens definidos no spec:

| Token | Valor |
|-------|-------|
| Cor primária | `#0D1117` |
| Cor de ação | `#E63946` |
| Acento âmbar | `#F4A261` |
| WhatsApp | `#25D366` |
| Tipografia display | Barlow Condensed 700 |
| Tipografia corpo | Inter 400/500 |

---

## 🧩 Seções da landing page

| Seção | Descrição |
|-------|-----------|
| **Hero** | Título principal, subtítulo e CTAs (WhatsApp + Ver serviços) |
| **Stats** | 30+ anos, 7 serviços, 15+ anos GNV, kit 5ª geração |
| **Sobre nós** | História, valores e diferenciais da empresa |
| **Serviços** | Grid com 7 serviços; card de destaque para GNV |
| **Contato** | Endereço, telefones, e-mail, horário e mapa Google Maps |
| **Footer** | Links de navegação, redes sociais e copyright |

---

## 🚀 Como rodar

Nenhuma dependência necessária. Basta abrir o arquivo no navegador:

```bash
# Opção 1 — abrir direto
open index.html

# Opção 2 — servidor local com Python
python3 -m http.server 8080
# acesse http://localhost:8080
```

---

## ✅ Checklist de entrega

- [x] Spec SDD escrito antes do código
- [x] Landing page implementada a partir do spec
- [x] Responsivo (mobile 375px até desktop 1440px)
- [x] Botão WhatsApp com link direto
- [x] Mapa Google Maps embutido
- [x] Telefones clicáveis no mobile (`tel:`)
- [x] Links de redes sociais (Instagram e Facebook)
- [x] HTML semântico e acessível

---

## 📌 Informações da empresa

**Escapamentos Catarina**
- 📍 R. Dr. João Colin, 2037 — América, Joinville-SC
- 📞 (47) 3435-3705
- 📱 (47) 99718-6768 / (47) 99170-0611
- ✉️ escapamentoscatarina@gmail.com
- 🕐 Seg–Sex: 7h30–18h00
- 🌐 [escapamentoscatarina.com.br](https://www.escapamentoscatarina.com.br)

---

*Projeto acadêmico*
