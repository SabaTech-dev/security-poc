# 🛡️ Security Audit POC — SabaTech

> Demo visual de auditoría de seguridad para sistemas de IA y agentes autónomos.

## 🎯 Qué es esto

POC (Proof of Concept) que demuestra las capacidades de auditoría de seguridad de SabaTech:

- **OWASP Agentic Apps 2026** — Top 10 riesgos de seguridad para aplicaciones agentic
- **EU AI Act Compliance** — Clasificación de riesgos, obligaciones de transparencia
- **NIST AI RMF** — AI Risk Management Framework
- **Escaneo en tiempo real** — Detección de vulnerabilidades críticas

## 🚀 Quick Start

### Opción 1: Docker (recomendado)

```bash
docker build -t security-poc .
docker run -p 8081:80 security-poc
# Abrir http://localhost:8081
```

### Opción 2: Servidor local

```bash
python3 -m http.server 8081
```

Abrir `http://localhost:8081` en el navegador.

## 🔍 Vulnerabilidades Detectadas (Demo)

La demo muestra los siguientes tipos de findings:

| Severity | Finding |
|----------|---------|
| 🔴 CRITICAL | Agent prompt injection — input sanitization bypass |
| 🔴 CRITICAL | Unrestricted tool execution — no RBAC on shell commands |
| 🔴 CRITICAL | API key exposed in agent memory/context window |
| 🟠 HIGH | Missing rate limiting on agent orchestration endpoints |
| 🟠 HIGH | Insecure SSE transport — no auth on streaming |
| 🟡 MEDIUM | CORS misconfiguration allows wildcard origins |
| 🟡 MEDIUM | Agent conversation logs stored without encryption |
| 🔵 LOW | Missing Content-Security-Policy headers |
| 🟢 PASS | TLS 1.3, JWT rotation, container isolation |

## 📊 Compliance Frameworks

- **EU AI Act** — Reglamento europeo de IA
- **OWASP Agentic 2026** — Top 10 seguridad aplicaciones agentic
- **NIST AI RMF** — Framework de gestión de riesgos de IA

## 📁 Estructura

```
security-poc/
├── index.html      # Landing page (self-contained, dark mode)
├── Dockerfile      # nginx:alpine
└── README.md       # Este archivo
```

## ⚠️ Nota

**Todos los datos mostrados son simulados/demo.** Los findings de seguridad son ejemplos representativos.

## 📄 Licencia

© 2026 SabaTech — Demo POC

## 🔗 Enlaces

- [SabaTech](https://sabatech.dev)
- [Contacto](https://sabatech.dev/contact)
