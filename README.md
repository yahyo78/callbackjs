# callbackjs
# Callback дар JavaScript

Дар JavaScript, **callback** (функсияи бозхонд) як функсияест, ки ҳамчун параметр ба функсияи дигар дода шуда, баъдтар иҷро мешавад. Callback асосан барои кор бо функсияҳои асинхронӣ ва ҳамзамон ҳалли масъалаҳои иҷрои пайдарпай истифода мешавад.

## 1. Чӣ гуна callback кор мекунад?

```js
function salom(name, callback) {
    console.log("Салом, " + name + "!");
    callback();
}

function khotima() {
    console.log("Хуш омадед ба ҷаҳони JavaScript!");
}

salom("Алишер", khotima);
```
📌 **Тавзеҳ:** Дар ин мисол, `khotima` ҳамчун callback ба `salom` дода шудааст ва пас аз иҷрои `console.log`, он низ иҷро мешавад.

---

## 2. Callback дар функсияҳои асинхронӣ

```js
console.log("Оғоз...");

setTimeout(function() {
    console.log("Маълумоти сервер қабул шуд!");
}, 2000);

console.log("Интизори маълумот...");
```
📌 **Тавзеҳ:** `setTimeout` як функсияи асинхронӣ буда, ки пас аз 2 сония callback-ро иҷро мекунад.

---

## 3. Callback бо коркарди массивҳо

```js
let ададҳо = [1, 2, 3, 4, 5];

function нишонДодан(арзиш) {
    console.log(арзиш * 2);
}

ададҳо.forEach(нишонДодан);
```
📌 **Тавзеҳ:** Функсияи `нишонДодан` ҳамчун callback ба `forEach` дода шудааст, ки барои ҳар як элемент онро иҷро мекунад.

---

## 4. Callback Hell (Мушкилоти callback)

Агар callback-ҳо зиёд бошанд, код мураккаб ва номафҳум мешавад. Инро **callback hell** меноманд:

```js
setTimeout(() => {
    console.log("Қадами 1");
    setTimeout(() => {
        console.log("Қадами 2");
        setTimeout(() => {
            console.log("Қадами 3");
        }, 1000);
    }, 1000);
}, 1000);
```
📌 **Тавзеҳ:** Ин код бо истифода аз **Promise** ё **async/await** соддатар мешавад.

---

📚 **Хулоса:** Callback як воситаи пурқувват барои иҷрои код дар вақти мувофиқ мебошад, аммо метавонад боиси мураккабии код гардад. Барои ҳалли ин мушкилот, **Promise** ва **async/await** истифода мешаванд.

🚀 *Callback-ҳоро дуруст истифода баред ва коди худро тоза нигоҳ доред!*


![image](https://github.com/user-attachments/assets/033e5797-f9a6-49cf-980b-0a7be02d1243)
