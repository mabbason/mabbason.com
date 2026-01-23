# Profile Sync Checklist

Use this checklist whenever updating resume, website, or LinkedIn to ensure consistency across all platforms.

## Quick Reference: File Locations

| Item | Location |
|------|----------|
| Website HTML | `public/index.html` |
| Website Resume PDF | `public/assets/miles-abbason-resume.pdf` |
| Resume Source | FlowCV (download latest from Downloads folder) |
| LinkedIn | https://www.linkedin.com/in/miles-abbason/ |
| Screenshots | `/mnt/c/Users/mabba/Pictures/Screenshots/` |

---

## 1. Summary/Intro Statement

All three platforms should convey the same core message.

| Platform | Location | Current Text |
|----------|----------|--------------|
| **Website** | `index.html` line ~66 | "I'm a software engineer with a passion for learning who develops resilient cloud applications using systematic practices and AI-augmented tooling." |
| **Resume** | Summary section | Similar messaging about systematic development, AI-augmented tooling, resilient cloud applications |
| **LinkedIn** | About section | Should match website/resume tone |
| **LinkedIn** | Featured > Personal Site card | Should match website intro |

### Validation Steps:
- [ ] Website intro matches resume summary in tone and key points
- [ ] LinkedIn About section aligns with resume summary
- [ ] LinkedIn Featured "Personal Site" card description matches website intro
- [ ] No outdated phrases (e.g., "recently built" for old projects)

---

## 2. Skills - Languages & Frameworks

| Platform | Location |
|----------|----------|
| **Website** | `index.html` Skills section (~line 109) |
| **Resume** | Skills > Languages and Frameworks |
| **LinkedIn** | Skills section + Experience entries |

### Current Canonical List:
```
JavaScript, TypeScript, Node.js, Koa, Express, React, Redux, Jest, Material UI, Python, C#, SQL, Go
```

### Validation Steps:
- [ ] All skills on resume appear on website (order may differ for visual layout)
- [ ] No skills on website that aren't on resume
- [ ] LinkedIn skills align with resume
- [ ] Website formatting displays correctly (check for awkward line breaks)

---

## 3. Skills - Cloud

| Platform | Location |
|----------|----------|
| **Website** | `index.html` Skills section (~line 114) |
| **Resume** | Skills > Cloud |
| **LinkedIn** | Skills section |

### Current Canonical List:
```
AWS: Lambda, SQS, SNS, EventBridge, IAM, RDS, ElasticBeanstalk, CDK, DigitalOcean, Heroku
```

### Validation Steps:
- [ ] All cloud skills on resume appear on website
- [ ] Consistent naming (CDK vs "Cloud Development Kit", DigitalOcean vs "Digital Ocean")
- [ ] Website formatting displays correctly

---

## 4. Skills - Other Technologies

| Platform | Location |
|----------|----------|
| **Website** | `index.html` Skills section (~line 119) |
| **Resume** | Skills > Other Technologies |
| **LinkedIn** | Skills section |

### Current Canonical List:
```
MongoDB, PostgreSQL, Git, REST APIs, Docker, Nginx, ElasticAPM, RabbitMQ, Sentry, Webhooks, AI development tooling
```

### Resume Additional (not on website):
```
Claude Code, systematic prompt engineering
```

### Validation Steps:
- [ ] Core technologies match between resume and website
- [ ] AI tooling terminology is appropriate (website: "AI development tooling", resume: "Claude Code")
- [ ] Website formatting displays correctly

---

## 5. Experience Dates

All dates must match exactly across platforms.

| Role | Dates |
|------|-------|
| Software Engineer, Botkeeper | 12/2022 – Present |
| Co-Creator, Software Engineer, Seymour | 05/2022 – 12/2022 |
| Full Stack Web Developer, Self Employed | 02/2021 – 05/2022 |
| Trading Systems Developer, Crucis Capital | 06/2018 – 03/2022 |
| Co-Founder, Pelican's SnoBalls | 01/2011 – 05/2018 |

### Validation Steps:
- [ ] Resume dates match this table
- [ ] LinkedIn dates match this table (format: "Mon YYYY - Mon YYYY")
- [ ] No roles showing as "Present" that should be ended
- [ ] Duration calculations on LinkedIn are correct

---

## 6. Resume PDF on Website

| Item | Details |
|------|---------|
| Website path | `public/assets/miles-abbason-resume.pdf` |
| Filename | Must remain `miles-abbason-resume.pdf` (links depend on it) |
| Source | Latest FlowCV export |

### Validation Steps:
- [ ] Website PDF matches the latest FlowCV export
- [ ] File size is similar to source (indicates successful copy)
- [ ] PDF is accessible via website download link
- [ ] Commit and deploy after updating

---

## 7. Visual/Formatting Checks

### Website Text Wrapping:
- [ ] "AI-augmented" stays on same line (uses `<span style="white-space: nowrap;">`)
- [ ] Skills sections display without awkward breaks
- [ ] Test at different browser widths

### LinkedIn:
- [ ] Profile photo is current
- [ ] Banner image is appropriate
- [ ] Featured section cards display correctly

---

## 8. Seymour Project References

Website mentions Seymour in multiple places. Ensure consistency:

| Location | Check |
|----------|-------|
| Banner intro | "I built Seymour..." (not "recently built") |
| Seymour section | Description matches case study |
| LinkedIn Seymour entry | Dates and description align |

### Validation Steps:
- [ ] No "recently" language for projects older than 1 year
- [ ] Case study link works: seymour-active-monitoring.github.io/case-study
- [ ] Seymour dates consistent (05/2022 – 12/2022)

---

## Sync Workflow

### When Resume is Updated:
1. Export new PDF from FlowCV
2. Run comparison analysis (see automation section below)
3. Update website content if needed
4. Copy new PDF to `public/assets/miles-abbason-resume.pdf`
5. Commit, push, deploy
6. Update LinkedIn to match
7. Take screenshots of LinkedIn for verification
8. Run final validation

### When Website is Updated:
1. Ensure changes align with resume
2. Update LinkedIn if needed
3. Deploy changes
4. Verify visual display (take screenshots)

### When LinkedIn is Updated:
1. Take screenshots for records
2. Verify alignment with resume/website
3. Update other platforms if LinkedIn has newer info

---

## Automation: Claude Code Analysis Prompt

When validating alignment, use this prompt with Claude Code:

```
Review my resume, website, and LinkedIn for alignment:

1. Read the most recent resume PDF from Downloads (FlowCV format)
2. Read the website at /home/mabba/capstone/job-hunt/personal-site/mabbason.com/public/index.html
3. Check recent screenshots in /mnt/c/Users/mabba/Pictures/Screenshots/ for LinkedIn content

Compare and report:
- Summary/intro statement consistency
- Skills alignment (Languages & Frameworks, Cloud, Other Technologies)
- Experience dates matching
- Any outdated language (e.g., "recently" for old projects)
- Formatting issues on website

Provide a table showing discrepancies and recommended fixes.
```

---

## Version History

| Date | Changes |
|------|---------|
| 2026-01-23 | Initial checklist created after full alignment session |

---

## Notes

- Resume is source of truth for dates and experience details
- Website can have slightly different skill ordering for visual layout
- Website uses "AI development tooling" (general), resume uses "Claude Code" (specific)
- Always test website display after changes (check screenshots)
- LinkedIn Featured section needs manual update (can't be automated)
