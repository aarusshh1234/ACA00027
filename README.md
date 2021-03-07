var bunny;
var carrot;
var edges;

function setup() {
createCanvas(600,600);

edges=createEdgeSprites();
bunny = createSprite(40,550,30,30); 
carrot = createSprite(560,40,30,30);

obs1 = createSprite(300,120,150,20);
obs1.velocityX = 0;
obs2 = createSprite(300,180,150,20);
obs2.velocityX = 0;
obs3 = createSprite(300,240,150,20);
obs3.velocityX = 0;
obs4 = createSprite(300,300,150,20);
obs4.velocityX = 0;
obs5 = createSprite(100,300,150,20);
obs5.velocityX = 0;
obs6= createSprite(100,240,150,20);
obs6.velocityX = 0;
obs7 = createSprite(100,180,150,20);
obs7.velocityX = 0;
obs8 = createSprite(100,120,150,20);
obs8.velocityX = 0;
obs9 = createSprite(500,210,170,210);
obs9.velocityX = 0;
carrot.shapeColor = "pink"
obs2.shapeColor = "red"
obs1.shapeColor = "red"
obs3.shapeColor = "red"
obs4.shapeColor = "red"
bunny.shapeColor="white"
}

function draw() {
background("black");  

bunny.bounceOff(edges[0]);
bunny.bounceOff(edges[1]);
bunny.bounceOff(edges[2]);
bunny.bounceOff(edges[3]);
obs1.bounceOff(edges[1]);
obs1.bounceOff(edges[0]);
obs2.bounceOff(edges[1]);
obs2.bounceOff(edges[0]);
obs3.bounceOff(edges[1]);
obs3.bounceOff(edges[0]);
obs4.bounceOff(edges[1]);
obs4.bounceOff(edges[0]);


if(keyDown("up")){
  bunny.y=bunny.y-3;
}
if(keyDown("down")){
  bunny.y=bunny.y+3;
}
if(keyDown("left")){
  bunny.x=bunny.x-3;
}
if(keyDown("right")){
  bunny.x=bunny.x+3;
}
if(bunny.isTouching(carrot)){
  text("YOU WIN",200,200);
}
if(bunny.isTouching(obs1)){
  obs1.velocityX=0;
  text("YOU LOSE",200,200);
}
if(bunny.isTouching(obs2)){
  obs2.velocityX=0;
  text("YOU LOSE",200,200);
}
  if(bunny.isTouching(obs3)){
    obs3.velocityX=0;
    text("YOU LOSE",200,200);
}
if(bunny.isTouching(obs4)){
  obs2.velocityX=0;
  text("YOU LOSE",200,200);
}
  drawSprites();
}
