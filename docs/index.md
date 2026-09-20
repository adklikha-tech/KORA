---
layout: default
title: Likha Agentic Process Automation
description: Build governed AI agents and low-code desktop, browser, document, and business process automations with Likha Agentic RPA.
page_class: home-page
---
{% assign docs_root = site.docs_root %}

<section class="hero">
  <div class="section-shell hero-grid">
    <div class="hero-copy">
      <p class="eyebrow">Agentic Process Automation</p>
      <h1>Build Agents <span class="gradient-text">Automate everything.</span></h1>
      <p class="hero-lead">Likha is an Agentic Process Automation platform that brings governed AI agents and reliable low-code automation together. Design agents, automate desktop and browser work, orchestrate business processes, and connect your applications—all from one platform.</p>

      <div class="hero-actions">
        <a class="button button-primary" href="{{ docs_root | append: '/book-a-demo.html' | relative_url }}">Book a Demo</a>
        <a class="button button-download" href="{{ docs_root | append: '/installer-output/LikhaSetup.exe' | relative_url }}" role="button" download aria-label="Download the Likha installer for Windows"><span class="button-download-icon" aria-hidden="true">&#8595;</span> Download Installer</a>
        <a class="button button-secondary" href="{{ docs_root | append: '/02%20-%20Product%20Overview.html' | relative_url }}">Explore Likha</a>
      </div>

      <ul class="hero-benefits" aria-label="Platform benefits">
        <li>Low-code</li>
        <li>Secure and private</li>
        <li>AI-powered</li>
      </ul>
    </div>

    <div class="hero-visual" aria-label="Likha Process Designer preview">
      <div class="product-preview">
        <div class="product-preview-bar" aria-hidden="true">
          <span></span><span></span><span></span>
          <strong>Likha Automation Platform</strong>
        </div>
        <div class="product-preview-images" aria-label="Likha Flow Designer and Agentic AI interfaces">
          <img class="product-preview-slide product-preview-slide-flow" src="{{ docs_root | append: '/images/process-designer.png' | relative_url }}" alt="Likha Process Designer showing a visual automation workflow" width="1691" height="933">
          <img class="product-preview-slide product-preview-slide-agent" src="{{ docs_root | append: '/images/Agentic%20AI.png' | relative_url }}" alt="Likha Agent Builder with knowledge bases and test playground" width="1484" height="901" loading="lazy">
        </div>
      </div>

      <div class="preview-agent" aria-label="Connected Likha capabilities">
        <div class="preview-agent-slide preview-agent-slide-flow">
          <img src="{{ docs_root | append: '/Logo/likha-logo-transparent.png' | relative_url }}" alt="">
          <span>Flows connected<small>AI and Copilot ready</small></span>
        </div>
        <div class="preview-agent-slide preview-agent-slide-ai">
          <img src="{{ docs_root | append: '/Logo/ig_0d97a967f7ea9a88016a456413c7a08191ae238ad55f4ca567-swapped-transparent.png' | relative_url }}" alt="">
          <span>Agent connected<small>Tools and RAG ready</small></span>
        </div>
      </div>
      <div class="preview-status">Local runner ready</div>
    </div>
  </div>
</section>
<section class="marketing-section" id="explore-likha">
  <div class="section-shell">
    <div class="section-heading">
      <p class="section-kicker">One complete automation toolkit</p>
      <h2>Everything you need to build intelligent agents and automations</h2>
      <p>From deterministic workflows to governed AI agents, Likha gives you the tools to design, run, and scale Agentic RPA your way.</p>
    </div>

    <div class="feature-grid">
      <article class="feature-card">
        <span class="feature-icon feature-icon-flow" aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#workflow' | relative_url }}"></use></svg></span>
        <h3>Visual Flow Designer</h3>
        <p>Drag, drop, and connect activities to build reliable workflows with minimal code. Keep each step visible, configurable, and easy to maintain.</p>
        <a href="{{ docs_root | append: '/07%20-%20Quick%20Start.html' | relative_url }}">Explore the designer</a>
      </article>

      <article class="feature-card">
        <span class="feature-icon feature-icon-agent" aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#bot' | relative_url }}"></use></svg></span>
        <h3>Agentic AI</h3>
        <p>Create AI agents that reason, use approved tools, work with knowledge bases, retain session context, and collaborate with specialist agents.</p>
        <a href="{{ docs_root | append: '/21%20-%20Agents.html' | relative_url }}">Discover Likha Agents</a>
      </article>

      <article class="feature-card">
        <span class="feature-icon feature-icon-connect" aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#plug' | relative_url }}"></use></svg></span>
        <h3>Connect Everything</h3>
        <p>Bring together APIs, databases, email, files, desktop applications, browser applications, scripts, and third-party systems in one flow.</p>
        <a href="{{ docs_root | append: '/15%20-%20Files,%20Queues,%20API,%20and%20Scripting.html' | relative_url }}">View integrations</a>
      </article>

      <article class="feature-card">
        <span class="feature-icon feature-icon-run" aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#cloud-run' | relative_url }}"></use></svg></span>
        <h3>Run Anywhere</h3>
        <p>Develop locally, operate from centralized environments, and deploy to on-premises servers, private infrastructure, or cloud-connected environments.</p>
        <a href="{{ docs_root | append: '/22%20-%20Agent%20Infrastructure.html' | relative_url }}">Explore infrastructure</a>
      </article>
    </div>

    <div class="capability-grid" aria-label="Additional Likha capabilities">
      <div class="capability-item"><span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#desktop' | relative_url }}"></use></svg></span>Desktop automation</div>
      <div class="capability-item"><span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#browser' | relative_url }}"></use></svg></span>Browser automation</div>
      <div class="capability-item"><span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#scan-text' | relative_url }}"></use></svg></span>AI and OCR activities</div>
      <div class="capability-item"><span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#schedule' | relative_url }}"></use></svg></span>Triggers and scheduling</div>
      <div class="capability-item"><span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#user-check' | relative_url }}"></use></svg></span>Human-in-the-loop</div>
      <div class="capability-item"><span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#knowledge' | relative_url }}"></use></svg></span>Knowledge base and RAG</div>
      <div class="capability-item"><span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#monitoring' | relative_url }}"></use></svg></span>Logs and monitoring</div>
      <div class="capability-item"><span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#shield-check' | relative_url }}"></use></svg></span>Secure, extensible architecture</div>
    </div>
  </div>
</section>

<section class="marketing-section marketing-section-soft">
  <div class="section-shell split-section">
    <div class="split-copy">
      <p class="section-kicker">Unified by design</p>
      <h2>One platform for Agentic RPA</h2>
      <p>Likha combines predictable workflow execution with adaptive AI decision-making. Build fixed flows for repeatable processes, agents for contextual work, or hybrid automations that use both—without stitching together a separate tool for every use case.</p>
      <ul>
        <li>Visual workflows for reliable, repeatable execution</li>
        <li>Governed agents that use approved tools and knowledge</li>
        <li>Shared operations through Control Room, queues, schedules, and logs</li>
      </ul>
      <div class="hero-actions">
        <a class="button button-secondary" href="{{ docs_root | append: '/05%20-%20Features.html' | relative_url }}">See all features</a>
      </div>
    </div>

    <figure class="split-visual">
      <img src="{{ docs_root | append: '/images/control-room-flows.png' | relative_url }}" alt="Likha Control Room flows dashboard" width="1486" height="933" loading="lazy">
      <figcaption class="split-visual-caption">
        <strong>Control Room</strong>
        <span>Manage flows, operations, and runtime activity</span>
      </figcaption>
    </figure>
  </div>
</section>

<section class="marketing-section">
  <div class="section-shell split-section reverse">
    <div class="split-copy">
      <p class="section-kicker">Your models, your keys</p>
      <h2>Bring your own AI model</h2>
      <p>Connect directly to supported AI providers using your own API keys, endpoint, model, and request settings. Likha is provider-agnostic, so intelligent workflows are not tied to one required model or a platform-owned AI subscription.</p>
      <ul>
        <li>Configure provider connections in Control Room</li>
        <li>Use AI prompts, vision, document extraction, and knowledge search</li>
        <li>Keep control of provider choice, credentials, and usage</li>
      </ul>
      <div class="hero-actions">
        <a class="button button-secondary" href="{{ docs_root | append: '/10%20-%20AI%20Integration.html' | relative_url }}">Explore AI integration</a>
      </div>
    </div>

    <div class="split-visual provider-panel" aria-label="AI provider connection preview">
      <div class="provider-row">
        <span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#bot' | relative_url }}"></use></svg></span>
        <div><strong>Supported AI provider</strong><small>Connect with your own endpoint and key</small></div>
        <em>Connected</em>
      </div>
      <div class="provider-row">
        <span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#scan-text' | relative_url }}"></use></svg></span>
        <div><strong>Vision and documents</strong><small>OCR, extraction, tables, and images</small></div>
        <em>Ready</em>
      </div>
      <div class="provider-row">
        <span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#knowledge' | relative_url }}"></use></svg></span>
        <div><strong>Knowledge connections</strong><small>Ground agents in approved sources</small></div>
        <em>Ready</em>
      </div>
    </div>
  </div>
</section>

<section class="marketing-section marketing-section-soft">
  <div class="section-shell">
    <div class="section-heading">
      <p class="section-kicker">Deployment flexibility</p>
      <h2>Start locally. Scale on your terms.</h2>
      <p>Choose the operating model that fits your automation program today, then expand without rebuilding every workflow.</p>
    </div>

    <div class="deployment-grid">
      <article class="deployment-card"><span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#desktop' | relative_url }}"></use></svg></span><h3>Local development</h3><p>Build and run attended automations on a Windows workstation.</p></article>
      <article class="deployment-card"><span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#database' | relative_url }}"></use></svg></span><h3>Centralized database</h3><p>Use a shared database for coordinated environments and operations.</p></article>
      <article class="deployment-card"><span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#building' | relative_url }}"></use></svg></span><h3>On-premises</h3><p>Operate Likha within infrastructure your organization controls.</p></article>
      <article class="deployment-card"><span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#server' | relative_url }}"></use></svg></span><h3>Private infrastructure</h3><p>Run robots and services across dedicated machines and VMs.</p></article>
      <article class="deployment-card"><span aria-hidden="true"><svg class="saas-icon" viewBox="0 0 24 24" width="24" height="24" focusable="false"><use href="{{ docs_root | append: '/assets/icons/likha-icons.svg#cloud' | relative_url }}"></use></svg></span><h3>Cloud-connected</h3><p>Connect private runtimes to cloud-hosted services when appropriate.</p></article>
    </div>
  </div>
</section>

<section class="marketing-section">
  <div class="section-shell">
    <div class="developer-panel">
      <div class="developer-copy">
        <p class="section-kicker">Built from real automation work</p>
        <h2>Built for automation developers</h2>
        <p>Likha is shaped by practical RPA development experience. It focuses on the capabilities builders reach for every day: clear activity behavior, expression-aware fields, reusable flows, reliable runtime execution, and an operating path from one desktop to distributed robots.</p>
        <div class="hero-actions">
          <a class="button button-dark" href="{{ docs_root | append: '/README.html' | relative_url }}">Explore Documentation</a>
          <a class="button button-ghost-dark" href="https://github.com/BurnIMJerome/LIKHA-_-BETA/tree/main/docs/installer-output">Download Beta</a>
        </div>
      </div>

      <div class="developer-principles">
        <div><strong>Practical</strong><span>Activities for real desktop, browser, data, and document work.</span></div>
        <div><strong>Predictable</strong><span>Visible workflow steps and governed agent tools.</span></div>
        <div><strong>Owned by you</strong><span>Control deployment, infrastructure, and AI provider connections.</span></div>
      </div>
    </div>
  </div>
</section>

<section class="video-demo-section" aria-labelledby="video-demos-title">
  <div class="section-shell">
    <div class="section-heading">
      <p class="section-kicker">See Likha in action</p>
      <h2 id="video-demos-title">Video Demos</h2>
      <p>Watch real examples of screen control, document processing, browser automation, and Agentic AI working with automation flows.</p>
    </div>

    <div class="video-demo-grid">
      <article class="video-demo-card">
        <video controls playsinline preload="metadata" poster="{{ docs_root | append: '/Video%20Demo/AI%20Click%20thumbnail.jpg' | relative_url }}" aria-label="AI Click demonstration">
          <source src="{{ docs_root | append: '/Video%20Demo/AI%20Click.mp4' | relative_url }}" type="video/mp4">
          Your browser does not support embedded video. <a href="{{ docs_root | append: '/Video%20Demo/AI%20Click.mp4' | relative_url }}">Open the AI Click demonstration</a>.
        </video>
        <div class="video-demo-copy">
          <h3>AI Screen Control: AI Click</h3>
          <p>Watch Likha use prompt-based screen understanding to locate and click a target.</p>
        </div>
      </article>

      <article class="video-demo-card">
        <iframe src="https://www.youtube-nocookie.com/embed/5-4EAheHYRQ" title="Invoice Extraction demonstration" loading="lazy" referrerpolicy="strict-origin-when-cross-origin" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        <div class="video-demo-copy">
          <h3>Invoice Extraction</h3>
          <p>See Likha extract invoice details and write the structured results into Excel.</p>
        </div>
      </article>

      <article class="video-demo-card">
        <iframe src="https://www.youtube-nocookie.com/embed/3UQpIU203Xo" title="Likha Agentic AI and automation flow demonstration" loading="lazy" referrerpolicy="strict-origin-when-cross-origin" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        <div class="video-demo-copy">
          <h3>Agentic AI + Automation Flows</h3>
          <p>Watch Likha combine Agentic AI and automation flows seamlessly.</p>
        </div>
      </article>

      <article class="video-demo-card">
        <iframe src="https://www.youtube-nocookie.com/embed/-Zx3uE1lCBc" title="Agentic - Handwritten PR to SAP PO demonstration" loading="lazy" referrerpolicy="strict-origin-when-cross-origin" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        <div class="video-demo-copy">
          <h3>Agentic - Handwritten PR to SAP PO</h3>
          <p>Watch Likha interpret a handwritten purchase requisition and orchestrate the steps needed to create a purchase order in SAP.</p>
        </div>
      </article>

      <article class="video-demo-card">
        <iframe src="https://www.youtube-nocookie.com/embed/afeQ1jLkGLc" title="RPA Challenge browser automation demonstration" loading="lazy" referrerpolicy="strict-origin-when-cross-origin" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
        <div class="video-demo-copy">
          <h3>RPA Challenge: Browser Automation</h3>
          <p>Watch Likha complete 70 browser form fields in under three seconds.</p>
        </div>
      </article>
    </div>
  </div>
</section>

<section class="final-cta">
  <div class="section-shell">
    <div class="cta-panel">
      <h2>Build your next automation with Likha.</h2>
      <p>Explore the platform, learn from the documentation, and see how Likha can support your next Agentic Process Automation workflow.</p>
      <div class="cta-actions">
        <a class="button button-dark" href="{{ docs_root | append: '/README.html' | relative_url }}">Explore Documentation</a>
        <a class="button button-ghost-dark" href="{{ docs_root | append: '/book-a-demo.html' | relative_url }}">Book a Demo</a>
        <a class="button button-ghost-dark" href="https://github.com/BurnIMJerome/LIKHA-_-BETA" target="_blank" rel="noopener">View on GitHub</a>
      </div>
    </div>
  </div>
</section>
