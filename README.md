# Random Color Gradient Generator Library in JavaScript / Библиотека для генерации случайных цветовых градиентов на JavaScript

**RU**: Эта библиотека позволяет генерировать случайные цветовые градиенты, которые можно использовать в веб-приложениях. Она написана на чистом JavaScript и не требует дополнительных зависимостей.  
**ENG**: This library allows you to generate random color gradients that can be used in web applications. It is written in pure JavaScript and does not require any additional dependencies.

## Installation / Установка

**RU**: Сохраните следующий код в файл `gradientGenerator.js`:

```javascript
// gradientGenerator.js

class GradientGenerator {
    static getRandomColor() {
        const letters = '0123456789ABCDEF';
        let color = '#';
        for (let i = 0; i < 6; i++) {
            color += letters[Math.floor(Math.random() * 16)];
        }
        return color;
    }

    static generateRandomGradient() {
        const color1 = this.getRandomColor();
        const color2 = this.getRandomColor();
        const angle = Math.floor(Math.random() * 360);
        return `linear-gradient(${angle}deg, ${color1}, ${color2})`;
    }
}
```

**ENG**: Save the following code in a file named `gradientGenerator.js`:

```javascript
// gradientGenerator.js

class GradientGenerator {
    static getRandomColor() {
        const letters = '0123456789ABCDEF';
        let color = '#';
        for (let i = 0; i < 6; i++) {
            color += letters[Math.floor(Math.random() * 16)];
        }
        return color;
    }

    static generateRandomGradient() {
        const color1 = this.getRandomColor();
        const color2 = this.getRandomColor();
        const angle = Math.floor(Math.random() * 360);
        return `linear-gradient(${angle}deg, ${color1}, ${color2})`;
    }
}
```

**RU**: Или же вы просто можете скачать файл `gradientGenerator.js` из этого репозитория и использовать его в своем проекте.  
**ENG**: Or you can just download a file named `gradientGenerator.js` from this repository and use it in your project.

## Usage / Использование

**RU**: Для использования этой библиотеки вам необходимо будет добавить в ваш HTML файл следующую часть кода:

```html
<script src="gradientGenerator.js"></script>
<script>
    // Устанавливаем случайный градиент в качестве фона
    document.body.style.background = GradientGenerator.generateRandomGradient();
</script>
```

**ENG**: To use this library, you need to add the following code part in your HTML file:

```html
<script src="gradientGenerator.js"></script>
<script>
    // Set a random gradient as the background
    document.body.style.background = GradientGenerator.generateRandomGradient();
</script>
```
