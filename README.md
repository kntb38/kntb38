function setup() {
    createCanvas(600, 400);
}

function draw() {
    background(0);
    circle(0, 0, 50);
}
//variavel
let xBolinha = 300;
let yBolinha = 200;
let diametro = 15;
let raio = diametro / 4;

//velocidade
let velocidadeXBolinha = 4;
let velocidadeYBolinha = 4;

function setup() {
    createCanvas(600, 400);
}

function draw() {
    background(0);
    mostraBolinha();
    movimentoBolinha();
    colisaoBolinha();
}

function mostraBolinha (){
  circle(xBolinha, yBolinha, diametro);
}
function movimentoBolinha (){
  xBolinha += velocidadeXBolinha;
  yBolinha += velocidadeYBolinha;
}
function colisaoBolinha (){
  if (xBolinha + raio > width || xBolinha - raio < 0) {
        velocidadeXBolinha *= -1;
    }
    if (yBolinha + raio > height || yBolinha - raio < 0) {
        velocidadeYBolinha *= -1;
    }
}
