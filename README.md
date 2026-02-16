# 5010-Assignment4

```
let img
function preload(){
img = loadImage('111.png');
   data = loadJSON('https://api.worldbank.org/v2/countries/CHN/indicators/SP.POP.TOTL?per_page=5000&format=json')
}
  
  
  function setup() {
colorMode(HSB)
 

}

function draw(){
  createCanvas(600,600)
  background(255,180,0)
  
if(data === undefined ) return
const records = data[1]
let population = []

for( let i = 0; i < records.length; i++ )
{console.log(records[i].value)
 let x=records[i].value/2000000
 population.push(x)
 console.log(population)
 noStroke()
fill(random(0),random(0,255),random(0,255))
circle(300,300,x)
}


noLoop()

image(img,-20,-20,640,640)
}
```

### https://editor.p5js.org/supperred1/full/__E4Y4zB5

### Here is my code and preview. This is a statistical chart of China's population, where each ring represents the population size for a particular year. I called a Chinese population API, extracted the "value" data from it, and used it to determine the radius of each ring. I also assigned a random color to each ring.
