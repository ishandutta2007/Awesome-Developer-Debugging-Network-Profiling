# Awesome-Developer-Debugging-Network-Profiling

## Top Developer Debugging & Network Profiling Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Traffic Interception, Performance Profiling & Production Error Tracking*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Developer Debugging & Network Profiling**. These tools help engineers inspect HTTP traffic, profile CPU and memory, trace distributed requests, and capture production errors—covering everything from browser DevTools and local proxies to full APM suites and error monitoring platforms.

**Examples** include Chrome DevTools, HTTP Toolkit, Wireshark, Sentry, Datadog APM, Charles Proxy, Fiddler, Proxyman, mitmproxy, and OWASP ZAP (the category leaders).

**Open-source emphasis**: This section highlights every major active project for self-hosted traffic inspection, open-source observability, and community-driven debugging—ideal for developers and teams seeking transparency and predictable costs over per-event or per-host SaaS billing. The open-source landscape is exceptionally strong here: **HTTP Toolkit** is a fully open-source (Apache-licensed) proxy with one-click interception and a powerful rules engine [citation:2], **Wireshark** remains the world's leading protocol analyzer with 1,000+ protocols [citation:14], and **SigNoz** provides an OpenTelemetry-native APM alternative to Datadog [citation:6].

Contributions welcome! Open an PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-products)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

| Product | Description | Pricing (Starting) | Free Tier / Trial Limits |
|---------|-------------|-------------------|--------------------------|
| **[Sentry](https://sentry.io/)** | Production error tracking and performance monitoring with stack traces, breadcrumbs, session replay, and distributed tracing. Captures errors, spans, replays, and profiles as separate metered quotas. | Developer: **$0/month**; Team starting tier: **$26/month** (annual) or **$29/month** (monthly); Business starting tier: **$80/month** (annual). | **Developer (Free forever)**: 5,000 errors/month, 10,000 transactions (5M spans)/month, 50 session replays/month, 1 user, 30-day data retention, 10 dashboards; **Free trial**: 14-day trial with full feature and unlimited event access. |
| **[Datadog APM](https://www.datadoghq.com/)** | Full-stack observability with APM, infrastructure monitoring, logs, and distributed tracing. APM requires underlying host infrastructure monitoring. | Infrastructure starting tier: Pro at **$15/host/month** (annual) or **$18/host/month** (on-demand); APM starting tier: Standard at **$31/host/month** (annual) or **$36/host/month** (on-demand) [Baseline total: **$46/host/month** annual]. | **Free Infrastructure plan (Free forever)**: Up to 5 hosts, 1-day metric retention (excludes APM); **APM Free trial**: 14-day fully featured trial with unlimited hosts and metrics. |
| **[Charles Proxy](https://www.charlesproxy.com/)** | Long-standing HTTP/HTTPS debugging proxy with SSL proxying, bandwidth throttling, breakpoints, rewrite rules, and AJAX/AMF inspection. | Single-user perpetual license: **$50 one-time fee** (includes all v5.x updates; major upgrades at 40% discount). | **Free trial**: 30-day evaluation period; after 30 days, continuous use is restricted to 30 minutes per session with automated application shutdown and a startup delay nag screen. |
| **[Fiddler Everywhere](https://www.telerik.com/fiddler)** | Cross-platform web debugging proxy with traffic capture, inspection, rules-based modification, and team collaboration. SOC 2, HIPAA, and GDPR compliant. | Lite starting tier: **$7/user/month** (annual commitment) or **$10/user/month** (monthly); Pro starting tier: **$13/user/month** (annual) or **$19/user/month** (monthly); Enterprise tier: **$37/user/month** (annual). | **Free trial only**: 10-day fully functional free trial with full feature access and unlimited captures; no ongoing perpetual free tier (legacy non-commercial Fiddler Classic is Windows-only). |
| **[Proxyman](https://proxyman.com/)** | Native macOS/Windows/Linux HTTPS debugging proxy with iOS companion app. SSL proxying, breakpoints, Map Local/Remote, scripting, and network conditions. | Standard desktop perpetual license: **$89 one-time fee** (1 seat / 1 active device, lifetime access with 1 year of free updates); iOS Premium from **$12.98/month**. | **Free version (Free forever for personal use)**: Unlimited duration for non-commercial use, restricted to 1–2 rules per advanced tool (Breakpoints, Map Local/Remote, Scripting, SSL Proxying list), and max 2 pinned domains/apps; **Commercial trial**: 14 days full evaluation before requiring a Pro license. |

## Open-Source GitHub Projects

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[HTTP Toolkit](https://github.com/httptoolkit/httptoolkit)** | [![Stars](https://img.shields.io/github/stars/httptoolkit/httptoolkit?style=social&color=white)](https://github.com/httptoolkit/httptoolkit/stargazers) | **The most complete open-source alternative to Chrome DevTools' network tab and Charles Proxy.** 100% open-source (Apache-licensed internals). One-click interception for browsers, mobile apps, Docker containers, terminal sessions, and backend processes (Node.js, Java, Python, Ruby). Features: **Monaco-based body editor** (VS Code internals) with syntax highlighting for JSON, Protobuf, Base64, HTML, XML; **breakpoints** for manual request/response editing; **rules engine** for mocking, redirecting, and transforming traffic; built-in documentation for 2,600+ APIs; automatic caching and compression analysis . |
| **[Wireshark](https://github.com/wireshark/wireshark)** | [![Stars](https://img.shields.io/github/stars/wireshark/wireshark?style=social&color=white)](https://github.com/wireshark/wireshark/stargazers) | **The world's leading network protocol analyzer.** Examines data from live network captures or saved files across wired, wireless (WiFi/Bluetooth), and USB sources. Supports **dozens of capture file formats and 1,000+ protocols**. Rich display filter language, TCP stream reassembly, file extraction from HTTP/CIFS, and RTP audio playback . Recent releases add **process attribution** (PID and process name per packet) and Zstandard compression . |
| **[mitmproxy](https://github.com/mitmproxy/mitmproxy)** | [![Stars](https://img.shields.io/github/stars/mitmproxy/mitmproxy?style=social&color=white)](https://github.com/mitmproxy/mitmproxy/stargazers) | **The standard scriptable intercepting proxy for automated traffic manipulation.** Interactive SSL/TLS-capable proxy for HTTP/1, HTTP/2, and WebSockets. Intercept and modify requests/responses on the fly, save conversations for replay, and use **Python scripts** to automate changes. Transparent proxy mode on macOS/Linux; SSL certificates generated on the fly . |
| **[OWASP ZAP](https://github.com/zaproxy/zaproxy)** | [![Stars](https://img.shields.io/github/stars/zaproxy/zaproxy?style=social&color=white)](https://github.com/zaproxy/zaproxy/stargazers) | **The world's most widely deployed open-source DAST proxy.** Intercepting proxy with passive scanning (safe) and active scanning (intrusive, test environments only). Includes traditional and AJAX spiders. **Baseline scans are CI-ready**—run `zap-baseline.py` on every PR for security header checks without risk . |
| **[SigNoz](https://github.com/SigNoz/signoz)** | [![Stars](https://img.shields.io/github/stars/SigNoz/signoz?style=social&color=white)](https://github.com/SigNoz/signoz/stargazers) | **OpenTelemetry-native observability platform—the leading open-source Datadog alternative.** Single application for logs, traces, and metrics. Built on ClickHouse for fast querying. Features: APM with p99 latency, error rate, and Apdex charts; distributed tracing with flamegraphs and Gantt charts; log management with powerful query builder; customizable dashboards; alerts on any telemetry signal; **LLM observability** for tracking token usage and prompt performance. Self-hosted via Docker or Helm; cloud option available . |

### Additional Strong Open-Source Options

| Project | Star Badge | Description |
|---------|------------|-------------|
| **[Betwixt](https://github.com/kdzwinel/betwixt)** | [![Stars](https://img.shields.io/github/stars/kdzwinel/betwixt?style=social&color=white)](https://github.com/kdzwinel/betwixt/stargazers) | System-wide network monitor and web debugging proxy. Captures traffic from **any installed application** (not just browsers) and renders it in a Chrome DevTools-compatible interface. Performs MITM HTTPS decryption via generated root certificate . |
| **[Front-end Debugging Tools Handbook](https://github.com/lala-hakobyan/front-end-debugging-handbook)** | [![Stars](https://img.shields.io/github/stars/lala-hakobyan/front-end-debugging-handbook?style=social&color=white)](https://github.com/lala-hakobyan/front-end-debugging-handbook/stargazers) | Practical guide to front-end debugging across DevTools, framework extensions, and IDEs. ~60 stars. Useful as a learning resource alongside tooling . |

**Frameworks for building custom systems**: Choose **HTTP Toolkit** for a full-featured open-source proxy with one-click interception and rules-based mocking, **Wireshark** for deep protocol analysis, **mitmproxy** for scriptable traffic automation, and **SigNoz** for OpenTelemetry-native APM—creating a fully open-source debugging and observability stack without per-host or per-event SaaS fees.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Debugging proxies intercept sensitive traffic including credentials and session tokens; **only intercept traffic you own or have explicit permission to inspect**. Install root certificates only in controlled environments and remove them when finished.
- **SaaS pricing models compound unpredictably.** Sentry meters errors, spans, replays, and attachments as separate quotas—a 2:10 AM error spike can exhaust the error quota before the first alert arrives, and uncapped pay-as-you-go turns that spike into an uncapped bill . Datadog bills per host for APM, per GB for logs, and per host for infrastructure—median contracts reach **~$154,080/year** . **Open-source alternatives eliminate per-host and per-event fees** but require infrastructure provisioning. **HTTP Toolkit** is the most complete open-source proxy replacement for Charles/Fiddler , and **SigNoz** provides a genuine Datadog APM alternative for teams willing to self-host .

---

**Made for developers, SREs, QA engineers, and teams debugging network traffic and production errors.**  
Let's make developer debugging and network profiling more open, observable, and cost-predictable.
