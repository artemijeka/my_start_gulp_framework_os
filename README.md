# install gulp guide

### work.artem.kuznecov.samara@yandex.ru
### 89608175048

### https://github.com/nodesource/distributions/blob/master/README.md
---
### (unix): 
  ***install nodejs and npm:***   
    ```
      sudo apt install curl  
      curl -fsSL https://deb.nodesource.com/setup_15.x | sudo -E bash -  
      sudo apt install -y nodejs  
      sudo apt install -y npm  
      node --version
      npm --version
      sudo apt autoremove
    ``` 
  ***install gulp:*** 
    ```
      npm i  
      sudo npm i gulp -g 
      gulp
    ```

### (windows):  
  ***install nodejs and npm:***   
    [https://nodejs.org/en/download/](https://nodejs.org/en/download/)  
  ***install gulp:***  
    ```
      npm i 
      npm i gulp -g  
      gulp 
    ```

### Ошибки:
  **Если ```gulp``` не запускается, то:**  
  ***Удалить:***
  ```
    node_modules
  ``` 
  ***и переустановить:***
  ```
    npm i
  ```

  **Если ```npm i``` не устанавливается, то:**
  ```
    # Update nodejs to latest version:
    sudo npm install -g n
    sudo n latest
    # Update npm to latest version:
    sudo npm install -g npm
    # Try npm install
    npm i
  ```

  **Ошибка: ```node-sass```** 
  ```
    gulp
    Error: Node Sass does not yet support your current environment: Linux 64-bit with Unsupported runtime (88)
    For more information on which environments are supported please see:
    https://github.com/sass/node-sass/releases/tag/v4.14.1
    at module.exports (/home/common/git_work/mida.ru/node_modules/node-sass/lib/binding.js:13:13)
    at Object.<anonymous> (/home/common/git_work/mida.ru/node_modules/node-sass/lib/index.js:14:35)
  ```
  ***Надо удалить:***
  ```
    npm uninstall gulp-sass -D
  ```
  ***И устанвоить:***
  ```
    npm i gulp-dart-sass -D
  ```
  ***gulpfile.js:***
  ```
    scss = require('gulp-dart-sass')
  ```