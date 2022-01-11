var atiro = {strike: false, spare: false, score: ""};
var tiros = [];
var bonus = 0;

function tiro() {
    var bolos = 11;
    var aTiro = {strike: false, spare: false, score: ""};
    bonus = atiro.spare || atiro.strike ? 10 : 0;

    console.log("Primer tiro .... ");
    bolos = Math.floor(Math.random() * bolos);
    aTiro.score = bolos + bonus;

    
    if (bolos == 10) {
        console.log("Strike!");
        aTiro.strike = true;
        console.log(aTiro);
        return aTiro;
    }

    bolosRestantes = 10 - bolos;
    console.log("Bolos derribados en el primer tiro " + bolos);
    console.log("Bolos restantes: " + bolosRestantes);

    console.log("Segundo tiro .... ");
    bolos = Math.floor(Math.random() * bolosRestantes);

    aTiro.score += bolos + bonus;

    console.log("Bolos derribados en el segundo tiro " + bolos);

    if (bolos == 10) {
        console.log("Spare!");
        aTiro.spare = true;
        console.log(aTiro);
        return aTiro;
    }

    bolos = bolosRestantes - bolos;
    console.log("Bolos restantes: " + bolos);
    console.log("bolos restantes " + bolos + " puntuación: " + aTiro.score);
    console.log(aTiro);
    return aTiro;
}

function juego(){
    var score = 0;

    for(var i=0; i<10; i++){
        console.log("Ronda " + (i+1));
        
        atiro = tiro();

        tiros.push(atiro);
        score = atiro.score + score;
        console.log(score);
    }

    console.log("RESUMEN DE LA PARTIDA:");
    console.log("|##########################################|");
    console.log(tiros);
}

juego();

