# mabbason.com - Personal Portfolio Site

## Project Overview

Personal portfolio website for Miles Abbason, deployed to Digital Ocean.

## Deployment

```bash
# Commit and push
git add . && git commit -m "message" && git push

# Deploy to server
ssh -i ~/.ssh/digitalocean_auto mabba@mabbason.com "cd ~/mabbason.com && git pull origin main"
```

## Key Files

| File | Purpose |
|------|---------|
| `public/index.html` | Main website content |
| `public/assets/miles-abbason-resume.pdf` | Resume PDF (must keep this filename) |
| `PROFILE_SYNC_CHECKLIST.md` | Alignment checklist for resume/website/LinkedIn |

---

## IMPORTANT: Profile Sync Validation

**Whenever the website content or resume is updated, run profile alignment validation.**

### Automatic Validation Trigger

When any of these occur:
- Resume PDF is updated
- `index.html` skills sections are modified
- Intro/summary text is changed
- Experience-related content is modified

### Validation Process

1. **Read the latest resume** from Downloads:
   ```
   /mnt/c/Users/mabba/Downloads/Miles-Abbason-FlowCV-Resume-*.pdf
   ```
   (Find most recent by date)

2. **Read website content**:
   ```
   public/index.html
   ```

3. **Check LinkedIn via screenshots**:
   ```
   /mnt/c/Users/mabba/Pictures/Screenshots/
   ```
   (Ask user to take fresh screenshots if needed)

4. **Compare and validate**:
   - Summary/intro statement consistency
   - Skills alignment (Languages & Frameworks, Cloud, Other Technologies)
   - Experience dates matching exactly
   - No outdated language ("recently" for old projects)
   - Formatting displays correctly (no awkward line breaks)

5. **Report discrepancies** in a table format and recommend fixes

### Current Canonical Data (Updated 2026-01-23)

**Intro Statement:**
> "I'm a software engineer with a passion for learning who develops resilient cloud applications using systematic practices and AI-augmented tooling."

**Skills - Languages & Frameworks:**
> JavaScript, TypeScript, Node.js, Koa, Express, React, Redux, Jest, Material UI, Python, C#, SQL, Go

**Skills - Cloud:**
> AWS: Lambda, SQS, SNS, EventBridge, IAM, RDS, ElasticBeanstalk, CDK, DigitalOcean, Heroku

**Skills - Other Technologies:**
> MongoDB, PostgreSQL, Git, REST APIs, Docker, Nginx, ElasticAPM, RabbitMQ, Sentry, Webhooks, AI development tooling

**Experience Dates:**
| Role | Dates |
|------|-------|
| Botkeeper | 12/2022 – Present |
| Seymour | 05/2022 – 12/2022 |
| Full Stack Web Developer | 02/2021 – 05/2022 |
| Trading Systems Developer | 06/2018 – 03/2022 |
| Pelican's SnoBalls | 01/2011 – 05/2018 |

### Formatting Rules

- Use `<span style="white-space: nowrap;">` for terms that shouldn't break (e.g., "AI-augmented")
- Website skill ordering may differ from resume for visual balance
- Website uses "AI development tooling" (general), resume uses "Claude Code" (specific)

See `PROFILE_SYNC_CHECKLIST.md` for complete validation checklist.
