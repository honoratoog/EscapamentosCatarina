# SDD Spec — Landing Page: Escapamentos Catarina

> **Spec-Driven Development (SDD)** é uma abordagem em que a especificação do produto é escrita *antes* do código. O spec serve como contrato entre designer, desenvolvedor e IA, garantindo que a implementação reflita a intenção original.

---

## 1. Vision Statement

Criar uma landing page moderna e profissional para a **Escapamentos Catarina**, auto center com mais de 30 anos de história em Joinville-SC, com o objetivo de converter visitantes em clientes via WhatsApp ou ligação telefônica.

---

## 2. Goals & Non-Goals

### Goals
- Apresentar os serviços de forma clara e organizada
- Destacar diferenciais: 30+ anos de experiência, equipe especializada, Kit GNV
- Gerar conversão via WhatsApp e telefone
- Ser responsivo (mobile-first)
- Carregar rápido (HTML/CSS puro, sem dependências pesadas)

### Non-Goals
- Sistema de agendamento online
- Área do cliente / login
- Blog ou conteúdo dinâmico
- E-commerce de peças

---

## 3. User Stories

| ID | Como... | Quero... | Para... |
|----|---------|----------|---------|
| US-01 | Motorista com problema no escapamento | Ver rapidamente que a oficina é especialista no serviço | Confiar que vou ao lugar certo |
| US-02 | Cliente em busca de GNV | Ver informações sobre instalação e qualidade do kit | Tomar decisão de conversão |
| US-03 | Usuário mobile | Clicar em um botão e abrir o WhatsApp diretamente | Agendar sem precisar digitar número |
| US-04 | Novo morador de Joinville | Ver endereço e mapa facilmente | Saber onde fica a oficina |
| US-05 | Cliente indeciso | Ver depoimentos ou sinais de credibilidade | Confiar na empresa antes de ir |

---

## 4. Functional Specifications

### 4.1 Seções da Página (em ordem)

#### HERO
- **Título principal:** "Mais de 30 anos cuidando do seu carro"
- **Subtítulo:** Auto center completo em Joinville-SC
- **CTA primário:** Botão "Falar no WhatsApp" → `https://wa.me/554797186768`
- **CTA secundário:** "Ver serviços" (scroll âncora)
- **Fundo:** Escuro com overlay, remetendo ao ambiente de oficina

#### SOBRE NÓS
- Texto institucional com foco em valores: experiência, transparência, gerações
- Destaque de 3 números: `30+ anos`, `7 serviços`, `2 telefones de contato`

#### SERVIÇOS
- Grid de cards com ícone + título + descrição curta
- 7 serviços: GNV/Reteste, Injeção Eletrônica, Scanner, Pneu/Geometria/Balanceamento, Escapamento/Catalisador, Suspensão/Freio, Troca de Óleo
- Card de destaque para GNV (serviço principal)

#### KIT GNV
- Seção dedicada com lista de especialidades
- 3 badges: Economia, Segurança, Eficiência
- CTA: "Solicitar orçamento GNV"

#### CONTATO
- Endereço: R. Dr. João Colin, 2037 - América, Joinville-SC
- Telefone: (47) 3435-3705
- WhatsApp: (47) 99718-6768 e (47) 99170-0611
- E-mail: escapamentoscatarina@gmail.com
- Horário: Seg - Sex: 7h30 - 18h
- Iframe do Google Maps

#### FOOTER
- Logo / nome
- Links das seções
- Redes sociais: Instagram, Facebook
- Copyright

---

## 5. Non-Functional Specifications

| Atributo | Requisito |
|----------|-----------|
| Performance | Carregamento em < 3s em 3G |
| Responsividade | Funcional em 320px até 1920px |
| Acessibilidade | Alt text em imagens, contraste WCAG AA |
| SEO | Meta tags: title, description, OG tags |
| Browser support | Chrome, Firefox, Safari, Edge — últimas 2 versões |

---

## 6. Design Tokens

### Paleta de Cores
```
--color-primary:     #1A1A2E  (azul escuro quase preto — seriedade/profissionalismo)
--color-accent:      #E63946  (vermelho mecânico — energia/ação)
--color-accent-2:    #F4A261  (laranja âmbar — calor/confiança)
--color-surface:     #F8F9FA  (branco gelo — leveza)
--color-text:        #212529  (preto suave)
--color-text-muted:  #6C757D  (cinza)
```

### Tipografia
```
Display: 'Barlow Condensed', sans-serif — peso 700, uppercase para headings de seção
Body:    'Inter', sans-serif — peso 400/500 para textos corridos
```

### Espaçamento
- Base: 8px grid
- Seções: padding 80px top/bottom (desktop), 48px (mobile)

---

## 7. Component Spec

### Button — Primary (WhatsApp)
```
background: #25D366 (verde WhatsApp)
color: white
border-radius: 8px
padding: 14px 28px
font-weight: 600
icon: ícone WhatsApp SVG à esquerda
hover: darken 10%
```

### Service Card
```
background: white
border: 1px solid #E0E0E0
border-radius: 12px
padding: 24px
icon: 40px, cor accent
title: 16px, weight 600
description: 14px, muted
hover: border-color accent, shadow sutil
```

### Stats Counter
```
número: 48px, weight 700, cor accent
label: 14px, muted, uppercase
layout: flex row, gap 40px
```

---

## 8. Acceptance Criteria

- [ ] Botão WhatsApp abre conversa direta no app/web
- [ ] Todos os serviços listados com descrição
- [ ] Mapa do Google Maps embutido e clicável
- [ ] Página responsiva em mobile (375px)
- [ ] Links de redes sociais funcionam e abrem em nova aba
- [ ] Telefones são `<a href="tel:...">` clicáveis no mobile
- [ ] Seção KIT GNV com lista de especialidades
- [ ] Footer com copyright e links

---

## 9. MCP Integration (Antigravity / AI for Code)

Este spec foi projetado para ser consumido por uma IA de geração de código. As instruções abaixo servem como prompt para o Antigravity IDE:

```
Contexto: Você é um desenvolvedor front-end expert em HTML/CSS/JS vanilla.
Spec: [este documento]
Tarefa: Implemente a landing page conforme o spec acima.
Regras:
  - HTML semântico (header, nav, main, section, footer)
  - CSS custom properties para todos os tokens
  - Sem frameworks externos (exceto Google Fonts)
  - JavaScript mínimo (smooth scroll, navbar sticky)
  - Imagens: use placeholders via placehold.co
  - Entrega: arquivo único index.html
```

---

## 10. Stitch Prototype Notes

Para importar no Stitch (Google):
1. Usar as cores do Design Tokens acima
2. Componentes: Navbar, HeroSection, StatsBar, ServiceGrid, GNVSection, ContactSection, Footer
3. Fluxo de prototipagem: Home → click CTA → WhatsApp (link externo)
4. Testar no frame Mobile 390 e Desktop 1440

---

*Spec versão 1.0 — criado em 18/06/2026*
*Entregável: SDD + Landing Page (index.html) + Protótipo Stitch*
