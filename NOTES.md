<!--
1. Issirenki dizaina. Ji issisaugai ir persikeli i Paint.
2. Ji issikerpi tiek kiek realiai naudosi.
3. Documents susikuri nauja projekta (49-grupe-live-video)
4. Ji atsidarai Visual Studio Code
5. Terminale: $npm init -y ( jo pagalba atsiranda package.json)
6. Terminale: $touch index.html .gitignore
7. Terminale: npm i -D dead-server
8. package.json
"scripts": {
    "dev": "dead-server --host=localhost --port=4906",
9. .gitignore:
node_modules
.vscode
.DS_Store
10. Terminale: $git init
11. Terminale: git add .
12. Terminale: $ git commit -m "Initial commit" (Git- spausti Publish)
index.html ! enter (ismes !DOCTYPE)
13. Prie <title> isirasyti projekto pav</title>
Terminale: $npm run dev (kad ismestu psl ir ar veikia dalykai)
Sutvarkyti Github: Nueiti i ji-> Settings -> Branch -> Master (Bet kas tik ne None)
Github griztam i Code -> About-> description (Student project) ->website (kokiam galiu rasti)->Topics (apie ka projektas)
14. Susikurti README.md (nusikopijuot is anksciau ka turiu)
-------------------------------------
Dizainas:
Sudarytas is:
 Virsutine dalis HEADER:
      jis suskaidytas i logotipa
      desiniam sone turi navigacija
      navigacija turi savo individualias nuorodas
      jei tinkame psl, jis nurodo jog ten esi
 Apatine dalis:
     socialiniai tinklai su savo ikonelem
     ikoneles pavaizduotos kaip nuorodos
 Pagrindas:
 Turi tekstini stulpeli:
    antraste
    paragrafas
    download migtukas ar nuoroda
 Paveiksliukas:
 ----------------------------------------
 Susitvarkom ir issisaugom kaip mums reikia. Saugom tame paciame dokumente kaip ir visas projektas.
 Jei per daug nuotrauku, susikuriam img ir sukeliam.
 -----------------------------------------
 index.html issideliojam struktura:
 Siuo atveju: <header>, <main>, <footer>
 ----------------------------------
 Kai reikia kelti logo is vieno html failo i kita, pvz i index.html noriu kelti foto is img: <header>
        <img src="./img/logo.png" alt="HIWOW logo">
 ---------------------------------------------
 CSS
 Header.css
 Jo tvarkymas:

 komentaras: tam, kad pasislinktu header i tinkamas vietas, juos floatinam i puses kur mums reikia. Tam, kad nedingtu aukstis, ivedame teviniam elementui display: inline-block;
 PVZ:

 header {
    display: inline-block;
    background-color: yellow;
}

header > img {
    float:left;

}
header > nav {
    float:right;
Kadangi po isivedimo mums truko plocio iki galo, dar paplidomai ivedem:
header {
    display: inline-block;
    width: 100%;
    background-color: yellow;
Logotipas per aukstas, todel pasitaisau ir iterpiu height:

header > img {
    float: left;
    height: 50px;

}
Pasididinau viso teksto srifta:
header a {
    font-size: 20px;

}
Kai noriu suzinoti header logotipo auksti ir desinej esanciu nuorodu auksti:

(H-h)/2   H- reiketu suprasti kaip Logotipo H, o h- kaip Home teksto. Cia kai norim atitraukti ir pasiziuret atstumus kaip viskas parasyta.

header a {
    font-size: 20px;
    line-height: 20px;
}
----------

Margin-top grazino per viduriuka:

header > nav {
    margin-top: 15px;
    float: right;
}
---------------------
Jei norim tarp header teksto nuorodu padaryti tarpus:
header a {
    float: left;
    margin-left: 50px;
    font-size: 20px;
    line-height: 20px;
    text-decoration: none;
}
Jei norim, kad paskurinioji nuoroda is ju butu be atsitraukimo. Mums pades psiaudo selektoriai, jie prasideda su 1 dvitaskiu:

header a:last-child {
    margin-right:0;
}

Psiaudo selektoriai:
Kai norim, kad kazka pvz darytu header su tekstu. Pvz nudazytu kokia spalva zodi, taip pat naudojame:

header a:last-child {
    margin-right:0;
}

header a:nth-child(2),
header a:nth-child(4),
header a:nth-child(6), {
    background-color: red;
}
Tai sitoje situacijoje nudazys kas antra raudonai, bet daug rasymo.

Sutrumpinimas:
div,
p,
a {
    font-size:30px;
}
 Cia vienu kartu visiems priskirs stiliu, tik aisku ne apie header kalba, o bendrai.


 -->
<!--
Ka reikia daryti jei reikia selektinimo, jei daug turiu ka reikia pazymeti pvz raudonai, pvz ir juos turi ideti i krepseli?

Yra formule: tiesine lygtis: f(x)=ax+b

Pvz. header a:nth-child (2n){
    background : red;
}
 (..n)- dvitaskuose yra tas skaicius, ties kuriuo mums reikes to paryskinimo.

O kaip paimti nelyginius narius. Kad paimtu 1,3,5,7.....*/

header a:nth-child (2n + 1) {
    background : red;
}

nth-of-type- ziuri ne ar visi vaikai, o kuris mergaite, kuris berniukas:

/* a:nth-of-type(2n){
    background-color: red;
}


 -->

<!--
css. calc funkcijoje aplink matematinius operatorius reikia prideti tarpus!!!!

main {
    display: inline-block;
    border: 1px solid red;
}

main > div {
    float: left;
    width: calc(40% - 20 px);
    padiing: 5%;
    border: 10px solid green;

}

sita versija paprastesne:
main > div {
    float: left;
    width: 50%;
    padiing: 80px;
    border: 30px solid green;
    box-sizing

}

 -->

 <!-- 
 Jei noriu nusistatyti sablona, kad visada butu:
 CTRL + SHIFT + P 
 atsiras virsuje nuorodos ir jose isivesti -> user sniooets.
 Tada renkames css + enter

 Kaip susikurti snipetus:

 "Labas": {
    "prefit": "snippets",
    "body": [
        "1) ctrl + shift + p",
        "2) search: user snippets",
        "3) filter: css",
        "4) susikuriam savp snippetus",
    
    ]
 }
  -->
  <!-- 
  Kai reikia pasidaryti nauja tuscia projekta 
  ir su jo pirminiais css faile esanciais turiniais:
  Reikia:
  Base (reset);
  Index.html;
  Main;
  Header;



   -->
