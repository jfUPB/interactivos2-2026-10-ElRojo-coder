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

## Bitácora de aplicación 



## Bitácora de reflexión
