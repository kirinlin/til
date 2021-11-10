# Simple Release by git tag

```shell
export LAST_REL_DATE="2021-05-05"
export REL_TAG="2021.4.1110"
# Check logs from last release date
git log --since="${LAST_REL_DATE}"
# Modify CHANGELOG and commit
git add CHANGELOG.md
git commit -s -m "Tag: ${REL_TAG}"
# Tag it and push all
git tag -a "v${REL_TAG}" -m "Release v${REL_TAG}"
git push --tags
```
