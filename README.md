var mysound
function preload(){
soundFormats("mp3")
  mysound =loadSound("123.mp3")
}
function setup() {
  createCanvas(400, 400);


}
var x = 1
var y = 300
var z = 1
var j = 1
var r = 1
var b = 30
var h = 0
var ok = 30
var v = 1
var v1 = 1
var o = 3
var b1 = 10
var a = [1,3,4]
var QQx = 1
var QQy = 300
var QQz = 1
var QQj =1
function draw() {
  background(x, ok+30, ok);
  noStroke()
  fill(25,25)
  rect(QQx,QQy,QQx-j,QQy + 100 + h)
  QQx=QQx+QQj
  if(QQx>width){QQj=-1}
  if(QQx<0){QQj=1}
  
  fill(ok)
  ellipse(x-z,j,z+y,y)
    // ellipse(x-z+30,j+100,y/10)
  
  
  
  stroke(1)
  fill(3)
  ellipse(x, y - h, b) //heads
  strokeWeight(10)
  line(x, y - h, x, y + 60) //body
  line(x, y + 60, x + j, y + 100 + h) //legs
  line(x, y + 60, x - j, y + 100 + h) //legs
  ellipse(x + v + b1, y + 100 + h, 10) //ball


  x = x + z
  j = j + r
  //line(x, y + 30 - h, x + j, y + 60 - h) //hands
  line(x, (2 * y - h + 60 + b) / 2, x + j + o, (2 * y - h + 60 + b) / 2 + (2 * y - h + 60 + b) / 100) //hands
  line(x, (2 * y - h + 60 + b) / 2, x - j + o, y + 60 - h) //hands
  stroke(1)
  line(0, y + 105 + h, width, y + 105 + h) //fl
  // if(j>=-10||j<=12){v=j}
  //if(j>12){v=10}
  // While(x+v+b1>x+20){ if(x+v+b1<x+j || x+v+b1<x-j){v1=random(0,10)}}
  if (z > 0) {//右
    v = v + v1
      if (x + v > width) {
       mysound.play() 
        
    v1 = -3, b1 = b1 * -0.1
  }
  if (x + v < 0) {
    v1 = 1
     if (x + v + b1 < x + j || x + v + b1 < x - j) {
    v1 = random(0, 10)
  }
  }
  }
 if (z <= 0) {  v = v -0.1*v1//左
              //if (x + v > width)
             //  {v1 = 3, b1 = b1 * -0.1 }
              if(x+v+b1<=0)
              {v1=3,b1 = b1 * -0.1} 
             }
  
  //if(x+v<=-200||x+v>=600){v=-1}/////extra

  if (x + v + b1 < x + j || x + v + b1 < x - j) {
    v1 = random(0, 10)
  }





  if (j > 12)(r = -0.6)
  if (j < -10)(r = 0.5)
  if (x > width) {
    z = -1, b = random(1, 100), y = random(height), h = random(0, 30),
       QQy=y,
    ok = random(0, 50), o = random(-10, 10)
    v = v * -1
    b1 = b1 * -1
  }

  fill(300, 300, 300)

  if (x < 0) {
    ok = random(0, 50)
    z = 1, b = random(1, 100), y = random(height), h = random(0, 30),
    QQy=y,
    
    
    o = random(-100, 100)
    v = v * -1
    b1 = b1 * -1
  }

  line(0, y + 105 + h, width, y + 105 + h) //fl
  stroke(1)
  
  
  
  // ellipse(QQx,QQy,10)
  
  
 if (keyIsDown(DOWN_ARROW)){
  QQy=QQy+1
  
  }
  

  
    if (keyIsDown(RIGHT_ARROW)){
  QQx=QQx+1
  
   }
  
  if (keyIsDown(LEFT_ARROW)){
   QQx=QQx-1
     }
  
//   QQy = QQy + QQt
  
//  // if (QQy>300){QQt= QQt*-0.3}
//   if(QQy<=y + h-QQR){QQt=3,QQR=random(-30,30)}//上
//   //if(300<=QQy<=400){QQt=10}
  
// //   if (QQy<300){QQt= QQt *-1}
// //   if(QQy>=300){QQt =QQt *1}
//     if (QQy>=y + 100 + h){QQt=QQt*random(-0.9,-1.5),QQR=random(-40,30)}//下
  
  
//   if(QQt>=20){QQt=QQt*0.1}//限速
  
  
//   if(y + 100-random(0.3,3)*y + h<=QQy<=y + 100 + h){ 
//   if (keyIsDown(UP_ARROW) ){
//   QQy=QQy-1}}
  
  
//   if(QQx<=0){QQx=0}
//   if(QQx>=400){QQx=400}
  
  
 // line(x,y,z,j)


}
