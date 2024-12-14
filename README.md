# README

## About

基于 Vue3 + Vite2 + Wails 的项目模板。
仅仅写了一个主页附带工具栏和侧边栏，方便二次开发一些小应用。





This is the official Wails Vue template.

You can configure the project by editing `wails.json`. More information about the project settings can be found
here: https://wails.io/docs/reference/project-config

## Live Development

To run in live development mode, run `wails dev` in the project directory. This will run a Vite development
server that will provide very fast hot reload of your frontend changes. If you want to develop in a browser
and have access to your Go methods, there is also a dev server that runs on http://localhost:34115. Connect
to this in your browser, and you can call your Go code from devtools.

## ![效果](.\效果.png)Building

To build a redistributable, production mode package, use `wails build`.
