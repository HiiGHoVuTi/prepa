---
dg-publish: true
---

# Cours 

```dataview
list
from #maths/cours
sort order asc
```

# Colles & Co.

```dataview
table chapitres, difficulté
from "Maths/Colles"
sort difficulté asc, file.cdate asc
```

# Preuves
```dataview
list from "Maths"
where regexmatch(".*Preuve.*", file.name)
sort file.cday asc
```


