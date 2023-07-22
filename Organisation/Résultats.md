
# DS

```dataviewjs  
const matieres = ["Maths", "Info", "Physique"]
for(const mat of ["Total", ...matieres]){
const postfix = mat == "Total" ? "" : "/" + mat.toLowerCase()
const data = dv.pages("#ds"+postfix).sort(p => p.mois)
  
const chartData = {  
type: 'line',  
options: {
   scales: {
      y: { min: 0, max: 20 }
   }
},
data: {  
labels: data.map(p => p.sujet).values,  
datasets: [{  
label: 'Notes' + postfix,  
data: data.map(p => p.note).values,  
backgroundColor: [  
'rgba(255, 99, 132, 0.2)'  
],  
borderColor: [  
'rgba(255, 99, 132, 1)'  
],  
borderWidth: 1  
},
{  
label: 'Satisfaction' + postfix,  
data: data.map(p => p.satisfaction * 2).values,  
backgroundColor: [  
'rgba(132, 99, 255, 0.2)'  
],  
borderColor: [  
'rgba(132, 99, 255, 1)'  
],  
borderWidth: 1  
}, 
{  
label: 'Classement' + postfix,  
data: data.map(p => (45 - p.classement + 1) * 20 / 45).values,  
backgroundColor: [  
'rgba(188, 188, 40, 0.2)'  
],  
borderColor: [  
'rgba(188, 188, 0, 1)'  
],  
borderWidth: 1  
}
]  
}  
}  

dv.el("h2", mat)

const abs = x => x < 0 ? -x : x;

for (const [name, datum] 
of [ [ "Notes: ", data.map(p=>p.note)]
   , ["Satisfaction: ", data.map(p=>p.satisfaction)]
   , ["Classement: ", data.map(p=>p.classement)]]){
	const avg = datum.values.reduce((a,b)=>a+b)/datum.values.length; 
	const std = datum.values.map(x => abs(x-avg)).reduce((a,b)=>a+b)/datum.values.length;
	dv.el("p", name + "$"+avg.toFixed(2)+ " \\pm "+std.toFixed(2)+"$");
}

window.renderChart(chartData, this.container);  
}

const data = matieres.map(m => dv.pages("#ds/"+m.toLowerCase()).map(p => p.note)).map(notes => {
   return notes.values.reduce((a,b) => a + b) / notes.length;
})

const chartData = {  
type: 'radar',  
options: {
   scales: {
      r: { min: 0, max: 20 }
   }
},
data: {  
labels: matieres,  
datasets: [{  
label: 'Notes',
data: data,  
backgroundColor: [  
'rgba(255, 99, 132, 0.2)'  
],  
borderColor: [  
'rgba(255, 99, 132, 1)'  
],  
borderWidth: 1  
}
]  
},
}  

dv.el("h2", "Répartition des notes");
window.renderChart(chartData, this.container);  
```


# Colles

```dataviewjs  
const matieres = ["Maths", "Info", "Physique", "Anglais"]
for(const mat of ["Total", ...matieres]){
const postfix = mat == "Total" ? "" : "/" + mat.toLowerCase()
const data = dv.pages("#colle"+postfix).sort(p => p.semaine)
  
const chartData = {  
type: 'line',  
options: {
   scales: {
      y: { min: 8, max: 20 }
   }
},
data: {  
labels: data.map(p => p.sujet).values,  
datasets: [{  
label: 'Notes' + postfix,  
data: data.map(p => p.note).values,  
backgroundColor: [  
'rgba(255, 99, 132, 0.2)'  
],  
borderColor: [  
'rgba(255, 99, 132, 1)'  
],  
borderWidth: 1
},
{  
label: 'Satisfaction' + postfix,  
data: data.map(p => p.satisfaction + 8).values,  
backgroundColor: [  
'rgba(132, 99, 255, 0.2)'  
],  
borderColor: [  
'rgba(132, 99, 255, 1)'  
],  
borderWidth: 1  
}
]  
}  
}  

dv.el("h2", mat)

const abs = x => x < 0 ? -x : x;
for (const [name, datum] 
of [ [ "Notes: ", data.map(p=>p.note)]
   , ["Satisfaction: ", data.map(p=>p.satisfaction)]]){
	const avg = datum.values.reduce((a,b)=>a+b)/datum.values.length; 
	const std = datum.values.map(x => abs(x-avg)).reduce((a,b)=>a+b)/datum.values.length;
	dv.el("p", name + "$"+avg.toFixed(2)+ " \\pm "+std.toFixed(2)+"$");
}

window.renderChart(chartData, this.container);  

}


const data = matieres.map(m => dv.pages("#colle/"+m.toLowerCase()).map(p => p.note)).map(notes => {
   return notes.values.reduce((a,b) => a + b) / notes.length;
})

const chartData = {  
type: 'radar',  
options: {
   scales: {
      r: { min: 0, max: 20 }
   }
},
data: {  
labels: matieres,  
datasets: [{  
label: 'Notes',
data: data,  
backgroundColor: [  
'rgba(255, 99, 132, 0.2)'  
],  
borderColor: [  
'rgba(255, 99, 132, 1)'  
],  
borderWidth: 1  
}
]  
},
}  

dv.el("h2", "Répartition des notes");
window.renderChart(chartData, this.container);  
```



