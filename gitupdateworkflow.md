## This is your ongoing workflow

Whenever Karpathy updates upstream:

```bash
git fetch upstream
git checkout master
git reset --hard upstream/master
git push origin master --force-with-lease

git checkout macos
git rebase master
git push origin macos --force-with-lease
```

## Good safety habit before each rebase

```bash
git checkout macos
git branch backup/macos-$(date +%Y%m%d-%H%M%S)
```

If something goes wrong:

```bash
git rebase --abort
```