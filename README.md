# www.adventuity.co.za

This repository only publishes the Adventuity Floodline website at **https://www.adventuity.co.za** (GitHub Pages).
It holds no website files of its own.

- The site's files live in [Katiso0623/adventuity-hub](https://github.com/Katiso0623/adventuity-hub) in the `floodline/` folder,
  written by the Floodline project.
- `.github/workflows/publish.yml` copies that folder and deploys it to GitHub Pages. It runs when this repository changes,
  when you start it by hand (Actions → Publish www.adventuity.co.za → Run workflow), and every 30 minutes, when it publishes
  only if the Floodline files have changed (it compares a fingerprint with `https://www.adventuity.co.za/site-version.txt`).
- Once a month it records a heartbeat commit (`.github/heartbeat`) so GitHub keeps the 30-minute check switched on.
- Address: Settings → Pages → custom domain `www.adventuity.co.za`, HTTPS enforced. DNS at Afrihost: `www` CNAME
  `katiso0623.github.io`, and the four GitHub A records on `adventuity.co.za` (GitHub forwards the bare domain to www).
  The domain is verified on the Katiso0623 account.
- The learner and tutor portal is a separate site: https://learn.adventuity.co.za (repository adventuity-hub).
