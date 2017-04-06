CSS
===

# Objective
```
Prise de notes sur la manipulation des elements en css.
```

# How to use
With **shyganer** in **/home/shyganer/**
```sh
firefox -new-window index.html
```

# CENTRAGE HORIZONTAL
## Centrer le contenu du span et son parent
```css

.parent {
  text-align: center;
}

/*
** Le contenu se centre par rapport a son parent.
** Fonctionne pour les elements qui sont en display: inline ou inline-block.
 */
.child {
  display: inline-block;
  height: 8%;   /* la hauteur doit etre renseigner */
  width: 12%;   /* la largeur doit etre renseigner */
}
```
*Une div enfant est par default en display: block;*

## Centrer un element div
Toutes div enfants est par default en display: block;

```css
.parent {
  text-align: center;
}

/*
** Pour un display block, on utilise les margins.
 */
 /* Centrer avec les blocks a la vertical */
.child {
  display: block;
  margin: 0 auto;
}

 /* Centrer avec les blocks sur une seule ligne */
.child {
  display: inline-block;
}
```

## Centrer un element en float
```css

.parent {
  text-align: center;
}

/*
** Le float: left va transformer les elements en block,
* *le text-align: center ne s'applique donc plus.
** Il faut creer un parent et le mettre en display: inline-block;
*/
.parents {
  display: inline-block;
}

.child {
  float: left;
}  
```

# CENTRAGE VERTICAL
## Centrer une div

```css
/*
** On definit la meme hauteur de ligne que la hauteur de la div,
** et on passe l'enfant en display: inline;
 */
.parent {
  height: 768px;
  line-height: 768px; /* La hauteur de ligne n'affecte que
                         les elements qui sont en display: inline;
                      */
}

.child {
  display: inline;
}
```

## Centrer verticalement a l'aide de display: table;
**vertical-align: middle;** ne fonctionne que pour les tableaux.
```css
/* Il faut au total 3 elements */
.parent {
display: table; /* On convertie la div en tableau. */
}

.child {
display: table-cell; /* On converti la div en cellule de tableau */
vertical-align: center;
}

.subChild {
/* Le contenu de notre choix */  
}
```

## Centrer verticalement grace a la position: absolute.
```css
.parent {
  position: relative;
}

.child {
  width: 60px; /* L'enfant doit avoir une largeur et hauteur fixes */
  height: 30px;
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  margin: auto;
}
```

## Centrer verticalement et horizontalement via les pourcentages.
```css

.parent {
  position: relative;
}

.child {
  position: absolute;
  width: 100px;
  height: 30px;
  top: 50%;
  left: 50%;
  transform: translateX(-50%) translateY(-50%);
}
```


# A retenir
## Pour le centrage
Le **text-align: center;** ne s'applique qu'aux elements de type **inline**.
Si l'element n'est pas de type inline (block), il faut utiliser **margin: 0 auto;**.
Le **vertical-align: center;** ne s'applique qu'au **cellule de tableau**.
Pour centrer un element par rapport a son coin **interieur gauche**, donnees les valeurs
de **width et height en pourcentage**.

# Errors
```
```

# Bugs
```
```

# Todo
```
```

# References
1. [Graphikart centrer elements css](https://www.youtube.com/watch?v=QhHzxF2Kq8Q)
2. [Tricks CSS](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
3. [Can I Use](http://caniuse.com/#search=flexbo)
