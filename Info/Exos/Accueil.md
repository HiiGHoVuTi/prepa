---
dg-publish: true
---

```dataview
table chapitres, difficulté
from "Info/Exos"
where file.name != "Accueil"
sort difficulté
```
