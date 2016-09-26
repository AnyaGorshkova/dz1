#Учебная сборка Loftschool (выпускной проект №1) 

Stack:
 - Gulp 4.0
 
Getting started:

1. clone this repo
2. cd path/to/
3. npm install gulpjs/gulp-cli -g  // Install the latest Gulp CLI tools globally
4. npm install
6. run "gulp" command to start


##Горшкова Анна Юрьевна, домашее задание №1

Добавила:

1. Таск для генерации спрайтов из графических файлов png и gif

	- установила плагин для генерации спрайтов - npm i gulp.spritesmith --save-dev
	- создала файл sprite.png.js с описанием таска (находим файлы с расширением png и gif в директории source/images/icons, запускаем gulp.spritesmith с параметрами, сохраняем полученный спрайт в папке build/assets/img/sprite, полученный scss файл - в папке /source/style/common. Полученный scss файл с помощью импорта подключается к app.scss)
	- в файле path/task.js прописала путь до файла с таской
	- подключила созданный таск к общей сборке в файле gulpfile.js

2. Таск для копирования шрифтов из папки с исхониками в папку для продакшена

	- создала файл copy.fonts.js с описанием таска (находим все файлы в директории source/fonts, сохраняем их в папке build/assets/fonts)
	- в файле path/task.js прописала путь до файла с таской
	- подключила созданный таск к общей сборке в файле gulpfile.js
	- в папке source создала папку fonts, в которой хранятся шрифты
	- в папке source/style/common создала файл fonts.sass, 	который с помощью импорта подключается к app.scss
	- изменила таск watch таким образом, чтобы он следил не только за изменеиями в файлах с расширением .scss, но и с расширением .sass, а также отслеживал изменения в папке со шрифтами. В случае добавления нового шрифта в папку с исходниками, он копируется в папку для продакшена
