var puX=52; var puY=61; var puW=180; var curX=57; var curY=curX-88; var recX=13; var recY=340; var recW=115; var recH=recW-96; var leftX=-96; var rightx=453; var lastcloud=83;

draw= function() { background(206,227,235); //last bottom cloud fill(223,234,237); noStroke(); ellipse(lastcloud,226,126,97); ellipse(lastcloud-73,231,70,60); ellipse(lastcloud+69,231,79,60);

lastcloud+=1;

//pupusa
fill(219, 196, 160);
noStroke();
ellipse(puX,puY,puW,puW-10);

//burn parts of the pupusa
fill(120,86,32);
stroke(54,37,7);
strokeWeight(4);

beginShape();// 1 upper left side 
curveVertex(curX-5/18*puW,curY-11/18*puW);
curveVertex(curX-11/36*puW,curY+17/36*puW);
curveVertex(curX-11/36*puW,curY+1/2*puW);
curveVertex(curX+5/9*puW,curY+5/9*puW);
endShape();

beginShape();// 2 lower left side 
curveVertex(curX-1/12*puW,curY-2/3*puW);
curveVertex(curX-1/32*puW,curY+29/36*puW);
curveVertex(curX-1/32*puW,curY+29/36*puW);
curveVertex(curX-47/36*puW,curY+3/4*puW);
endShape();

beginShape();// 3 upper middle
curveVertex(curX-13/36*puW,curY-19/18*puW);
curveVertex(curX-1/6*puW,curY+1/12*puW);
curveVertex(curX-1/6*puW,curY+1/6*puW);
curveVertex(curX+2/9*puW,curY+15/18*puW);
endShape();

beginShape();// 4 middle middle
curveVertex(curX-5/18*puW,curY+5/9*puW);
curveVertex(curX-1/9*puW,curY+1/3*puW);
curveVertex(curX,curY+17/36*puW);
curveVertex(curX-1/36*puW,curY-1/4*puW);
endShape();

beginShape();// 5 lower right
curveVertex(curX+11/12*puW,curY+11/36*puW);
curveVertex(curX+11/36*puW,curY+23/36*puW);
curveVertex(curX+11/36*puW,curY+25/36*puW);
curveVertex(curX-1/4*puW,curY+7/36*puW);
endShape();

 beginShape();// 6 upper right
curveVertex(curX-5/18*puW,curY+5/9*puW);
curveVertex(curX+5/18*puW,curY+1/4*puW);
curveVertex(curX+5/18*puW,curY+1/4*puW);
curveVertex(curX-2/9*puW,curY-1/4*puW);
endShape();

puX+=1;
puY+=1;
curX+=1;
curY+=1;

//cloud
fill(250, 250, 250);
noStroke();
//left cloud
ellipse(leftX,60,126,97);
ellipse(leftX+62,61,70,60);
ellipse(leftX-62,61,70,60);

fill(35,112,54);
textSize(30);
text("Pupuseria El Retorno!",54,70);

//cloud
fill(255, 255, 255);
noStroke();
//right cloud
ellipse(rightx,20,126,97);
ellipse(rightx+62,25,70,60);
ellipse(rightx-63,25,79,60);

leftX+=1;
rightx-=1;

//casita cement
fill(166,163,163);
stroke(115,109,109);
strokeWeight(2);
rect(recX-10,recY+42,recW+18,10);

//casita green part
fill(28,87,8);
stroke(10,110,13);
rect(recX,recY+22,recW,20);

//casita white part
fill(245,237,237);
stroke(248,237,237);
rect(recX,recY,recW,24);

//casita white upper part
fill(245,237,237);
stroke(204,204,204);
rect(recX-4,recY-6,recW+8,10);

//doors
fill(8,8,8);
stroke(8,8,8);
rect(recX+28,recY+12,recW-107,30);//left

fill(8,8,8);
stroke(8,8,8);
rect(recX+78,recY+12,recW-107,30);//right

fill(8,8,8);
textSize(22);
text("La Variedad Favorita del Salvador!", 31, 129);
textSize(16);
text("Te Esperamos",132,180);

textSize(20);
text("Martes-Domingo", 118, 223);
text(" 2:30 PM - 8 PM", 115, 253);
};
