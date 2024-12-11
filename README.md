# Random Color Gradient Generator Library in JavaScript/Библиотека для генерации случайных цветовых градиентов на JavaScript
RU: Эта библиотека позволяет генерировать случайные цветовые градиенты, которые можно использовать в веб-приложениях. Она написана на чистом JavaScript и не требует дополнительных зависимостей. n\
ENG: This library allows you to generate random color gradients that can be used in web applications. It is written in pure JavaScript and does not require any additional dependencies.

## Installation
RU: Сохраните следующий код в файл `gradientGenerator.js`: n\
ENG: Save the following code in a file named `gradientGenerator.js`:

```javascript
// gradientGenerator.js

(function() {
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

    // Экспортируем класс для использования в других скриптах
    window.GradientGenerator = GradientGenerator;
})();
