# README Improvement Notes

Melhorias identificadas para o README do perfil GitHub. Pendentes de implementação.

---

## 1. Header visual (impacto alto)

### Capsule Render — banner wave no topo e rodapé

Substituir o `<h1>` texto puro por um banner gerado com [Capsule Render](https://github.com/kyechan99/capsule-render). Combina com o tema escuro do portfolio (dark + emerald).

**Header:**
```markdown
<img src="https://capsule-render.vercel.app/api?type=waving&color=0,0d1117,10b981&height=200&section=header&text=Keuvyn%20Teixeira&fontSize=50&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Full%20Stack%20Developer&descAlignY=56&descSize=20&descColor=10b981" width="100%"/>
```

**Footer (espelha o wave do header):**
```markdown
<img src="https://capsule-render.vercel.app/api?type=waving&color=0,10b981,0d1117&height=100&section=footer" width="100%"/>
```

### Typing SVG — subtítulo animado

Substituir o parágrafo estático de tagline por uma animação de digitação com [readme-typing-svg](https://github.com/DenverCoder1/readme-typing-svg). Alterna entre diferentes roles/skills.

```markdown
<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&pause=1200&color=10B981&center=true&vCenter=true&width=500&lines=Full+Stack+Developer;SaaS+%26+AI-powered+products;Next.js+%C2%B7+TypeScript+%C2%B7+Node.js;Available+for+remote+roles" alt="Typing SVG"/>
</p>
```

Linhas sugeridas (editar conforme preferência):
- `Full Stack Developer`
- `SaaS & AI-powered products`
- `Next.js · TypeScript · Node.js`
- `Available for remote roles`
- `Building end-to-end from schema to deploy`

---

## 2. Estrutura do header pós-melhorias

Ordem recomendada após as mudanças:

```
[Capsule Render wave + nome]
[Typing SVG animado]
[Badges: Portfolio | LinkedIn | Email]
[Status pills: Available | UTC-3 | Overlap | Async-first]
---
[Bio]
...
[Footer wave]
```

---

## 3. Streak Stats (impacto médio)

Adicionar o card de streak ao lado das GitHub Stats para mostrar consistência de contribuições.

```markdown
<p align="center">
  <img height="160" src="https://github-readme-stats.vercel.app/api?username=keuvyndev&show_icons=true&theme=github_dark&hide_border=true&include_all_commits=true"/>
  &nbsp;
  <img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=keuvyndev&layout=compact&theme=github_dark&hide_border=true"/>
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=keuvyndev&theme=github-dark-blue&hide_border=true&date_format=j%20M%5B%20Y%5D"/>
</p>
```

> Nota: o streak card só fica bom quando houver contribuições consistentes. Avaliar quando o histórico de commits melhorar.

---

## 4. Profile views counter (impacto baixo)

Badge discreta que mostra quantas vezes o perfil foi visitado. Coloca abaixo dos status pills ou no rodapé.

```markdown
<img src="https://komarev.com/ghpvc/?username=keuvyndev&color=10b981&style=flat-square&label=profile+views"/>
```

---

## 5. Separadores visuais entre seções (impacto baixo)

Trocar os `---` por uma linha SVG customizada para consistência visual com o banner.

```markdown
<img src="https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/colored.png" width="100%"/>
```

Ou versão minimalista com gradiente:
```markdown
<img src="https://capsule-render.vercel.app/api?type=rect&color=0,0d1117,10b981,0d1117,0&height=2" width="100%"/>
```

---

## 6. Tech Stack com ícones Devicons (impacto médio)

Alternativa aos shields.io atuais — ícones coloridos maiores, mais visual e escaneável.

```markdown
<p align="center">
  <img src="https://skillicons.dev/icons?i=nextjs,react,ts,tailwind,nodejs,prisma,postgres,docker,vercel&theme=dark"/>
</p>
```

Referência: [skillicons.dev](https://skillicons.dev)

> Pode combinar: usar skillicons para o bloco principal e manter os shields.io para tecnologias menores que não têm ícone lá.

---

## 7. Seção "Currently" ou "Now" (impacto médio)

Bloco rápido de contexto atual — substitui ou complementa parte da bio. Útil para recrutadores que querem saber o status de forma imediata.

```markdown
**Currently**
- Working at Plano Consultoria Empresarial as Developer & Team Leader
- Shipping freelance products (SaaS, AI tools, e-commerce)
- Open to international remote full-time or contract roles
```

---

## 8. Ordem dos projetos featured (revisão)

Considerar reordenar pela impressão que causam:

1. **Forja3D** — maior breadth de features (atual posição 1 ✓)
2. **Finance AI** — SaaS + AI + Stripe = stack mais alinhada com mercado internacional
3. **Fila Cidadã** — complexidade técnica (state machine, multi-role)
4. **Smart Crypto Trade** — mais simples, manter como 4º

Argumento: Finance AI ter Stripe + OpenAI + SaaS chama mais atenção de empresas internacionais do que Fila Cidadã (produto mais local/BR).

---

## Prioridade sugerida de implementação

| # | Melhoria | Esforço | Impacto |
|---|----------|---------|---------|
| 1 | Capsule Render header + footer | Baixo | Alto |
| 2 | Typing SVG animado | Baixo | Alto |
| 3 | skillicons.dev no stack | Baixo | Médio |
| 4 | Reordenar projetos featured | Mínimo | Médio |
| 5 | Seção "Currently" | Mínimo | Médio |
| 6 | Streak stats | Baixo | Médio* |
| 7 | Profile views counter | Mínimo | Baixo |
| 8 | Separadores SVG | Baixo | Baixo |

*Implementar quando commits forem mais consistentes.
