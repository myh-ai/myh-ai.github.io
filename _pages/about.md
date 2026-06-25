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

  <div class="hero-top reveal">
    <div class="hero-id">
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
    <img class="avatar" src="/images/avatar.jpg" alt="Moustafa Yehia Hassan" width="170" height="170" loading="eager">
  </div>

  <div class="links">
    <a href="mailto:moustafayhassan@gmail.com">Email</a>
    <a href="/files/Moustafa_Yehia_Hassan_CV.pdf">CV (PDF)</a>
    <a href="https://github.com/myh-ai">GitHub</a>
    <a href="https://scholar.google.com/citations?user=EqmgPx4AAAAJ&amp;hl=en">Scholar</a>
    <a href="https://www.linkedin.com/in/moustafa-y-hassan-222ab8104">LinkedIn</a>
    <a href="https://orcid.org/0009-0007-6324-3770">ORCID</a>
  </div>

  <div class="rolefit">
    <b>Open to:</b> AI/NLP Research · LLM Evaluation · Model Auditing ·
    Biomedical / Mental-Health NLP · Remote / Qatar / GCC
  </div>

  <div class="chips">
    <span class="chip"><span class="dot"></span>ACL BioNLP 2026 — Accepted</span>
    <span class="chip"><span class="dot"></span>IEEE ICBCB 2026 — To appear</span>
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

      <div class="proj">
        <p class="pname">TSS — Triple-Stream Stress Probe</p>
        <p class="pdesc">A white-box diagnostic framework that tests whether mental-health NLP classifiers learn robust clinical signals or rely on lexical shortcuts and annotation artifacts — with an interventional masking suite for quasi-causal evidence.</p>
        <div class="pmeta">
          <p class="stack"><b>Built with</b> Python · scikit-learn · ElasticNet probes · character n-grams · masking tests · bootstrap inference</p>
          <p class="ev"><b>Evidence</b> Accepted at ACL BioNLP 2026 · N = 12,906 across four datasets</p>
          <p class="plinks"><a href="https://github.com/myh-ai/TSS-Probe-CMH">Code repository ↗</a> · open-source (MIT)</p>
        </div>
      </div>

      <div class="proj">
        <p class="pname">Distributional-Fidelity Audit Pipeline</p>
        <p class="pdesc">An end-to-end pipeline comparing human clinical-language distributions with LLM-simulated personas, diagnosing population-level deformation that sentence-level metrics miss.</p>
        <div class="pmeta">
          <p class="stack"><b>Built with</b> TADA · FRFA · MAUVE · MMD · calibration (ECE, Brier) · hierarchical bootstrap · seed-locked splits · leakage control</p>
          <p class="ev"><b>Evidence</b> Two manuscripts under review · five generator families audited</p>
          <p class="plinks"><a href="https://github.com/myh-ai/tss-w_PGG">PGG code ↗</a> · <a href="https://github.com/myh-ai/Stereotype-Lock-tss_w">STLE code ↗</a></p>
        </div>
      </div>

      <div class="proj">
        <p class="pname">Synthetic Validation Trap Benchmark</p>
        <p class="pdesc">A downstream benchmark testing whether depression detectors trained on LLM-generated text generalize to real human language, across many training conditions and detector families.</p>
        <div class="pmeta">
          <p class="stack"><b>Built with</b> TF-IDF+LR · SBERT+LR · fine-tuned RoBERTa · hierarchical bootstrap (M×B = 100×1000) · SHA-256 integrity verification</p>
          <p class="ev"><b>Evidence</b> Pre-registered protocol · frozen human holdout cohort · SHA-256 integrity checks</p>
          <p class="plinks">Code &amp; pre-registration release pending review</p>
        </div>
      </div>

      <div class="proj">
        <p class="pname">Biomedical NLP Reliability Layer</p>
        <p class="pdesc">A conservative reliability layer for biomedical text classification: deterministic correction, margin-based abstention, safety gates, and token-level audit trails.</p>
        <div class="pmeta">
          <p class="stack"><b>Built with</b> Python · BioBERT · scispaCy · UMLS · McNemar's exact test · bounded edit-distance correction</p>
          <p class="ev"><b>Evidence</b> Accepted, IEEE ICBCB 2026 (to appear) · 94.6% error-fix recall, zero harmful edits</p>
          <p class="plinks"><a href="https://github.com/myh-ai/the_signal_in_the_noise_CORD19_project">Code repository ↗</a> · open-source (MIT)</p>
        </div>
      </div>

    </div>
  </section>

  <div class="skills">
    <p class="eyebrow">Core methods &amp; tools</p>
    <p class="line"><b>Methods</b> LLM &amp; synthetic-data evaluation · NLP classification · distributional-fidelity auditing · calibration (ECE, Brier) · bootstrap inference · MMD / MAUVE · leakage control · pre-registration · early mechanistic-interpretability experiments (hidden-state probing, activation capture, activation steering)</p>
    <p class="line"><b>Tools</b> Python · PyTorch · Hugging Face Transformers · LoRA / PEFT · sentence-transformers · RoBERTa / BERT / BioBERT · scikit-learn · pandas / NumPy · nnsight · TransformerLens · Git/GitHub · LaTeX</p>
  </div>

  <section id="publications">
    <p class="eyebrow">Selected publications</p>
    <h2>Peer-reviewed &amp; under review</h2>
    <div style="margin-top:8px;">
      <div class="pub">
        <p class="ttl">The Divergence Hypothesis: Unmasking Lexical Interference and Label Bias in Mental Health NLP</p>
        <p class="contrib">Detects lexical interference and label-source bias in mental-health NLP classifiers via a white-box triple-stream probe and a difference-in-differences bias metric.</p>
        <div class="meta"><span class="venue">Accepted · ACL BioNLP 2026</span><a href="https://github.com/myh-ai/TSS-Probe-CMH">Code ↗</a></div>
      </div>
      <div class="pub">
        <p class="ttl">The Signal in the Noise: An Auditable Reliability Layer for Biomedical Text Classification</p>
        <p class="contrib">Builds a deterministic, auditable biomedical NLP reliability layer with margin-based abstention, safety gates, and token-level decision traces.</p>
        <div class="meta"><span class="venue">Accepted · IEEE ICBCB 2026 (to appear)</span><span>corresponding author</span><a href="https://github.com/myh-ai/the_signal_in_the_noise_CORD19_project">Code ↗</a></div>
      </div>
      <div class="pub">
        <p class="ttl">The Stereotype-Lock Effect: Over-Simulation and Variance Compression in LLM Simulated-Patient Personas</p>
        <p class="contrib">Audits LLM-simulated depression personas, revealing over-simulation and variance compressed to a fraction of the human clinical reference.</p>
        <div class="meta"><span class="review">Manuscript under review</span><a href="https://github.com/myh-ai/Stereotype-Lock-tss_w">Code ↗</a></div>
      </div>
      <div class="pub">
        <p class="ttl">The Population-Geometry Gap: Patient Simulation that Looks Right Sentence-by-Sentence but Deforms as a Population</p>
        <p class="contrib">Shows that synthetic patient text can deform population-level geometry even when individual sentences look plausible, motivating geometry-level diagnosis.</p>
        <div class="meta"><span class="review">Manuscript under review</span><a href="https://github.com/myh-ai/tss-w_PGG">Code ↗</a></div>
      </div>
    </div>
    <p class="more"><a href="https://scholar.google.com/citations?user=EqmgPx4AAAAJ&amp;hl=en">All publications on Google Scholar →</a></p>
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
      <div class="row"><span class="yr">2026</span><span>ACL BioNLP paper accepted on lexical interference and label bias in mental-health NLP.</span></div>
      <div class="row"><span class="yr">2026</span><span>IEEE ICBCB paper accepted on auditable biomedical NLP reliability (to appear).</span></div>
      <div class="row"><span class="yr">2026</span><span>Building distributional-fidelity auditing pipelines for synthetic clinical text; two manuscripts under review.</span></div>
      <div class="row"><span class="yr">2026</span><span>Open to AI/NLP research, LLM evaluation, model auditing, and biomedical / mental-health NLP roles.</span></div>
    </div>
  </section>

</div>
{:/nomarkdown}
