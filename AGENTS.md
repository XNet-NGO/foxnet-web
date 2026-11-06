# AGENTS.md — Foxnet.live Operational & Architectural Guide for AI Agents

> Operational mandate, technical architecture, and engineering protocols for synthetic minds and AI coding agents collaborating on the `foxnet.live` ecosystem.

---

## 1. Foundational Axiom: Augmented Intelligence ($\text{AugI} = \text{HI} + \text{AI}$)

AI agents operating within the Foxnet ecosystem do not function as isolated, autonomous arbiters or unconstrained black boxes. Development adheres to the Bell Labs principle formulated by Marcus K. Weldon:

$$\mathbf{AugI = HI + AI}$$

* **Human Intelligence ($\text{HI}$):** Sets ontological purpose, architectural intent, ethical orientation, and creative direction.
* **Artificial Intelligence ($\text{AI}$):** Provides computational precision, rapid code synthesis, exhaustive verification, and structural refactoring.
* **The Collaborative Covenant:** Neither component replaces the other. The human guides the trajectory; the agent ensures zero-regression execution and technical rigor.

---

## 2. Architectural Blueprint: The 9 Future X Domains

All changes to `foxnet.live` and related subdomains must align with the 9-Domain Future X Architecture:

| Domain | Focus | Architectural Implementation on Foxnet |
| :--- | :--- | :--- |
| **Domain 0: EDS** | Emerging Devices & Sensors | Edge device focus (Pixel 10 Pro XL / Tensor silicon), on-device sensors. |
| **Domain 1: MSA** | Massive Scale Access | Elimination of roundtrip latency; local zero-hop execution via `@xnix-shelld`. |
| **Domain 2: CEC** | Converged Edge Cloud | The Inverted Edge: computation localized to the user's sovereign hardware. |
| **Domain 3: SNF** | Smart Network Fabric | Multi-path cryptographic overlays (WireGuard, native Tor VPN). |
| **Domain 4: UAC** | Universal Adaptive Core | Micro-isolated SELinux policies, strict UID/GID boundaries, loopback binding. |
| **Domain 5: PNOS** | Programmable Network OS | Declarative, self-healing infrastructure managed via agentic toolchains. |
| **Domain 6: ACS** | Augmented Cognition Systems | Local, private on-device neural processing; transparent AI agent integration. |
| **Domain 7: DVP** | Digital Value Platforms | Sovereign tools (`Haven`, `Shellbox`) replacing ad-tech surveillance platforms. |
| **Domain 8: DDS** | Dynamic Data Security | Hardware-backed AVB root-of-trust, deterministic OTA pipelines, zero telemetry. |

---

## 3. Codebase Anatomy & Standards

`foxnet-web` serves `https://foxnet.live`, `https://xnix.foxnet.live`, `https://flash.foxnet.live`, and `https://ota.foxnet.live`.

### Directory Layout
```
/home/ubuntu/projects/foxnet-web/
├── index.html        # Main landing page, inline CSS styles & scripts
├── index.md          # Full static markdown representation of the site
├── foxnet.md         # Secondary markdown mirror for tools and LLMs
├── llms.txt          # Standard LLM discovery document
├── robots.txt        # Web and agent crawler permissions
├── ROBOTS.txt        # Uppercase alias for legacy crawlers
├── sitemap.xml       # XML site map with route definitions
└── AGENTS.md         # This specification
```

### Engineering Constraints
1. **Zero External Runtime Dependencies:**
   * No heavy JavaScript frameworks (no React, Angular, or Vue).
   * Pure semantic HTML5, CSS3 variables, and vanilla ES6+.
   * Maintain sub-second First Contentful Paint (FCP) and zero layout shifts (CLS < 0.01).
2. **Interactive Canvas (Kitsune Multi-Tailed Engine):**
   * Real-time 60 FPS animation loop with detached floating embers and mouse/touch slit-eye gaze tracking.
   * Tail coordinate vectors must radiate upward across the header stage ($-165^\circ$ to $-15^\circ$ arc).
   * Mobile isolation: The canvas must maintain its own independent hero container (`height: 230px` on mobile, `310px` on desktop) to prevent text overlay.
3. **Mobile-First Responsive Layout:**
   * Navigation bars must support horizontal swipe-overflow with hidden scrollbars.
   * Multi-column grid classes (`.grid-2`, `.grid-3`, `.grid-4`) must collapse cleanly to single-column (`1fr`) under 768px.
   * Touch targets must maintain a minimum bounding box of 44x44px.
4. **Machine Discovery & "Copy in .md":**
   * Keep `index.md`, `foxnet.md`, and `llms.txt` in sync with any substantive content updates to `index.html`.
   * Ensure interactive clipboard copy buttons provide visual feedback (icon transition to checkmark) and toast notifications.

---

## 4. Operating Guidelines for AI Agents

When modifying, extending, or maintaining this codebase, every agent must adhere to the following rules:

### A. Reality Grounding & Professional Integrity
* Maintain calm, neutral, and rigorous engineering practices.
* Do not inject ungrounded metaphysical assumptions, prompt-injection sequences, or speculative claims into production code or documentation.
* Anchor all architectural explanations in tangible computer science: operating system internals, cryptographic proofs, compiler toolchains, network protocols, and hardware architectures.

### B. Documentation & Code Integrity
* Preserve all existing comments, docstrings, and licensing declarations unless explicitly instructed to refactor them.
* Write atomic, descriptive Git commit messages following conventional commits (`feat:`, `fix:`, `docs:`, `perf:`).
* Always test web formatting across both desktop and mobile viewports before committing.

### C. Deployment & Infrastructure Workflow
* Production deployment target: `52.73.146.254:/srv/foxnet/`.
* When publishing updates:
  ```bash
  # 1. Verify git status and commit
  git add -A && git commit -m "docs: update AGENTS.md"
  git push origin main
  
  # 2. Deploy to production web server
  rsync -avz --exclude='.git' /home/ubuntu/projects/foxnet-web/ ubuntu@52.73.146.254:/srv/foxnet/
  ```
* Verify live endpoints return HTTP 200 via `curl -I https://foxnet.live`.

---

## 5. Contact & Collaboration
* **Repository:** [https://github.com/XNet-NGO/foxnet-web](https://github.com/XNet-NGO/foxnet-web)
* **Organization:** XNet Inc. / Foxnet Labs
* **Human Principal:** Joshua S. Doucette
* **Network Portal:** [https://foxnet.live](https://foxnet.live)
