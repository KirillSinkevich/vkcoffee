## vkcoffee
Это шифровщик и расшифровщик VK Coffee сообщений.
## Установка
npm install vkcoffee
## Использование:
```javascript
const vkcoffee = require('vkcoffee');

// шифровка:
var cryptedMessage = vkcoffee.encrypt('сообщение');
// Получаем "VK CO FF EE 54 4C 4F 48 73 4D 61 56 77 4A 33 77 37 37 65 54 58 6C 4B 6F 72 79 46 2F 76 77 42 47 39 2F 44 70 78 76 70 4E 51 47 58 76 64 4C 49 3D VK CO FF EE"
// его уже можно послать другу и без ключа он сможет его расшифровать

// VK Coffee поддерживает от 4 до 16 цифр.
var cryptedMessWithKey = vkcoffee.encrypt('сообщение2', 35368);
// Получаем "VK C0 FF EE 39 64 61 65 54 49 64 45 68 47 41 43 4D 32 67 49 51 7A 59 31 58 38 78 47 51 35 42 4C 51 66 41 62 6A 47 30 53 2F 34 4C 35 6A 41 6F 3D VK C0 FF EE"
// его можно отправить другу, сообщив код, в моем случае это 35368
// и после расшифровки он увидит "сообщение2"

// расшифрока:
var encryptedMessage = vkcoffee.decrypt(cryptedMessage);
// Получаем "сообщение"

var encryptedMessWithKey = vkcoffee.decrypt(cryptedMessWithKey, 35368);
// получаем "сообщение2"
```
