## To create the helm chart
Udate the version present in `Chart.yaml` with new version (not the appVersion)
Run below commands from root directory:
```
helm package syncpolicy-test/testchart/ -d helm-packages/
helm repo index helm-packages/

```
---
##  To host the chart 
First you need to go to your git repo, then
- Go to `Settings` for the repo
- Go to `Pages`
- Under `Build and deployment` , select:
  - Source > Deploy from a branch
  - Branch > Select a branch where you have uploaded you helm chart
  Then click Save.
- Wait for a while, you will receive the site link where your helm chart is hosted ("Your site is live at https://testsite.github.io/repoName")
---