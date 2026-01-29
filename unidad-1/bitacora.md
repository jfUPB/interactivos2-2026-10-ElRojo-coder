# Unidad 1

## Bitácora de proceso de aprendizaje
experimentando un poco con una base que vi en la documentación quise hacer un beat como de hip hop simple el cual lo compone la bateria o bd, el platillo o el hh, el clap o cp y la caja o bank

```js
setcps(.6)

let chords = chord("<Dm7 Gm7>/2").dict('ireal')

stack(

  stack(
    
    s("bd")
      .struct("<x 0 0 x>"),

    s("sd")
      .struct("<0 x 0 x>")
      .gain(.9),

    n("0 1 0 1")
      .s("hh")
      .gain(.5)
      .speed("<1 1.2>")
  )
  .bank("crate")
  .room(.2),
)
.size(3)

```

#### Experimento 2 
Le pedí a chat que creara en base a ese bit un dembow y la propuesta fue interesante
```js
setcps(.6)

let chords = chord("<Dm7 Gm7>/2").dict('ireal')

stack(
  // Kick dembow
  s("bd")
    .struct("<x 0 x 0>")
    .gain(1),

  // Snare / clap en el 3
  s("sd")
    .struct("<0 0 x 0>")
    .gain(.9),

  // Hi-hat movido
  n("0 1 0 1")
    .s("hh")
    .struct("x*4")
    .gain(.5)
    .speed("<1 1.2>"),

  // Chord stab simple
  chords
    .s("keys")
    .gain(.6)
    .room(.3)
)
.bank("crate")
.size(3)

```
## Bitácora de aplicación 

para este quise hacer algo mas robusto con un afro house 
```js
samples('github:eddyflux/crate')
setcps(.8)


let chords = chord("<Bbm7 Fm7>/4").dict('ireal')

stack(

  stack(
    s("bd")
      .struct("<x 0 x 0>"),

    n("0 <0 0>")
      .s("conga")
      .gain("<0 .8>"),

    n("0 0 0 0")
      .s("shaker")
      .gain(.6),

    n("0")
      .s("rim")
      .struct("<0 0 x 0>")
  )
  .bank('crate')
  .room(.3),

  
  chords
    .voicing()
    .s("gm_epiano1")
    .gain(.7)
    .room(.6)
    .shape(.3),


  n("0 0 <0 2>")
    .set(chords)
    .mode("root:g2")
    .s("gm_acoustic_bass")
    .gain(.8)
    .room(.2)
)
.size(3)
```
## Bitácora de reflexión

