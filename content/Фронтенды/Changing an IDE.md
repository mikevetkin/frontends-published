---
author: Михаил Веткин
date: 2024-07-30
---
![[vscode red.png]]
## Введение

По разным причинам, которые известны лишь... всем, программисты в России всё меньше пользуются WebStorm. Недавно ко мне пришли ребята с вопросом, как жить на VS Code. Они знали, что несмотря на возможность установить корпоративный WebStorm, я оставался приверженцем бесплатного vscode.

Эта заметка составлена из сообщений, в которых я рассказывал, как использую VS Code.

Надеюсь, она будет полезна тем разработчикам, которые сейчас находятся в состоянии фрустрации. Многие сидели на PyCharm и CLion ещё с универа. Взять и резко сменить инструмент на что-то другое непросто.

~~JetBrains давал бесплатные лицензии, чтобы подсадить ни о чём не догадывающихся студентов на капиталистическую иглу платных подпи... Проклятые капиталисты, они меня до могилы доведут!~~

Короче, факт остаётся фактом, Джетбрейнс больше нет. Но мы не какие-то там пфф... любители! И можем собрать IDE из чего угодно! А самый быстрый и простой способ - это установить VS Code и накинуть на него плагины.

## Плагины

- Какие-то базовые вещи
	- [Better Comments](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments) - симпотно подсвечивает комменты с TODO, ?, !;
	- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens) - работа с git;
	- [GitGraph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph) - работа с графом git;
	- [Git changelists manager](https://marketplace.visualstudio.com/items?itemName=Aktyn.git-changelists-manager) - полезно, когда подсовываешь, какие-то данные для работы, которые не должны оказаться в истории гита, например, хэши или временные стабы для разработки, экран какой-то надо врубить в сложном флоу;
	- [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced) - можно смотреть прёвью MD файлов;
	- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode) - форматировние кода на кнопку или при сохраненнии. Это не только JS тема, может быть полезно для GraphQL, JSON штук;
	- [Material Icon Theme](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme) - в боковом меню файлам и папкам с определёнными именами будет присвоен значок;
	- [Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker) - проверяет грамотность на инглише, с банковскими терминами мастхэв;
	- [Russian Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker-russian) - то же, но для русского языка;
	- [Batch Rename](https://marketplace.visualstudio.com/items?itemName=JannisX11.batch-rename-extension) - когда скопом нужно что-то переименовать;
	- [Live Share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare) - шарить свой код и прогать вместе;
	- [Bookmarks](https://open-vsx.org/vscode/item?itemName=alefragnani.Bookmarks) - когда нужно тыкаться в несколько мест в большой кодовой базе и не забыть, куда тыкался;
	- [DotENV](https://open-vsx.org/vscode/item?itemName=mikestead.dotenv) - подсветка синтаксиса для .env файлов;
- Front-end
	- [Pretty TypeScript Errors](https://open-vsx.org/vscode/item?itemName=yoavbls.pretty-ts-errors) - человекочитаемые TypeScript ошибки;
	- [Javascript Booster](https://marketplace.visualstudio.com/items?itemName=sburg.vscode-javascript-booster) - всякие полезности для JS косметического рефакторинга;
	- [CodeMetrics](https://marketplace.visualstudio.com/items?itemName=kisstkondoros.vscode-codemetrics) - считает цикломатическую сложность и количество строк кода, подсвечивает те методы, у которых метрика отстойная. То есть его нужно переписать, разбить, упростить;
	- [Jest Runner](https://marketplace.visualstudio.com/items?itemName=firsttris.vscode-jest-runner) - жизненно необходимо при TDD, ты переписываешь код, при сохранении сразу же видишь, что тесты зеленеют и двигаешься дальше;
- Back-end
	- [Go](https://marketplace.visualstudio.com/items?itemName=golang.Go) - поддержка Go;
	- [Go struct tag](https://marketplace.visualstudio.com/items?itemName=liuchao.go-struct-tag) - заполнятор тэгов для структур, полезно для мапинга в json, например;
	- [GraphQL: Language Feature Support](https://marketplace.visualstudio.com/items?itemName=GraphQL.vscode-graphql) - валидация и автокомплит;
	- [GraphQL: Syntax Highlighting](https://marketplace.visualstudio.com/items?itemName=GraphQL.vscode-graphql-syntax) - подсвечивает синтаксис для GraphQl;
	- [SQLTools](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools) - менеджер БД;
	- [SQLTools PostgreSQL/Cockroach Driver](https://marketplace.visualstudio.com/items?itemName=mtxr.sqltools-driver-pg) - вместе с предыдущим заменяют DataGrip от JetBrains;
- AI
	- [IntelliCode](https://marketplace.visualstudio.com/items?itemName=VisualStudioExptTeam.vscodeintellicode) - всякие подсказки, которые берутся прямо из GitHub;
	- [Tabnine](https://marketplace.visualstudio.com/items?itemName=TabNine.tabnine-vscode) - очень мощный Ai генератор. Мне лично задачи стало в два раза быстрее делать;
	- [Codeium](https://marketplace.visualstudio.com/items?itemName=Codeium.codeium) - AI автоподсказки, чат и помощник в рефакторинге;
- Для новоприбывших c WebStorm
	- [JetBrains IDE Keymap](https://marketplace.visualstudio.com/items?itemName=isudox.vscode-jetbrains-keybindings) - всем, кто привык к шорткатам. Вообще, в [документации](https://code.visualstudio.com/docs/getstarted/keybindings#_keymap-extensions) есть шорткаты и из других редакторов;
	- [JetBrains Icons Enhanced](https://marketplace.visualstudio.com/items?itemName=BrennonDenny.vsc-jetbrains-icons-enhanced) - иконки;
	- [JetBrains Mono](https://marketplace.visualstudio.com/items?itemName=NarasimaPandiyan.jetbrainsmono) - шрифт Mono;
	- [JetBrains Darcula Theme](https://marketplace.visualstudio.com/items?itemName=Anan.jetbrains-darcula-theme) - привычная цветовая палитра;

## Про merge-конфликты

Я использую для этого уже очень давно [Sublime Merge](https://www.sublimemerge.com/), но есть восьмиминутное [видео](https://youtu.be/HosPml1qkrg?si=TuxpEpkJ0vlLQqIM) с официального канала vscode, которое должно закрыть 90% вопросов того, как это делать прямо в IDE.

## Ещё Штуки

Vscode в проектах смотрит в папку `.vscode`, где есть разные конфиги специфические для проекта.

Я кладу к проектам тему, которую хочу на них использовать. Чтобы можно было быстро переключаться между проектами и на уровне подсознания ориентироваться, где ты сейчас находишься. Мне лично сильно помогает при чтении кода.

![[CodeThemeSwitcher.mp4]]

Для этого в `.vscode/settings.json` нужно положить:

```json
{
	"workbench.colorTheme": "Aurora X", // Цветовая тема
}
```

## Горячие клавиши

Майкрософт написали неплохую [документацию](https://code.visualstudio.com/docs/getstarted/keybindings) на эту тему и подсказки для [Macos](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf) и [Windows](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf). От себя добавлю, что я чаще всего использую эти шорткаты:

- `f2` - переименовать переменную;
- `cmd + d` - найти совпадения в файле и поставить каретку;
- `alt + click` - расставляет каретки в выбранные места;
- `cmd + p` - найти какой-либо файл;
- `cmd + b` - скрыть/показать панель навигации;
- `cmd + w` - закрыть таб;
- `cmd + j` - открыть терминал;
- `cmd + \` - разделить файл на несколько редакторов;

## Пара слов о том, почему мне норм на VS Code

Мой первый редактор я открыл для себя в 14 лет. Это был стандартный блокнот windows, на нём я написал свой первый [сайт](http://mihaelvetkin.narod.ru), и его функционала было для меня более, чем достаточно.

Кстати, из-за того, что Narod перешёл к Ucoz я так и не смог вернуть доступ к личному кабинету и он, кажется, навсегда остался в интернете. Вы можете зайти и покринжевать с того, какие я тогда писал амбициозные слоганы и выставлял внушающие ценники на разработку.

В школе мы писали на Notepad++ и turboPascal. Подсветка ключевых слов это уже было большое продвижение.

Позже я открыл для себя Adobe Dreamweaver, но действительно надолго задержался на Sublime Text, который увидел в уроках "JavaScript Джедай" от Sorax.

Чёрт, как же это было хорошо! Нас всегда учили не судить о книге по обложке, но это было по-настоящему впервые красиво, быстро, удобно. Он был хорош всем:

- подсветка синтаксиса;
- поддержка vim;
- конфиг настроек в одном файле;
- куча кастомных тем.

Его не нужно было крякать, особо разбираться, как он устроен, просто пиши код.

Позже в Политехе чего только не было. Пришлось вернуться к TurboPascal, попробовать XCode и Eclipse, MS Visual Studio, nano, vim. Но в домашних проектах я всё равно использовал Sublime Text.

Когда я пришёл на свою первую работу, мне предложили установить VS Code. Моя реакция была что-то типа:

>[!quote]
>Это та хрень с лабораторных у Молодякова? Ни за что.

Мне объяснили, что это вообще другой продукт, и по сути, похож во много м на Sublime, только есть тонна полезных плагинов. Я подумал: "Почему бы и нет", - и на 5 лет завис в этом редакторе.

Подводя итог, хочу сказать, что я не особо прихотлив в выборе IDE. Не исключено, что и от VS Code придётся отказаться, но для разработчика, дизайнера, просто ищущего человека это никогда не будет проблемой.

## Neovim

Ещё рекомендую ознакомиться со статьями Алексея Агапова про то, как он пробовал перейти с Xcode на Neovim:
- https://t.me/agposdev/58
- https://t.me/agposdev/65
- https://t.me/agposdev/68
- https://t.me/agposdev/69

## Вдохновляют
- Свобода от продуктов по подписке и мощь свободного программного обеспечения
- Клинт Иствут и Серджио Леоне

## Тэги
#фронтенды #инструменты #vscode #IDE #плагины