# Subir *Biofónica* a GitHub

```powershell
cd "D:\Dv\Repo\Ableton\Biofonica"
gh auth login -h github.com
gh repo create biofonica-touchme --public --description "Biofónica — Ableton Live + TouchMe, concierto táctil" --source=. --remote=origin --push
```

URL: https://github.com/fernandoog/biofonica-touchme