# Solo-Dev-Ops-Playbook
Lightweight checklist for deploying, managing, and operating apps (frontend, backend, DB, Redis, etc.) as a solo developer.

---

## 🔹 Daily
- [ ] Check error logs (app, DB, Redis)
- [ ] Verify uptime monitor (UptimeRobot / BetterStack)
- [ ] Look at key metrics (requests/sec, DB connections, error rates)

> 💡 Automate alerts → Slack/Discord/email. Don’t rely on manual checks.

---

## 🔹 Weekly
- [ ] Review slow DB queries (use EXPLAIN or monitoring tool)
- [ ] Scan logs for warnings (not just errors)
- [ ] Confirm monitoring + alerts are still working
- [ ] Check SSL certs are valid (if not auto-renewed)

---

## 🔹 Monthly
- [ ] Test backup + restore (DB + Redis snapshot)
- [ ] Apply system & library security patches
- [ ] Review infra costs (shut down unused services)
- [ ] Check resource usage (CPU, memory, disk)
- [ ] Rotate sensitive secrets / API keys

---

## 🔹 Quarterly
- [ ] Audit access (SSH keys, API tokens, DB users)
- [ ] Run security scans (npm audit, Snyk, etc.)
- [ ] Perform light load test (simulate higher traffic)
- [ ] Review architecture → does it still fit current scale?

---

## 🔹 Yearly (or Major Releases)
- [ ] Do a "fire drill" (kill DB or server, test recovery process)
- [ ] Review vendor lock-in risks (migration feasibility)
- [ ] Clean up old code, services, infra not in use

---

## ⚡ Tools to Automate
- **Monitoring**: BetterStack, UptimeRobot
- **Logging**: Logtail, Axiom, Datadog
- **Backups**: Cloud provider snapshots, DB-native backups (cron/managed)
- **CI/CD**: GitHub Actions → auto-deploy (Vercel/Render/Fly.io)
- **Security**: Dependabot, Snyk

---

## 🚩 Common Pitfalls
- ❌ No restore testing (backups unverified)
- ❌ Cost creep from unused infra
- ❌ Manual deploys → human error
- ❌ Overbuilding infra too early (K8s, multi-VPS, service mesh)
- ❌ No monitoring (finding out from users when app is down)

---

✅ Stick to this playbook → you’ll cover 90% of what full SRE teams do, solo.
