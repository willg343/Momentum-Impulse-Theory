//this is version 2.2 where proportions were used to increase/decrease the pixel distance difference

var O = canvas.getContext('2d')
var d = 22,c=0,b=false,sp=4,m=10,v=20,t=1;z='m = 10kg; F = 200N; Δt = 1s; v = 20m/s';

$("h1").click(function (){
  Q=+prompt('Please input the value with - or + sign ( Please try keeping m > 0):')
  sp*=(1+(200/(m+Q)-v)/v)
  m+=Q
  v=200/m
  $("h3").text(z.replace(/(?<=m = )\d+/,m+'').replace(/(?<=v = )\d+/,v+''))
})

$("h2").click(function (){
  B=+prompt('please input the value with - or + sign (try keeping v>0):')
  sp*=(1+B/v)
  v+=B
  m=200/v
  $("h3").text(z.replace(/(?<=v = )\d+/,v+'').replace(/(?<=m = )\d+/,m+''))
})

function S(){
  if (d>=canvas.width-50)  clearInterval(s)
    O.fillStyle = '#700202'
    O.fillRect(10,86,1200,20)
    O.beginPath()
    d+=sp
    O.fillStyle='#F90606'
    O.arc(d,59,28,0,Math.PI*2)
    O.fill()
}
$("body").keydown(function (E){
  if (E.keyCode==13){
    clearInterval(s)
    d=22
    b=false
    c=0
    s = setInterval(function(){
      O.clearRect(0,0,1200,380)
      S()
    },15)
  }
  if (E.keyCode==32){
    c++
    if(c%2==0){
      s = setInterval(function(){
      O.clearRect(0,0,1200,380)
      S()
    },15)
  ;return
  }
  clearInterval(s)        
  }
})

s = setInterval(function(){
  O.clearRect(0,0,1200,380)
  S()
},15)
