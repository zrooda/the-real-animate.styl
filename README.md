# the-real-animate.styl
**TL;DR** The [animate.css](https://github.com/daneden/animate.css) port to Stylus that you're looking for.

Stylus | [SASS](https://github.com/mystrdat/the-real-animate.sass)  

- Keyframes are rendered automatically on first use, no extra imports needed, no duplicates
- No classes, animations are directly attached to styled element
- Automatic optimization for animated properties
- Stylus hashes as data source (JSON-like)

```Sass
@import 'src/the-real-animate'

my-widget

  &.coming-in-hot
    animate(bounceInLeft) // default 1s

  &.delayed-bye-bye
    animate(fadeOut, 3s, 250ms)
```

```Css
my-widget.coming-in-hot {
  animation-name: bounceInLeft;
  animation-duration: 1000ms;
  animation-fill-mode: both;
  will-change: opacity, transform; }

@keyframes bounceInLeft { ... }

my-widget.delayed-bye-bye {
  animation-name: fadeOut;
  animation-duration: 3s;
  animation-delay: 250ms;
  animation-fill-mode: both;
  will-change: opacity; }

@keyframes fadeOut { ... }

```
