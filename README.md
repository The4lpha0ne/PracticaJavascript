# Practica Javascript 1: Hoverboard
---
## 1ro CFGS DAW, Richard Francisco Vaca García
---
### En este proyecto se utiliza:
* **HTML**
* **CSS**
* **JavaScript**
---
### Este proyecto consiste en una plataforma rectangular formada por pequeños cuadrados de color gris que cambian de color cuando el puntero del ratón pasa por por encima, como una patineta que deja un rastro mientras se desliza sobre una plataforma.
---
### El código más destacado del projecto (JavaScript):
```python=
const container = document.getElementById('container')
const colors = ['#e74c3c', '#8e44ad', '#3498db', 
    '#e67e22', '#2ecc71']
const SQUARES = 476

for (let i = 0; i < SQUARES; i++) {
    const square = document.createElement('div')
    square.classList.add('square')
    square.addEventListener('mouseover', () => 
        setColor(square))
    square.addEventListener('mouseout', () => 
        removeColor(square))
    container.appendChild(square)
}

function setColor(element) {
    const color = getRandomColor()
    element.style.background = color
    element.style.boxShadow = 
        `0 0 2px ${color}, 0 0 10px ${color}`     
}

function removeColor(element) {
    element.style.background = '#1d1d1d'
    element.style.boxShadow = `0 0 2px #000`
}

function getRandomColor() {
    return colors[Math.floor(
        Math.random() * colors.length)]
}
```
---
***[Link del Repositorio](https://github.com/The4lpha0ne/PracticaJavascript.git)***
--
***[Link de la Página Web alojado en GitHub Pages](https://the4lpha0ne.github.io/PracticaJavascript/)***
--
---
###### tags: `Programación` `HTML` `CSS` `JavaScript`