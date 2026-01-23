# mabbason.com

Personal portfolio site deployed to Digital Ocean.

## Deployment

```bash
git add . && git commit -m "message" && git push
ssh -i ~/.ssh/digitalocean_auto mabba@mabbason.com "cd ~/mabbason.com && git pull origin main"
```

## Profile Sync Validation

**When updating resume PDF, skills, intro text, or experience content:** Read `PROFILE_SYNC_CHECKLIST.md` and run alignment validation across resume, website, and LinkedIn.
