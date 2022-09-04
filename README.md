# typeracer-autotype

Start race, paste script in console, type

```
var element = document.getElementsByClassName('inputPanel')[0]
var textElements = element.getElementsByTagName('span')
var text = ''
for (var i = 0; i < textElements.length; i++) {
    text += textElements[i].innerHTML
}
var counter = 0
var input = document.getElementsByClassName('txtInput')[0]
function onKeyDown(e) {
    e.preventDefault()
    input.value += text[counter]
    counter++
}
input.addEventListener('keydown', onKeyDown);
```
