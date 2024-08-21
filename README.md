let palavra;

function setup() {
  createCanvas(400, 400);
  
  
  let palavras = ["Otavio", "Augusto", "Oliveira"];
  
  palavra = random(palavras);
}

function inicializaCores() {
  
  background("rgb(7,7,7)");
  fill("rgb(248,246,246)");
  textSize(64);
  textAlign(CENTER, CENTER);
}

function draw() {
  
  inicializaCores();

  let maximo = width;
  let minimo = 0;
  // mouseX, 0, width ==> 0, palavra.length
  
  let quantidade = map(mouseX, 0, width, 1, palavra.length);
  //console.log(quantidade);
  let parcial = palavra.substring(0, quantidade);
  text(parcial, 200, 200);
  
}
