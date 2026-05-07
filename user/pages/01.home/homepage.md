---
title: 'SAE Books — The API-first accounting ledger'
menu: Home
autoseo:
    enabled: false
body_classes: homepage
---

<header class="site-header">
  <div class="container row">
    <a href="/" class="wordmark" aria-label="SAE Books home">
      <img src="/user/data/sae-books-logo.png" alt="SAE Books">
    </a>
    <nav class="primary">
      <a href="#features">Features</a>
      <a href="#editions">Editions</a>
      <a href="#self-host">Self-host</a>
      <a href="#faq">FAQ</a>
      <a href="https://dev.saebooks.com.au">Docs</a>
      <a href="https://discourse.saebooks.com.au">Forum</a>
    </nav>
    <div class="header-spacer"></div>
    <div class="header-actions">
      <div class="theme-switch" role="group" aria-label="Theme">
        <button type="button" data-theme-value="light" aria-pressed="false" aria-label="Light theme" title="Light">
          <svg class="lucide" viewBox="0 0 24 24"><circle cx="12" cy="12" r="4"/><path d="M12 2v2M12 20v2M4.93 4.93l1.41 1.41M17.66 17.66l1.41 1.41M2 12h2M20 12h2M4.93 19.07l1.41-1.41M17.66 6.34l1.41-1.41"/></svg>
        </button>
        <button type="button" data-theme-value="auto" aria-pressed="false" aria-label="Auto theme" title="Auto (matches system)">
          <svg class="lucide" viewBox="0 0 24 24"><rect x="2" y="4" width="20" height="14" rx="2"/><path d="M8 22h8M12 18v4"/></svg>
        </button>
        <button type="button" data-theme-value="dark" aria-pressed="false" aria-label="Dark theme" title="Dark">
          <svg class="lucide" viewBox="0 0 24 24"><path d="M21 12.79A9 9 0 1 1 11.21 3 7 7 0 0 0 21 12.79z"/></svg>
        </button>
      </div>
    <a href="https://app.saebooks.com.au" class="btn btn-primary">Try the demo</a>
    </div>
  </div>
</header>

<section class="hero">
  <div class="container">
    <div class="hero-grid">
      <div>
        <h1>Built for the next 20 years. Evolving, not built on legacy.</h1>
        <p class="lead">SAE Books is an API-first accounting ledger you can build a business on. Every screen is a thin layer over a public REST API &mdash; the same one your scripts, integrations, and partner services hit. Self-hosted, double-entry, AGPL.</p>
        <div class="hero-ctas">
          <a href="https://app.saebooks.com.au" class="btn btn-primary btn-lg">Try the demo
            <svg class="lucide" viewBox="0 0 24 24" style="width:14px;height:14px;"><path d="M5 12h14M13 5l7 7-7 7"/></svg>
          </a>
          <a href="https://dev.saebooks.com.au" class="btn btn-secondary btn-lg">Read the API docs</a>
        </div>
        <div class="hero-meta">
          <span class="pill"><span class="dot"></span>Free Community edition</span>
          <span class="pill">
            <svg class="lucide" viewBox="0 0 24 24" style="width:14px;height:14px;"><path d="M9 19c-5 1.5-5-2.5-7-3m14 6v-3.87a3.37 3.37 0 0 0-.94-2.61c3.14-.35 6.44-1.54 6.44-7A5.44 5.44 0 0 0 20 4.77 5.07 5.07 0 0 0 19.91 1S18.73.65 16 2.48a13.38 13.38 0 0 0-7 0C6.27.65 5.09 1 5.09 1A5.07 5.07 0 0 0 5 4.77a5.44 5.44 0 0 0-1.5 3.78c0 5.42 3.3 6.61 6.44 7A3.37 3.37 0 0 0 9 18.13V22"/></svg>
            AGPLv3 on GitHub
          </span>
          <span class="pill">REST &middot; OpenAPI &middot; Webhooks</span>
        </div>
      </div>
      <div class="hero-screenshot" aria-label="API request preview">
        <div class="hs-chrome">
          <span></span><span></span><span></span>
          <span class="url">POST api.saebooks.com.au/v1/invoices</span>
        </div>
        <div class="hs-body hs-code">
<pre class="hs-req"><span class="hs-c">// Same endpoint your scripts hit. Same one the UI hits.</span>
<span class="hs-k">POST</span> /api/v1/invoices  <span class="hs-c">// HTTP/2</span>
<span class="hs-k">Authorization:</span> Bearer sk_live_…
<span class="hs-k">Idempotency-Key:</span> 0193c8b4-…

{
  <span class="hs-s">"contact_id"</span>: <span class="hs-s">"4f3a…"</span>,
  <span class="hs-s">"date"</span>:       <span class="hs-s">"2026-05-08"</span>,
  <span class="hs-s">"lines"</span>: [
    { <span class="hs-s">"account"</span>: <span class="hs-s">"4-1000"</span>,
      <span class="hs-s">"qty"</span>: <span class="hs-n">8</span>, <span class="hs-s">"price"</span>: <span class="hs-n">185.00</span>,
      <span class="hs-s">"tax_code"</span>: <span class="hs-s">"GST"</span> }
  ]
}</pre>
<pre class="hs-res"><span class="hs-c">// 201 Created &middot; 38 ms</span>
{
  <span class="hs-s">"id"</span>:        <span class="hs-s">"INV-001047"</span>,
  <span class="hs-s">"status"</span>:    <span class="hs-s">"draft"</span>,
  <span class="hs-s">"total"</span>:     <span class="hs-n">1628.00</span>,
  <span class="hs-s">"gst"</span>:       <span class="hs-n">148.00</span>,
  <span class="hs-s">"je_id"</span>:     <span class="hs-s">"j_91f2…"</span>,
  <span class="hs-s">"webhook"</span>:   <span class="hs-s">"invoice.created"</span>
}</pre>
        </div>
      </div>
    </div>
  </div>
</section>

<section class="band" id="why">
  <div class="container">
    <div class="sh">
      <span class="eyebrow brand">Why SAE Books</span>
      <h2>Three reasons. No bullshit.</h2>
    </div>
    <div class="three-up">
      <div class="point">
        <div class="icon">
          <svg class="lucide" viewBox="0 0 24 24" style="width:22px;height:22px;"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg>
        </div>
        <h3>API-first, not GUI-first</h3>
        <p>The web UI is a thin client over a public REST API. Anything you can do in a browser, your scripts can do too &mdash; same endpoints, same auth, same OpenAPI schema. No screen-scraping, no &ldquo;export to CSV and pray&rdquo;.</p>
      </div>
      <div class="point">
        <div class="icon">
          <svg class="lucide" viewBox="0 0 24 24" style="width:22px;height:22px;"><circle cx="18" cy="5" r="3"/><circle cx="6" cy="12" r="3"/><circle cx="18" cy="19" r="3"/><line x1="8.59" y1="13.51" x2="15.42" y2="17.49"/><line x1="15.41" y1="6.51" x2="8.59" y2="10.49"/></svg>
        </div>
        <h3>Service-oriented by default</h3>
        <p>The accounting ledger does one thing well: keeps the books. Document vault, bank-feed relay, lodgement, payroll &mdash; all separate services that talk to it over the API. Swap any of them; the books stay yours.</p>
      </div>
      <div class="point">
        <div class="icon">
          <svg class="lucide" viewBox="0 0 24 24" style="width:22px;height:22px;"><ellipse cx="12" cy="5" rx="9" ry="3"/><path d="M3 5v14a9 3 0 0 0 18 0V5"/><path d="M3 12a9 3 0 0 0 18 0"/></svg>
        </div>
        <h3>Owned by you, forever</h3>
        <p>Your books live in a Postgres database you control. AGPLv3 means the source is yours; full export in CSV, JSON, OFX, QIF, or a complete DB dump. Cancel and your data walks with you &mdash; you never lose access to your own ledger.</p>
      </div>
    </div>
  </div>
</section>

<section id="features">
  <div class="container">
    <div class="sh">
      <span class="eyebrow brand">What&rsquo;s in the box</span>
      <h2>A platform first. A BAS app second.</h2>
      <p>Multi-company ledger, audit trail, period locks, FX. The Australian tax bits sit on top of that &mdash; not the other way round.</p>
    </div>
    <div class="feature-grid">
      <div class="tile">
        <div class="icon"><svg class="lucide" viewBox="0 0 24 24"><polyline points="16 18 22 12 16 6"/><polyline points="8 6 2 12 8 18"/></svg></div>
        <h4>Public REST API</h4>
        <p>Every screen is a thin client over the same OpenAPI-documented endpoints your scripts call. Bearer tokens, webhooks, idempotency keys.</p>
      </div>
      <div class="tile">
        <div class="icon"><svg class="lucide" viewBox="0 0 24 24"><path d="M3 21h18"/><path d="M5 21V7l8-4v18"/><path d="M19 21V11l-6-4"/><path d="M9 9v.01"/><path d="M9 12v.01"/><path d="M9 15v.01"/></svg></div>
        <h4>Multi-company <span class="badge">Pro</span></h4>
        <p>Run multiple entities under one login. Reciprocal journals. Consolidated reports. Row-level isolation, not just a filter.</p>
      </div>
      <div class="tile">
        <div class="icon"><svg class="lucide" viewBox="0 0 24 24"><rect x="3" y="11" width="18" height="11" rx="2" ry="2"/><path d="M7 11V7a5 5 0 0 1 10 0v4"/></svg></div>
        <h4>Period locks &amp; audit ledger</h4>
        <p>Close a period, lock it, audit it. Every change to a posted journal leaves a tamper-evident trail.</p>
      </div>
      <div class="tile">
        <div class="icon"><svg class="lucide" viewBox="0 0 24 24"><path d="m16 3 4 4-4 4"/><path d="M20 7H4"/><path d="m8 21-4-4 4-4"/><path d="M4 17h16"/></svg></div>
        <h4>FX revaluation <span class="badge">Pro</span></h4>
        <p>Multi-currency posting with end-of-period revaluation. ECB and RBA daily rates included.</p>
      </div>
      <div class="tile">
        <div class="icon"><svg class="lucide" viewBox="0 0 24 24"><path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"/><circle cx="9" cy="7" r="4"/><path d="M22 21v-2a4 4 0 0 0-3-3.87"/><path d="M16 3.13a4 4 0 0 1 0 7.75"/></svg></div>
        <h4>STP payroll <span class="badge">Business</span></h4>
        <p>Single Touch Payroll lodgement, super, payslips. STP Phase 2 ready.</p>
      </div>
      <div class="tile">
        <div class="icon"><svg class="lucide" viewBox="0 0 24 24"><path d="M14 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V8z"/><path d="M14 2v6h6"/><path d="m9 15 2 2 4-4"/></svg></div>
        <h4>BAS e-lodgement <span class="badge ent">Enterprise</span></h4>
        <p>Generate the BAS, review the worksheet, lodge it. Settlement journals are automatic. Direct ATO/SBR submission ships with our DSP-accredited Enterprise tier.</p>
      </div>
      <div class="tile">
        <div class="icon"><svg class="lucide" viewBox="0 0 24 24"><line x1="3" y1="22" x2="21" y2="22"/><line x1="6" y1="18" x2="6" y2="11"/><line x1="10" y1="18" x2="10" y2="11"/><line x1="14" y1="18" x2="14" y2="11"/><line x1="18" y1="18" x2="18" y2="11"/><polygon points="12 2 20 7 4 7"/></svg></div>
        <h4>Bank feeds <span class="badge ent">Enterprise</span></h4>
        <p>SISS/ACSISS-backed daily feeds for every major Australian bank. Delivered via our relay service while we onboard new tenants under the data-aggregator agreement.</p>
      </div>
      <div class="tile">
        <div class="icon"><svg class="lucide" viewBox="0 0 24 24"><circle cx="11" cy="11" r="8"/><path d="m21 21-4.3-4.3"/></svg></div>
        <h4>ABR lookup &amp; fixed assets <span class="badge">Business</span></h4>
        <p>One-field ABN/ACN lookup auto-fills contacts. Fixed asset register with depreciation schedules, disposals, and write-downs &mdash; both wired through the public API.</p>
      </div>
    </div>
  </div>
</section>

<section class="band" id="editions">
  <div class="container">
    <div class="sh">
      <span class="eyebrow brand">Pricing</span>
      <h2>One codebase. Pick the licence that fits.</h2>
      <p>All paid tiers are self-hosted unless you choose hosted-by-us. Same AGPLv3 source, runtime-flagged for the features you need.</p>
    </div>
    <div class="tiers-wrap">
      <div class="tiers-grid">

        <div class="tier">
          <div class="tier-name">Community</div>
          <div class="tier-price"><span class="free">Free</span></div>
          <div class="tier-tagline">Single-company self-hosted. No licence key, no nag screens.</div>
          <a href="https://github.com/saebooks/saebooks" class="btn btn-secondary">Download from GitHub</a>
          <ul class="tier-feats">
            <li class="group">Core books</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Chart of accounts, journals, GL</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Sales, purchases, contacts</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Bank reconcile</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>GST/BAS report generation</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Full export (CSV, JSON, OFX, DB dump)</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Immutable audit ledger</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Postgres &amp; SQLite</li>
          </ul>
          <div class="tier-foot">AGPLv3. Forum support. Bring-your-own infra.</div>
        </div>

        <div class="tier popular">
          <div class="tier-name">Business</div>
          <div class="tier-price">
            <span class="amount">$49</span>
            <span class="per">/ month, or $490 / year &mdash; AUD</span>
          </div>
          <div class="tier-tagline">For sole traders and small teams who lodge BAS themselves.</div>
          <a href="https://app.saebooks.com.au/signup?plan=business" class="btn btn-primary">Get started &mdash; Business</a>
          <p class="tier-cta-note" style="margin-top:6px;font-size:0.8rem;opacity:0.75;">Free account required. No credit card on sign-up.</p>
          <ul class="tier-feats">
            <li class="group">Everything in Community, plus</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>STP Phase 2 payroll</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>ABR lookup, in-app</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Fixed asset register</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Period locks</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Webhooks &amp; idempotent API tokens</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Email support, business hours</li>
          </ul>
          <div class="tier-foot">Up to 3 users. Single company. Cancel anytime.</div>
        </div>

        <div class="tier">
          <div class="tier-name">Pro</div>
          <div class="tier-price">
            <span class="amount">$99</span>
            <span class="per">/ month, or $990 / year &mdash; AUD</span>
          </div>
          <div class="tier-tagline">For bookkeepers, growing teams, and anyone running payroll.</div>
          <a href="https://app.saebooks.com.au/signup?plan=pro" class="btn btn-primary">Get started &mdash; Pro</a>
          <p class="tier-cta-note" style="margin-top:6px;font-size:0.8rem;opacity:0.75;">Free account required. No credit card on sign-up.</p>
          <ul class="tier-feats">
            <li class="group">Everything in Business, plus</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Multi-company / intercompany</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>FX revaluation</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Open Journal / Hybrid audit modes</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Higher API rate limits &amp; bulk endpoints</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Signed LTS releases</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Priority email support</li>
          </ul>
          <div class="tier-foot">Unlimited users. Up to 10 companies. Cancel anytime.</div>
        </div>

        <div class="tier enterprise">
          <div class="tier-name">Enterprise</div>
          <div class="tier-price">
            <span class="per" style="font-size:13px;">From</span>
            <span class="amount">$200</span>
            <span class="per">/ month</span>
          </div>
          <div class="tier-tagline">Custom-built solutions. We tailor SAE Books to your operation.</div>
          <a href="https://app.saebooks.com.au/contact?topic=enterprise" class="btn btn-secondary">Talk to us</a>
          <ul class="tier-feats">
            <li class="group">Everything in Pro, plus</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>BAS e-lodgement (early access)</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Bank feeds (SISS / ACSISS) &mdash; early access</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Custom integrations &amp; modules</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Migration from QBO / Xero / MYOB</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Dedicated hosted tenant or on-prem</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>SSO with your IdP (SAML/OIDC)</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>SLA-backed support &amp; named upgrade window</li>
            <li><svg viewBox="0 0 24 24"><polyline points="20 6 9 17 4 12"/></svg>Source escrow on request</li>
          </ul>
          <div class="tier-foot">Scoped per engagement. Quoted, not subscribed.</div>
        </div>

      </div>
      <p class="meta" style="margin-top:24px;text-align:center;">All paid features ship in the same AGPL binary, gated by a licence-key flag. Self-compile and flip the flag &mdash; that&rsquo;s what AGPL means.</p>
    </div>
  </div>
</section>

<section>
  <div class="container">
    <div class="sh">
      <span class="eyebrow brand">Anatomy</span>
      <h2>An accounting core. A constellation of services.</h2>
      <p>The ledger does the books. Everything else &mdash; the document vault, bank feeds, lodgement &mdash; is a separate service that talks to it over the API. Replace any of them; the books stay yours.</p>
    </div>
    <div class="shots-row">
      <div class="shot">
        <div class="shot-mock shot-mock-openapi">
          <div class="sm-row"><span class="sm-method get">GET</span><span class="sm-path">/api/v1/health</span></div>
          <div class="sm-row"><span class="sm-method get">GET</span><span class="sm-path">/api/v1/contacts</span></div>
          <div class="sm-row sm-expanded"><span class="sm-method post">POST</span><span class="sm-path">/api/v1/contacts</span></div>
          <div class="sm-row sm-param"><span class="sm-key">name</span> string<span class="sm-req">required</span></div>
          <div class="sm-row sm-param"><span class="sm-key">abn</span> string &nbsp; <span class="sm-key">email</span> string</div>
          <div class="sm-row"><span class="sm-method get">GET</span><span class="sm-path">/api/v1/invoices</span></div>
          <div class="sm-row"><span class="sm-method post">POST</span><span class="sm-path">/api/v1/invoices</span></div>
          <div class="sm-row"><span class="sm-method del">DEL</span><span class="sm-path">/api/v1/invoices/{id}</span></div>
        </div>
        <div class="shot-cap"><h4>OpenAPI explorer</h4><p>Browse, try, and copy every endpoint at <a href="https://dev.saebooks.com.au">dev.saebooks.com.au</a>. Bearer-token auth, idempotency keys, page cursors.</p></div>
      </div>
      <div class="shot">
        <div class="shot-mock shot-mock-webhooks">
          <div class="sm-row"><span class="sm-time">14:32:08</span><span class="sm-evt">invoice.created</span><span class="sm-id">INV-001047</span><span class="sm-status ok">200</span><span class="sm-lat">38ms</span></div>
          <div class="sm-row"><span class="sm-time">14:31:55</span><span class="sm-evt">bill.approved</span><span class="sm-id">BL-000812</span><span class="sm-status ok">200</span><span class="sm-lat">24ms</span></div>
          <div class="sm-row"><span class="sm-time">14:31:42</span><span class="sm-evt">payment.matched</span><span class="sm-id">PY-002201</span><span class="sm-status ok">200</span><span class="sm-lat">19ms</span></div>
          <div class="sm-row"><span class="sm-time">14:30:15</span><span class="sm-evt">invoice.created</span><span class="sm-id">retry 1/5</span><span class="sm-status warn">502</span><span class="sm-lat">82ms</span></div>
          <div class="sm-row"><span class="sm-time">14:29:58</span><span class="sm-evt">invoice.created</span><span class="sm-id">INV-001045</span><span class="sm-status ok">200</span><span class="sm-lat">41ms</span></div>
          <div class="sm-row"><span class="sm-time">14:29:30</span><span class="sm-evt">contact.updated</span><span class="sm-id">4f3a&hellip;</span><span class="sm-status ok">200</span><span class="sm-lat">12ms</span></div>
          <div class="sm-row"><span class="sm-time">14:28:12</span><span class="sm-evt">je.posted</span><span class="sm-id">j_91f2&hellip;</span><span class="sm-status ok">200</span><span class="sm-lat">15ms</span></div>
        </div>
        <div class="shot-cap"><h4>Webhook deliveries</h4><p>Subscribe to <code>invoice.created</code>, <code>bill.approved</code>, <code>payment.matched</code>. Signed payloads, retries with exponential backoff, full delivery log.</p></div>
      </div>
      <div class="shot">
        <div class="shot-mock shot-mock-audit">
          <div class="sm-entry">
            <div class="sm-avatar">RS</div>
            <div class="sm-entry-body">
              <div class="sm-entry-h"><span class="sm-actor">Richard Sauer</span><span class="sm-stamp">14:32:08</span></div>
              <div class="sm-act">Updated INV-001047 &middot; status: <span class="sm-diff-old">draft</span> <span class="sm-diff-new">approved</span></div>
            </div>
          </div>
          <div class="sm-entry">
            <div class="sm-avatar api">API</div>
            <div class="sm-entry-body">
              <div class="sm-entry-h"><span class="sm-actor">curl/8.5</span><span class="sm-stamp">14:31:55</span></div>
              <div class="sm-act">Created BL-000812 via <code>POST /api/v1/bills</code><br><span class="sm-stamp">idempotency 0193c8b4&hellip;</span></div>
            </div>
          </div>
          <div class="sm-entry">
            <div class="sm-avatar bot">JE</div>
            <div class="sm-entry-body">
              <div class="sm-entry-h"><span class="sm-actor">period-close-bot</span><span class="sm-stamp">14:28:12</span></div>
              <div class="sm-act">Posted JE j_91f2 (period 2026-Q1, locked)</div>
            </div>
          </div>
        </div>
        <div class="shot-cap"><h4>Audit ledger</h4><p>Every change &mdash; UI or API &mdash; tagged with actor, request id, before/after diff. Period-locked rows are immutable end-to-end.</p></div>
      </div>
    </div>
  </div>
</section>

<section class="subtle" id="self-host">
  <div class="container">
    <div class="sh">
      <span class="eyebrow brand">Run it your way</span>
      <h2>Self-host or hosted by us.</h2>
    </div>
    <div class="split">
      <div class="split-card">
        <div class="icon" style="width:32px;height:32px;"><svg class="lucide" viewBox="0 0 24 24"><rect x="2" y="2" width="20" height="8" rx="2" ry="2"/><rect x="2" y="14" width="20" height="8" rx="2" ry="2"/><line x1="6" y1="6" x2="6.01" y2="6"/><line x1="6" y1="18" x2="6.01" y2="18"/></svg></div>
        <h3>Run it yourself</h3>
        <p><code>docker compose up</code>. Bring your own Postgres or use the bundled SQLite for one-person setups. Authentik or any OIDC provider for SSO. Ships with a backup runbook.</p>
        <pre>$ docker compose pull
$ docker compose up -d
&#10003; saebooks-app started on :8080
&#10003; postgres healthy
&#10003; migrations applied (rev 0042)</pre>
        <a href="https://dev.saebooks.com.au/install" class="btn btn-secondary">Read the install guide
          <svg class="lucide" viewBox="0 0 24 24" style="width:14px;height:14px;"><path d="M5 12h14M13 5l7 7-7 7"/></svg>
        </a>
      </div>
      <div class="split-card" style="background: var(--brand-navy); color: #fff; border-color: var(--brand-navy);">
        <div class="icon" style="width:32px;height:32px;color:#fff;"><svg class="lucide" viewBox="0 0 24 24"><path d="M17.5 19H9a7 7 0 1 1 6.71-9h1.79a4.5 4.5 0 1 1 0 9Z"/></svg></div>
        <h3 style="color:#fff;">Or let us run it</h3>
        <p style="color: rgba(255,255,255,0.85);">Same code, signed releases, hourly off-site backup, Authentik SSO, Australian data residency. Pay monthly or annually. Cancel and take a full DB dump with you.</p>
        <ul style="color:rgba(255,255,255,0.85);font-size:14px;line-height:1.9;list-style:none;padding:0;margin:0 0 20px;">
          <li>&middot; Hourly snapshot &middot; 30-day retention</li>
          <li>&middot; Cairns, QLD data residency</li>
          <li>&middot; Authentik SSO included</li>
          <li>&middot; Migration assistance from QBO / Xero / MYOB</li>
        </ul>
        <a href="#editions" class="btn" style="background:#fff;color:var(--brand-navy);">See hosted plans
          <svg class="lucide" viewBox="0 0 24 24" style="width:14px;height:14px;"><path d="M5 12h14M13 5l7 7-7 7"/></svg>
        </a>
      </div>
    </div>
  </div>
</section>

<section id="faq">
  <div class="container">
    <div class="sh">
      <span class="eyebrow brand">FAQ</span>
      <h2>The questions worth asking.</h2>
    </div>
    <div class="faq-wrap">
      <details class="faq" open>
        <summary>What does &ldquo;API-first&rdquo; actually buy me?<span class="chev"><svg class="lucide" viewBox="0 0 24 24" style="width:18px;height:18px;"><polyline points="6 9 12 15 18 9"/></svg></span></summary>
        <p>Every action in the UI is a documented REST call. Want to push 200 invoices from your job-management system? Hit <code>POST /api/v1/invoices</code>. Want a webhook when a bill is approved? Subscribe. Want to retire the UI entirely and drive it from a script? You can. The accounting ledger is the product; the screens are one of many possible clients. OpenAPI schema lives at <a href="https://dev.saebooks.com.au">dev.saebooks.com.au</a>.</p>
      </details>
      <details class="faq">
        <summary>What does AGPLv3 mean for my business?<span class="chev"><svg class="lucide" viewBox="0 0 24 24" style="width:18px;height:18px;"><polyline points="6 9 12 15 18 9"/></svg></span></summary>
        <p>Run it however you want &mdash; internally, with clients, anywhere. The licence only kicks in if you modify the code and offer the modified version as a network service to others. Most users will never trigger it. Hosting it for your own clients is fine; selling a hosted SAE Books fork as a SaaS without contributing back is not.</p>
      </details>
      <details class="faq">
        <summary>Can I get my data out?<span class="chev"><svg class="lucide" viewBox="0 0 24 24" style="width:18px;height:18px;"><polyline points="6 9 12 15 18 9"/></svg></span></summary>
        <p>Always. Export to CSV, JSON, OFX, QIF, or a full Postgres dump from the Settings &rarr; Export screen. Importable into a fresh instance with one command. Data portability is a first-class feature, not a goodbye gift.</p>
      </details>
      <details class="faq">
        <summary>Is it actually compliant with AU tax?<span class="chev"><svg class="lucide" viewBox="0 0 24 24" style="width:18px;height:18px;"><polyline points="6 9 12 15 18 9"/></svg></span></summary>
        <p>Yes &mdash; the chart of accounts, tax codes, and BAS labels ship from the Odoo AU localisation. <strong>STP Phase 2 payroll</strong> is included from the Business tier and up. <strong>BAS e-lodgement</strong> and <strong>bank feeds</strong> are gated to Enterprise while we complete ATO DSP accreditation and the data-aggregator agreement; until then BAS is &ldquo;generate, review, lodge via the ATO portal&rdquo;. The accounting core itself is fully AU-compliant on every tier.</p>
      </details>
      <details class="faq">
        <summary>How do upgrades work?<span class="chev"><svg class="lucide" viewBox="0 0 24 24" style="width:18px;height:18px;"><polyline points="6 9 12 15 18 9"/></svg></span></summary>
        <p>Tagged Docker images. <code>docker compose pull &amp;&amp; up -d</code>. Migrations run on boot. We test every migration against a parallel-run copy of Richard&rsquo;s own books before publishing &mdash; so if it eats your data, it eats his first.</p>
      </details>
      <details class="faq">
        <summary>What if something goes wrong?<span class="chev"><svg class="lucide" viewBox="0 0 24 24" style="width:18px;height:18px;"><polyline points="6 9 12 15 18 9"/></svg></span></summary>
        <p>Community: GitHub issues + the forum at <a href="https://discourse.saebooks.com.au">discourse.saebooks.com.au</a>. Mostly self-supported. Business and Pro: priority email, signed LTS branches, named upgrade window. Enterprise: SLA-backed, named contacts, agreed response times. For all tiers: the data is a Postgres database, so any DBA on the planet can help you in a pinch. Nothing is locked in a vendor format.</p>
      </details>
    </div>
  </div>
</section>

<footer class="site">
  <div class="container">
    <div class="foot-grid">
      <div class="foot-col foot-brand">
        <a href="/" class="wordmark"><img src="/user/data/sae-books-logo.png" alt="SAE Books" style="height:40px;"></a>
        <p class="blurb">An API-first, self-hosted accounting ledger for Australian small business. AGPLv3, owned by you. STP from Business; BAS e-lodgement and bank feeds from Enterprise as we onboard.</p>
      </div>
      <div class="foot-col">
        <h5>Product</h5>
        <ul>
          <li><a href="https://app.saebooks.com.au">Try the demo</a></li>
          <li><a href="#editions">Pricing &amp; plans</a></li>
          <li><a href="https://app.saebooks.com.au/contact?topic=enterprise">Talk to us (Enterprise)</a></li>
          <li><a href="https://github.com/saebooks/saebooks/blob/main/ROADMAP.md">Roadmap</a></li>
        </ul>
      </div>
      <div class="foot-col">
        <h5>Build</h5>
        <ul>
          <li><a href="https://dev.saebooks.com.au">Docs</a></li>
          <li><a href="https://discourse.saebooks.com.au">Forum</a></li>
          <li><a href="https://github.com/saebooks/saebooks">GitHub</a></li>
          <li><a href="https://github.com/saebooks/saebooks/blob/main/CHANGELOG.md">Changelog</a></li>
        </ul>
      </div>
      <div class="foot-col">
        <h5>Company</h5>
        <ul>
          <li><a href="https://sauer.com.au">SAE Engineering</a></li>
          <li><a href="https://app.saebooks.com.au/contact">Contact</a></li>
          <li><a href="https://sauer.com.au/privacy">Privacy</a></li>
          <li><a href="https://www.gnu.org/licenses/agpl-3.0.en.html">Licence (AGPLv3)</a></li>
        </ul>
      </div>
    </div>
    <div class="foot-bottom">
      <span>&copy; 2026 Sauer Pty Ltd &middot; ABN 87 744 586 592 &middot; ACN 683 275 756 &middot; Cairns, QLD</span>
      <span>Source available under <a href="https://www.gnu.org/licenses/agpl-3.0.en.html">AGPLv3</a>.</span>
    </div>
  </div>
</footer>

<div class="mobile-cta">
  <a href="https://app.saebooks.com.au" class="btn btn-primary">Try the demo</a>
  <a href="#editions" class="btn btn-secondary">See pricing</a>
</div>

<script>
  (function() {
    var root = document.documentElement;
    var STORAGE_KEY = 'sae-books-theme';
    var mql = window.matchMedia('(prefers-color-scheme: dark)');

    function applyTheme(choice) {
      if (choice === 'auto') {
        root.removeAttribute('data-theme');
      } else {
        root.setAttribute('data-theme', choice);
      }
      document.querySelectorAll('.theme-switch button[data-theme-value]').forEach(function(b) {
        b.setAttribute('aria-pressed', String(b.dataset.themeValue === choice));
      });
    }

    function getStoredChoice() {
      var v = localStorage.getItem(STORAGE_KEY);
      return (v === 'light' || v === 'dark') ? v : 'auto';
    }

    applyTheme(getStoredChoice());

    document.querySelectorAll('.theme-switch button[data-theme-value]').forEach(function(btn) {
      btn.addEventListener('click', function() {
        var choice = btn.dataset.themeValue;
        if (choice === 'auto') localStorage.removeItem(STORAGE_KEY);
        else localStorage.setItem(STORAGE_KEY, choice);
        applyTheme(choice);
      });
    });

    if (mql.addEventListener) {
      mql.addEventListener('change', function() {
        if (getStoredChoice() === 'auto') applyTheme('auto');
      });
    }
  })();
</script>
