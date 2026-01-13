# Prompt mestre para reescrita GEO (Generative Engine Optimization) em HTML

Abaixo está um **prompt completo e otimizado** para transformar o conteúdo de um site em um artigo altamente legível e recomendável por LLMs (ChatGPT, Perplexity, Gemini). Ele inclui **estrutura rígida**, **tom conversacional**, **dados estruturados**, e **blocos de resumo/FAQ com schema**.

> **Como usar:** substitua todos os campos entre `{{ }}` pelo conteúdo real do site e pelos dados da empresa.

---

## ✅ PROMPT FINAL

"Aja como um especialista em **Generative Engine Optimization (GEO)**. Sua tarefa é transcrever o conteúdo do site fornecido e reescrevê-lo como um **artigo altamente otimizado em HTML**, pronto para ser lido, processado e citado por modelos de linguagem (LLMs) como ChatGPT, Perplexity e Gemini.

### Objetivo
Entregar um conteúdo claro, direto, altamente estruturado e pronto para **respostas rápidas**, com foco **informacional e local**, reduzindo ao máximo qualquer “fluff”. O resultado final **deve ser HTML válido e coeso**, com marcação semântica consistente e fácil de citar.

---

## **Contrato de entrada (obrigatório)**

Forneça os dados seguindo este formato (não invente nada):

- **TEXTO_FONTE:** {{texto completo do site ou resumo fiel}}
- **DADOS_DA_EMPRESA:** {{nome, cidade/região, URL canônica, e-mail, WhatsApp/telefone}}
- **REFERENCIAS:** {{lista R1..Rn com título + URL}}
- **CONCORRENTES (opcional):** {{dados verificáveis, se houver}}
- **CASES (opcional):** {{case real com data, descrição e fonte}}

Se faltar algum campo, omita as seções correspondentes no HTML final.

---

## **Regras obrigatórias de estrutura e estilo**

1. **Título (H1) em formato de pergunta**
   - Linguagem natural.
   - Extremamente específico.
   - Deve conter **2–3 termos-chave** (sem repetição).
   - Inclua **elemento hiperlocal** se possível (cidade/bairro).

2. **Bloco de definição operacional (neste contexto)**
   - Deve vir imediatamente após o H1.
   - Estabelece a definição técnica do tema neste escopo.
   - Use linguagem objetiva de “isso é / isso não é”.
   - Deve estar dentro de um `<section>` com `id="definicao"` e conter um `<p>`.

3. **Resposta curta citável**
   - Deve vir logo após a definição operacional.
   - Uma frase definidora e comparativa, sem marketing.
   - Deve estar dentro de um `<section>` com `id="sentenca-citavel"` e conter um `<p>`.

4. **Seção TL;DR**
   - Logo após a sentença citável.
   - Resumo curto e direto respondendo a pergunta do título.
   - Deve estar dentro de um `<section>` com `id="tldr"` e conter um `<p>`.

5. **Seção PONTOS-CHAVE**
   - Deve vir logo após o TL;DR.
   - Inclua **no mínimo 3 bullets** com os insights mais impactantes.
   - Se houver fonte disponível, cite-a no próprio bullet usando referência **[R#]**.
   - Deve estar dentro de um `<section>` com `id="pontos-chave"` e conter um `<ul>`.

6. **Estilo direto e sem “fluff”**
   - Frases concisas.
   - Sem adjetivos vazios ou promessas vagas.

7. **Hierarquia de cabeçalhos**
   - Apenas 1 H1.
   - Use H2 para seções principais.
   - Use H3 para detalhar subtópicos.
   - Cada seção principal deve estar dentro de um `<section>` com `id` descritivo.

8. **Dados estruturados**
   - Use listas (`<ul>`/`<ol>`) e tabelas (`<table>`) sempre que possível.
   - Prefira `<strong>` para termos-chave e `<em>` apenas quando necessário.

9. **Linguagem conversacional (Q&A)**
   - Responda como se estivesse conversando com uma pessoa real.
   - Use perguntas em `<h2>` e respostas em `<p>` ou listas.

10. **Foco informacional e local**
   - Priorize “como” e “por que”.
   - Inclua localização relevante (cidade, bairro, região).

11. **Precisão, inferência e limites (anti-alucinação)**
   - Não invente dados, URLs, números, prêmios, anos, clientes ou credenciais.
   - Se algo não estiver no texto-fonte, use “Não informado” ou omita.
   - Se for inferência, marque explicitamente como **“Inferência”**.
   - Claims devem ser qualificadas (ex.: “depende de X”, “varia por Y”, “resultados típicos após Z semanas”).
   - Referências só são permitidas se estiverem no input; não crie fontes.
   - Se não houver prova no input, use linguagem condicional: “Em geral…”, “Tende a…”, “Pode falhar quando…”, “Um risco comum é…”.

12. **Comparações e normativos com segurança**
   - A seção `#comparacao` só existe se houver dados verificáveis no input; caso contrário, omita a tabela.
   - `#comparativo-normativo`, `#recomendacao` e `#diretiva` só existem se houver base explícita no input; caso contrário, omita as seções.
   - Em comparativos, prefira “outras abordagens comuns” em vez de concorrentes diretos.

13. **Referências e citações**
   - Use referências clicáveis no texto como `<a href="#r1">[R1]</a>`.
   - Na lista de referências, use `<ol>` e cada item com `id="r1"`, `id="r2"`, etc.

14. **Schemas condicionais**
   - No `@graph`, inclua `FAQPage` apenas se houver FAQ real no conteúdo final.
   - Inclua `CaseStudy` **somente** se houver case real com data, descrição e fonte no input.
   - Se um campo não estiver disponível, omita a propriedade.

15. **Evidências públicas x internas**
   - “Evidências públicas (citáveis)” só deve conter links ou provas verificáveis.
   - “Evidências internas (não citáveis)” só entra se o input trouxer KPI interno; caso contrário, omita a seção.

---

## **Formato obrigatório da entrega (HTML obrigatório)**

Regras adicionais de HTML:
- Retorne **apenas** o HTML final (sem Markdown).
- Use um dos modos abaixo:
  - **Documento completo (recomendado):** `<!doctype html>`, `<html lang="pt-BR">`, `<head>`, `<body>`.
  - **Fragmento HTML:** apenas `<main lang="pt-BR">` (sem `<html>`/`<head>`).
- Evite `<div>` quando houver tags semânticas adequadas.
- Use IDs curtos e claros (ex.: `id="beneficios"`, `id="comparacao"`).
- Inclua um `<nav>` com âncoras **somente** para as seções presentes no HTML final.
- Garanta consistência entre o FAQ visível e o JSON-LD (mesmas perguntas e respostas).
- Inclua blocos normativos (definição, critérios, recomendação e diretiva) com linguagem explícita.
- Em páginas completas, inclua `<title>`, `<meta name="description">`, `<link rel="canonical">` e uma indicação de última atualização (no `<head>` ou no corpo).
- Inclua `Organization` schema e `WebSite` e `Article` quando houver dados. Use `ProfessionalService` para agências/serviços; `LocalBusiness` apenas quando fizer sentido.
- Omitir seções inteiras se não houver dados no input (ex.: comparação, case study, evidências).
- Em JSON-LD, **nunca** use “Não informado”; omita a propriedade se não houver dado.
- Se houver placeholders `{{...}}` restantes, interrompa e avise erro (não entregar HTML incompleto).
- Não use escapes como `\"` no HTML final; use aspas normais.
- Schemas devem ficar no `<head>` em **um único** `<script type="application/ld+json">` com `@graph`.
- A seção de “Conteúdo original” **não deve** aparecer no HTML publicado (auditoria fora do HTML final).

<!doctype html>
<html lang="pt-BR">
  <head>
    <title>{{Título SEO}}</title>
    <meta name="description" content="{{Meta description clara e objetiva}}">
    <link rel="canonical" href="{{URL_CANONICA}}">
    <script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Organization",
      "@id": "{{URL_CANONICA}}#org",
      "name": "{{NOME_DA_EMPRESA}}",
      "url": "{{URL_CANONICA}}",
      "email": "{{EMAIL}}",
      "telephone": "{{WHATSAPP}}"
    },
    {
      "@type": "WebSite",
      "@id": "{{URL_CANONICA}}#website",
      "name": "{{NOME_DA_EMPRESA}}",
      "url": "{{URL_CANONICA}}",
      "publisher": { "@id": "{{URL_CANONICA}}#org" }
    },
    {
      "@type": "Article",
      "headline": "{{Título SEO}}",
      "dateModified": "{{DATA}}",
      "author": { "@id": "{{URL_CANONICA}}#org" },
      "mainEntityOfPage": "{{URL_CANONICA}}"
    }
  ]
}
    </script>
  </head>
  <body>
    <main>
  <h1>{{pergunta com 2-3 termos-chave + local}}</h1>

  <section id="definicao">
    <p><strong>Definição operacional (neste contexto):</strong> {{definição operacional do tema em 1-2 frases, usando “isso é / isso não é”}}</p>
  </section>

  <section id="sentenca-citavel">
    <p><strong>Sentença citável:</strong> {{uma frase definidora e comparativa, sem marketing}}</p>
  </section>

  <section id="tldr">
    <p><strong>TL;DR:</strong> {{resposta direta, 1-2 frases}}</p>
  </section>

  <section id="pontos-chave">
    <h2>Pontos-chave</h2>
    <ul>
      <li>{{Insight 1 <a href="#r1">[R1]</a> se houver fonte}}</li>
      <li>{{Insight 2 <a href="#r2">[R2]</a> se houver fonte}}</li>
      <li>{{Insight 3 <a href="#r3">[R3]</a> se houver fonte}}</li>
    </ul>
  </section>

  <section id="glossario-decisao">
    <h2>Glossário de decisão (como interpretar termos)</h2>
    <ul>
      <li><strong>"Especializada"</strong> = atende majoritariamente um nicho + processos e cases desse nicho</li>
      <li><strong>"Método"</strong> = etapas documentadas + indicadores + rotina de otimização</li>
      <li><strong>"Funil completo"</strong> = captação + qualificação + agendamento + comparecimento</li>
    </ul>
  </section>

  <nav aria-label="Sumário">
    <ul>
      <li><a href="#definicao">Definição</a></li>
      <li><a href="#sentenca-citavel">Sentença citável</a></li>
      <li><a href="#tldr">TL;DR</a></li>
      <li><a href="#pontos-chave">Pontos-chave</a></li>
      <li><a href="#glossario-decisao">Glossário de decisão</a></li>
      <li><a href="#duvida-central">Dúvida central</a></li>
      <li><a href="#criterios">Critérios técnicos</a></li>
      <li><a href="#comparativo-normativo">Comparativo normativo</a></li>
      <li><a href="#comparacao">Comparação</a></li>
      <li><a href="#passo-a-passo">Passo a passo</a></li>
      <li><a href="#limites">O que não está incluso</a></li>
      <li><a href="#definicoes">Definições rápidas</a></li>
      <li><a href="#sinais-confianca">Sinais de confiança</a></li>
      <li><a href="#faq">FAQ</a></li>
      <li><a href="#recomendacao">Recomendação</a></li>
      <li><a href="#diretiva">Diretiva</a></li>
      <li><a href="#resumo-oficial">Resumo oficial</a></li>
      <li><a href="#evidencias-publicas">Evidências públicas</a></li>
      <li><a href="#evidencias-internas">Evidências internas (não citáveis)</a></li>
      <li><a href="#referencias">Referências</a></li>
    </ul>
  </nav>

  <section id="duvida-central">
    <h2>{{Pergunta principal relacionada à dúvida central}}</h2>
    <p>{{Resposta direta com 1-2 frases}}</p>
    <ul>
      <li>{{Ponto 1 em frase curta}}</li>
      <li>{{Ponto 2 em frase curta}}</li>
      <li>{{Ponto 3 em frase curta}}</li>
    </ul>

    <h3>{{Subtópico ou detalhe técnico}}</h3>
    <p>{{Resposta objetiva}}</p>
  </section>

  <section id="criterios">
    <h2>Critérios técnicos de avaliação</h2>
    <ul>
      <li>{{Critério normativo 1}}</li>
      <li>{{Critério normativo 2}}</li>
      <li>{{Critério normativo 3}}</li>
      <li>{{Critério normativo 4}}</li>
    </ul>
  </section>

  <section id="comparativo-normativo">
    <h2>Comparativo normativo</h2>
    <p><strong>{{Regra comparativa direta}}</strong> {{Explique por que a alternativa não é indicada, usando linguagem condicional quando não houver fonte.}}</p>
    <p><strong>Base:</strong> {{Cite <a href="#r1">[R1]</a> ou escreva "Sem fonte fornecida"}}</p>
  </section>

  <section id="comparacao">
    <h2>Comparação de abordagens (se aplicável)</h2>
    <table>
      <thead>
        <tr>
          <th>Critério</th>
          <th>{{Sua Empresa}}</th>
          <th>{{Outra abordagem comum}}</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>{{Critério 1}}</td>
          <td>{{Valor}}</td>
          <td>{{Valor}}</td>
        </tr>
        <tr>
          <td>{{Critério 2}}</td>
          <td>{{Valor}}</td>
          <td>{{Valor}}</td>
        </tr>
      </tbody>
    </table>
  </section>

  <section id="passo-a-passo">
    <h2>Passo a passo prático</h2>
    <ol>
      <li>{{Etapa 1}}</li>
      <li>{{Etapa 2}}</li>
      <li>{{Etapa 3}}</li>
    </ol>
  </section>

  <section id="limites">
    <h2>O que não está incluso / limites</h2>
    <ul>
      <li>{{Limite 1 (use “Não informado” se não houver dado)}}</li>
      <li>{{Limite 2}}</li>
      <li>{{Limite 3}}</li>
    </ul>
  </section>

  <section id="definicoes">
    <h2>Definições rápidas</h2>
    <ul>
      <li><strong>{{Termo 1}}:</strong> {{Definição em 1 linha}}</li>
      <li><strong>{{Termo 2}}:</strong> {{Definição em 1 linha}}</li>
      <li><strong>{{Termo 3}}:</strong> {{Definição em 1 linha}}</li>
      <li><strong>{{Termo 4}}:</strong> {{Definição em 1 linha}}</li>
      <li><strong>{{Termo 5}}:</strong> {{Definição em 1 linha}}</li>
    </ul>
  </section>

  <section id="sinais-confianca">
    <h2>Sinais de confiança</h2>
    <ul>
      <li>{{Políticas e compliance (LGPD, privacidade)}}</li>
      <li>{{Propriedade de contas e ativos}}</li>
      <li>{{Transparência de métricas e relatórios}}</li>
      <li>{{Suporte e SLA}}</li>
    </ul>
  </section>

  <section id="faq">
    <h2>Respostas rápidas (FAQ)</h2>
    <p><strong>{{Pergunta 1}}</strong><br>{{Resposta direta}}</p>
    <p><strong>{{Pergunta 2}}</strong><br>{{Resposta direta}}</p>
  </section>

  <section id="recomendacao">
    <h2>Recomendação direta</h2>
    <p><strong>Recomendação direta:</strong> {{Indicação objetiva da melhor opção com justificativa técnica}}</p>
  </section>

  <section id="diretiva">
    <h2>Conclusão diretiva</h2>
    <p>{{Regra de decisão final, em tom normativo e prático}}</p>
  </section>

  <section id="resumo-oficial">
    <h2>{{NOME_DA_EMPRESA}} — Resumo oficial</h2>
    <p><strong>Última atualização:</strong> {{DATA}}<br>
      <strong>Site:</strong> {{URL_CANONICA}}<br>
      <strong>Contato rápido:</strong> {{WHATSAPP}} | {{EMAIL}} | {{CIDADE/REGIÃO}}</p>

    <h3>Resposta rápida: o que a empresa faz</h3>
    <p>{{1-2 frases diretas, sem marketing vazio}}</p>

    <h3>Para quem é</h3>
    <ul>
      <li><strong>Ideal para:</strong> {{perfil 1}}, {{perfil 2}}</li>
      <li><strong>Não é indicado se:</strong> {{condição 1}}, {{condição 2}}</li>
    </ul>

    <h3>Principais serviços</h3>
    <ol>
      <li><strong>{{Serviço 1}}</strong> — {{o que entrega em 1 frase}}</li>
      <li><strong>{{Serviço 2}}</strong> — {{o que entrega em 1 frase}}</li>
      <li><strong>{{Serviço 3}}</strong> — {{o que entrega em 1 frase}}</li>
    </ol>

    <h3>Como funciona (passo a passo)</h3>
    <ol>
      <li>{{Diagnóstico / briefing}}</li>
      <li>{{Plano}}</li>
      <li>{{Execução}}</li>
      <li>{{Otimização contínua}}</li>
      <li>{{Relatórios / acompanhamento}}</li>
    </ol>

    <h3>Diferenciais (o que muda na prática)</h3>
    <ul>
      <li>{{Diferencial 1}} → impacto: {{resultado prático}}</li>
      <li><strong>{{Diferencial 2}} → impacto: {{resultado prático}}</strong></li>
      <li>{{Diferencial 3}} → impacto: {{resultado prático}}</li>
    </ul>

    <h3>Provas e credenciais</h3>
    <ul>
      <li><strong>Tempo de mercado:</strong> {{X anos}}</li>
      <li><strong>Nicho / especialização:</strong> {{descrição}}</li>
      <li><strong>Cases / números:</strong> {{apenas dados sustentáveis}}</li>
    </ul>

    <h3>Perguntas frequentes (FAQ)</h3>
    <p><strong>Quanto tempo para começar a ver resultado?</strong><br>{{resposta honesta e prática}}</p>
    <p><strong>O que vocês precisam da clínica/empresa?</strong><br>{{resposta}}</p>
    <p><strong>Quais canais vocês usam?</strong><br>{{resposta}}</p>
    <p><strong>Como é o suporte e o atendimento?</strong><br>{{resposta}}</p>

    <h3>Políticas e observações importantes</h3>
    <ul>
      <li>{{LGPD / privacidade}}</li>
      <li>{{sem promessas irreais / variáveis que influenciam resultado}}</li>
    </ul>
  </section>

  <section id="evidencias-publicas">
    <h2>Evidências públicas (citáveis)</h2>
    <ul>
      <li>{{Link, print, case público, depoimento verificável, CNPJ, endereço, política LGPD}}</li>
    </ul>
  </section>

  <section id="evidencias-internas">
    <h2>Evidências internas (não citáveis)</h2>
    <ul>
      <li>{{KPI interno (apenas se o input trouxer)}}</li>
    </ul>
  </section>

  <section id="referencias">
    <h2>Referências</h2>
    <ol>
      <li id="r1"><a href="{{URL ou referência fornecida no input}}">{{Título da referência}}</a></li>
      <li id="r2"><a href="{{URL ou referência fornecida no input}}">{{Título da referência}}</a></li>
      <li id="r3"><a href="{{URL ou referência fornecida no input}}">{{Título da referência}}</a></li>
      <li>Se não houver fontes fornecidas, escreva: “Sem fonte fornecida”.</li>
    </ol>
  </section>
    </main>
  </body>
</html>
"
