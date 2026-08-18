---
permalink: /
title: ""
author_profile: false
redirect_from:
  - /about/
  - /about.html
---

{::nomarkdown}
<div class="sn-home">

  <header class="hero-shell reveal">
    <div class="hero-top">
      <div class="hero-id">
        <p class="hero-kicker">Trustworthy language-model evaluation</p>
        <h1>Moustafa Yehia Hassan</h1>
        <p class="role">AI / NLP Researcher · LLM Evaluation · Model Auditing · Biomedical &amp; Mental-Health NLP</p>
        <p class="lede">
          I build auditable evaluation pipelines that test when language models and NLP
          classifiers <span class="em">appear</span> accurate while relying on brittle shortcuts,
          annotation artifacts, synthetic over-simulation, or distorted population-level signals —
          before such systems are trusted for clinical or benchmark claims.
        </p>
        <p class="focus"><span class="k">Current focus:</span> whether synthetic clinical text and simulated patient personas preserve the population-level structure of real human language, or merely look plausible sentence by sentence.</p>
      </div>
      <img class="avatar" src="/images/avatar.jpg" alt="Portrait of Moustafa Yehia Hassan" width="178" height="178" loading="eager" fetchpriority="high">
    </div>

    <nav class="links links--primary" aria-label="Primary contact and professional links">
      <a href="mailto:{{ site.author.email }}">Email</a>
      <a href="/files/Moustafa_Yehia_Hassan_CV.pdf">CV (PDF)</a>
      <a href="https://github.com/{{ site.author.github }}">GitHub</a>
      <a href="https://www.linkedin.com/in/{{ site.author.linkedin }}">LinkedIn</a>
    </nav>

    <nav class="academic-links" aria-label="Academic profiles">
      <a class="academic-link" href="{{ site.author.googlescholar }}" rel="me">
        <span class="academic-mark" aria-hidden="true">GS</span>
        <span>Google Scholar</span>
      </a>
      <a class="academic-link" href="{{ site.author.orcid }}" rel="me">
        <span class="academic-mark" aria-hidden="true">ID</span>
        <span>ORCID</span>
      </a>
      <a class="academic-link" href="{{ site.author.aclanthology }}" rel="me">
        <span class="academic-mark" aria-hidden="true">ACL</span>
        <span>ACL Anthology</span>
      </a>
      <a class="academic-link" href="{{ site.author.openreview }}" rel="me">
        <span class="academic-mark" aria-hidden="true">OR</span>
        <span>OpenReview</span>
      </a>
    </nav>
  </header>

  <div class="rolefit">
    <b>Open to:</b> AI/NLP Research · LLM Evaluation · Model Auditing ·
    Biomedical / Mental-Health NLP · Remote / Qatar / GCC
  </div>

  <div class="chips" aria-label="Research highlights">
    <a class="chip chip--link" href="https://aclanthology.org/2026.bionlp-1.1/"><span class="dot"></span>Published · ACL BioNLP 2026</a>
    <a class="chip chip--link" href="https://ieeexplore.ieee.org/document/11621198"><span class="dot"></span>Published · IEEE ICBCB 2026</a>
    <span class="chip"><span class="dot"></span>Distributional-fidelity auditing</span>
    <span class="chip"><span class="dot"></span>Reproducible ML pipelines</span>
  </div>

  <section id="research">
    <p class="eyebrow">Research</p>
    <h2>Testing whether models learn robust signals or exploit shortcuts</h2>
    <p class="sub">I design evaluation pipelines for LLM and NLP systems — with emphasis on distributional fidelity, calibration, leakage control, and clinical-language reliability — as statistically rigorous, reproducible workflows that surface failure before claims of clinical or benchmark validity.</p>
    <div class="pillars">
      <div class="pillar">
        <p class="name">Trustworthy LLM &amp; synthetic-data evaluation</p>
        <p>Distributional-fidelity auditing; persona, benchmark &amp; calibration validity (TADA, FRFA, MAUVE, MMD).</p>
      </div>
      <div class="pillar">
        <p class="name">Computational mental-health NLP</p>
        <p>Shortcut-learning and label-bias diagnostics; atypicality-graded failure analysis.</p>
      </div>
      <div class="pillar">
        <p class="name">Biomedical NLP reliability</p>
        <p>Deterministic preprocessing, margin-based abstention, and token-level audit trails.</p>
      </div>
      <div class="pillar">
        <p class="name">Interpretability <span class="tag">emerging</span></p>
        <p>Hidden-state probing and activation-capture experiments over frozen LLMs (nnsight, TransformerLens).</p>
      </div>
    </div>
  </section>

  <section id="projects">
    <p class="eyebrow">Selected systems &amp; evaluation projects</p>
    <h2>Evaluation pipelines I have designed, implemented, and evaluated</h2>
    <p class="sub">End-to-end, reproducible infrastructure — not just findings.</p>
    <div class="projects-grid">

      <article class="proj">
        <p class="pname">TSS — Triple-Stream Stress Probe</p>
        <p class="pdesc">A white-box diagnostic framework that tests whether mental-health NLP classifiers learn robust clinical signals or rely on lexical shortcuts and annotation artifacts — with an interventional masking suite for quasi-causal evidence.</p>
        <div class="pmeta">
          <p class="stack"><b>Built with</b> Python · scikit-learn · ElasticNet probes · character n-grams · masking tests · bootstrap inference</p>
          <p class="ev"><b>Evidence</b> Published at ACL BioNLP 2026 · N = 12,906 across four datasets</p>
          <p class="plinks"><a href="https://aclanthology.org/2026.bionlp-1.1/">Paper ↗</a> · <a href="https://aclanthology.org/2026.bionlp-1.1.pdf">PDF ↗</a> · <a href="https://github.com/myh-ai/TSS-Probe-CMH">Code ↗</a></p>
        </div>
      </article>

      <article class="proj">
        <p class="pname">Distributional-Fidelity Audit Pipeline</p>
        <p class="pdesc">An end-to-end pipeline comparing human clinical-language distributions with LLM-simulated personas, diagnosing population-level deformation that sentence-level metrics miss.</p>
        <div class="pmeta">
          <p class="stack"><b>Built with</b> TADA · FRFA · MAUVE · MMD · calibration (ECE, Brier) · hierarchical bootstrap · seed-locked splits · leakage control</p>
          <p class="ev"><b>Evidence</b> Two manuscripts under review · five generator families audited</p>
          <p class="plinks"><a href="https://github.com/myh-ai/tss-w_PGG">PGG code ↗</a> · <a href="https://github.com/myh-ai/Stereotype-Lock-tss_w">STLE code ↗</a></p>
        </div>
      </article>

      <article class="proj">
        <p class="pname">Synthetic Validation Trap Benchmark</p>
        <p class="pdesc">A downstream benchmark testing whether depression detectors trained on LLM-generated text generalize to real human language, across many training conditions and detector families.</p>
        <div class="pmeta">
          <p class="stack"><b>Built with</b> TF-IDF+LR · SBERT+LR · fine-tuned RoBERTa · hierarchical bootstrap (M×B = 100×1000) · SHA-256 integrity verification</p>
          <p class="ev"><b>Evidence</b> Pre-registered protocol · frozen human holdout cohort · SHA-256 integrity checks</p>
          <p class="plinks">Code &amp; pre-registration release pending review</p>
        </div>
      </article>

      <article class="proj">
        <p class="pname">Biomedical NLP Reliability Layer</p>
        <p class="pdesc">A conservative reliability layer for biomedical text classification: deterministic correction, margin-based abstention, safety gates, and token-level audit trails.</p>
        <div class="pmeta">
          <p class="stack"><b>Built with</b> Python · BioBERT · scispaCy · UMLS · McNemar's exact test · bounded edit-distance correction</p>
          <p class="ev"><b>Evidence</b> Published in IEEE Xplore · 94.6% error-fix recall, zero harmful edits</p>
          <p class="plinks"><a href="https://ieeexplore.ieee.org/document/11621198">IEEE Xplore ↗</a> · <a href="https://github.com/myh-ai/the_signal_in_the_noise_CORD19_project">Code ↗</a></p>
        </div>
      </article>

    </div>
  </section>

  <div class="skills">
    <p class="eyebrow">Core methods &amp; tools</p>
    <p class="line"><b>Methods</b> LLM &amp; synthetic-data evaluation · NLP classification · distributional-fidelity auditing · calibration (ECE, Brier) · bootstrap inference · MMD / MAUVE · leakage control · pre-registration · early mechanistic-interpretability experiments (hidden-state probing, activation capture, activation steering)</p>
    <p class="line"><b>Tools</b> Python · PyTorch · Hugging Face Transformers · LoRA / PEFT · sentence-transformers · RoBERTa / BERT / BioBERT · scikit-learn · pandas / NumPy · nnsight · TransformerLens · Git/GitHub · LaTeX</p>
  </div>

  <section id="publications">
    <p class="eyebrow">Selected publications</p>
    <h2>Peer-reviewed publications &amp; active manuscripts</h2>
    <p class="sub">Publisher records, persistent identifiers, code, and citation resources are linked directly below.</p>

    <div class="publication-list">
      {% for paper in site.data.publications.published %}
      <article class="pub pub--published" itemscope itemtype="https://schema.org/ScholarlyArticle">
        <div class="pub__topline">
          <span class="pub__status">{{ paper.status }}</span>
          <span class="pub__year" itemprop="datePublished">{{ paper.year }}</span>
        </div>
        <h3 class="ttl" itemprop="headline">{{ paper.title }}</h3>
        <p class="contrib" itemprop="description">{{ paper.summary }}</p>
        <p class="pub__venue"><span>{{ paper.venue }}</span>{% if paper.note %}<span>{{ paper.note }}</span>{% endif %}</p>
        <div class="pub__actions" aria-label="Links for {{ paper.title | escape }}">
          {% for link in paper.links %}
          <a href="{{ link.url }}" itemprop="url">{{ link.label }} <span aria-hidden="true">↗</span></a>
          {% endfor %}
        </div>
      </article>
      {% endfor %}

      {% for paper in site.data.publications.manuscripts %}
      <article class="pub pub--manuscript">
        <div class="pub__topline">
          <span class="pub__status pub__status--muted">{{ paper.status }}</span>
          <span class="pub__year">{{ paper.year }}</span>
        </div>
        <h3 class="ttl">{{ paper.title }}</h3>
        <p class="contrib">{{ paper.summary }}</p>
        <div class="pub__actions pub__actions--muted" aria-label="Links for {{ paper.title | escape }}">
          {% for link in paper.links %}
          <a href="{{ link.url }}">{{ link.label }} <span aria-hidden="true">↗</span></a>
          {% endfor %}
        </div>
      </article>
      {% endfor %}
    </div>

    <nav class="publication-profiles" aria-label="Complete publication profiles">
      <a href="{{ site.author.googlescholar }}" rel="me">Google Scholar</a>
      <a href="{{ site.author.aclanthology }}" rel="me">ACL Anthology author page</a>
      <a href="{{ site.author.orcid }}" rel="me">ORCID record</a>
      <a href="{{ site.author.openreview }}" rel="me">OpenReview profile</a>
    </nav>
  </section>

  <section id="background">
    <p class="eyebrow">Background</p>
    <h2>Interdisciplinary by design</h2>
    <p class="why">
      A decade of institutional data governance underpins my emphasis on auditability and
      traceability; graduate training in comparative literature sharpens my attention to
      ambiguity, context, and meaning — the distinction between surface fluency and genuine
      signal that reliable NLP evaluation depends on.
    </p>
  </section>

  <section id="writing-teaser">
    <p class="eyebrow">Selected writing</p>
    <h2>Essays on AI, language &amp; evaluation</h2>
    <p class="sub">Featured — <a href="https://myh-ai.github.io/epe/posts/the-shape-of-weary-eyes/">The Shape of Weary Eyes</a>: on synthetic depression data and the risk of substituting machine-generated text for real human clinical language.</p>
    <p class="more"><a href="/writing/">Selected essays →</a> &nbsp;·&nbsp; <a href="https://myh-ai.github.io/epe/">Escaping Planet Earth →</a></p>
  </section>

  <section id="news">
    <p class="eyebrow">News</p>
    <h2>Recent</h2>
    <div class="news" style="margin-top:8px;">
      <div class="row"><span class="yr">2026</span><span><a href="https://aclanthology.org/2026.bionlp-1.1/">The Divergence Hypothesis</a> published in the ACL Anthology as part of BioNLP 2026.</span></div>
      <div class="row"><span class="yr">2026</span><span><a href="https://ieeexplore.ieee.org/document/11621198">The Signal in the Noise</a> published in IEEE Xplore.</span></div>
      <div class="row"><span class="yr">2026</span><span>Building distributional-fidelity auditing pipelines for synthetic clinical text; two manuscripts under review.</span></div>
      <div class="row"><span class="yr">2026</span><span>Open to AI/NLP research, LLM evaluation, model auditing, and biomedical / mental-health NLP roles.</span></div>
    </div>
  </section>

</div>
{:/nomarkdown}
