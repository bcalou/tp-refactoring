# DOM Scripting Refactoring

Voici des extraits de code réels. À vous de les refactoriser, c'est à dire :

- comprendre la logique et le but du code présenté
- renommer logiquement les variables, fonctions... pour clarifier la situation
- découper le code en plusieurs fonctions si nécessaire
- raccourcir le code au moyen de boucles et autres astuces
- rendre le code adaptable à des variables d'entrée différentes, l'adapter à plus de situations

## Partie 1

- Créez un codepen ou un document sur votre machine.
- Ajoutez à la page le script ci-dessous, et les éléments HTML permettant de le faire fonctionner.
- Constatez le bon fonctionnement du script et comprenez-en le fonctionnement : arrivez-vous à le reformuler à l'oral ?
- Vous pouvez refactoriser !
- Vérifiez à la fin que le code fonctionne toujours à l'identique

```
let lether = document.getElementById("lether");
let wool = document.getElementById("wool");
let lyocell = document.getElementById("lyocell");

let lether__text = document.getElementById("lether__text");
let wool__text = document.getElementById("wool__text");
let lyocell__text = document.getElementById("lyocell__text");

lether.addEventListener("click", function() {
  lether__text.className = "is-checked";
  wool__text.className = "fabric__choice";
  lyocell__text.className = "fabric__choice";
});

wool.addEventListener("click", function() {
  lether__text.className = "fabric__choice";
  wool__text.className = "is-checked";
  lyocell__text.className = "fabric__choice";
});

lyocell.addEventListener("click", function() {
  lether__text.className = "fabric__choice";
  wool__text.className = "fabric__choice";
  lyocell__text.className = "is-checked";
});
```

Voir la correction sur [Codepen](https://codepen.io/heticschool/pen/XWbVYoy)

## Partie 2

```
const Colwhite = document.querySelector(".color__Col--white");
const Colgreen = document.querySelector(".color__Col--green");
const Colyellow = document.querySelector(".color__Col--yellow");
const Colred = document.querySelector(".color__Col--red");
const Colblue = document.querySelector(".color__Col--blue");
const Colpurple = document.querySelector(".color__Col--purple");

Colwhite.addEventListener("click", function() {
  root.style.setProperty("--third-bg-color", "white");
});
Colgreen.addEventListener("click", function() {
  root.style.setProperty("--third-bg-color", "lightgreen");
});
Colyellow.addEventListener("click", function() {
  root.style.setProperty("--third-bg-color", "lightyellow");
});
Colred.addEventListener("click", function() {
  root.style.setProperty("--third-bg-color", "red");
});
Colblue.addEventListener("click", function() {
  root.style.setProperty("--third-bg-color", "lightcyan");
});
Colpurple.addEventListener("click", function() {
  root.style.setProperty("--third-bg-color", "purple");
});
```

Voir la correction sur [Codepen](https://codepen.io/heticschool/pen/gOpEzKK)

## Partie 3

```
const btnTest =  document.getElementById("more1");
const btnmore =  document.getElementById("more2");
const btnTest3 =  document.getElementById("more3");
const btnTest4 =  document.getElementById("more4");
const btnTest5 =  document.getElementById("more5");



btnTest.addEventListener("click", function() {
  const btnTest =  document.getElementById("more1");

  var changewindow = document.getElementById("window1").style.display
	var more = document.getElementById("more1")

	if(changewindow == "none")
	{
   	changewindow = document.getElementById("window1").style.display = "block" ;
		more.innerHTML ="-";
	}

	else if(changewindow == "block")
	{
		changewindow = document.getElementById("window1").style.display = "none" ;
		more.innerHTML ="+";
  }

});

btnmore.addEventListener("click", function() {

  var changewindow = document.getElementById("window2").style.display
	var more = document.getElementById("more2")

	if(changewindow == "none")
	{
   	changewindow = document.getElementById("window2").style.display = "block" ;
		more.innerHTML ="-";
	}

	else if(changewindow == "block")
	{
		changewindow = document.getElementById("window2").style.display = "none" ;
		more.innerHTML ="+";
  }

});

btnTest3.addEventListener("click", function() {

  var changewindow = document.getElementById("window4").style.display
	var more = document.getElementById("more3")

	if(changewindow == "none")
	{
   	changewindow = document.getElementById("window4").style.display = "block" ;
		more.innerHTML ="-";
	}

	else if(changewindow == "block")
	{
		changewindow = document.getElementById("window4").style.display = "none" ;
		more.innerHTML ="+";
  }

});

btnTest4.addEventListener("click", function() {

  var changewindow = document.getElementById("window5").style.display
	var more = document.getElementById("more4")

	if(changewindow == "none")
	{
   	changewindow = document.getElementById("window5").style.display = "block" ;
		more.innerHTML ="-";
	}

	else if(changewindow == "block")
	{
		changewindow = document.getElementById("window5").style.display = "none" ;
		more.innerHTML ="+";
  }

});

btnTest5.addEventListener("click", function() {

  var changewindow = document.getElementById("window6").style.display
	var more = document.getElementById("more5")

	if(changewindow == "none")
	{
   	changewindow = document.getElementById("window6").style.display = "block" ;
		more.innerHTML ="-";
	}

	else if(changewindow == "block")
	{
		changewindow = document.getElementById("window6").style.display = "none" ;
		more.innerHTML ="+";
  }

});
```

Voir la correction sur [Codepen](https://codepen.io/heticschool/pen/abOMKBL)
