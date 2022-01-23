# 📱 simple-pwa-example
This is a simple example of a PWA (Progressive Web App) application.

## ✨ Demo
![demo](https://user-images.githubusercontent.com/9096344/150696033-be1e48ec-14f2-4441-b990-739175ea24c8.gif)

## 👌 Install
Clone this project to a directory of your choice:
```bash
$ git clone https://github.com/victorbadaro/simple-pwa-example
```

## 🚀 Run
Access the project directory:
```bash
$ cd simple-pwa-example
```
Run the app:
```bash
$ npx serve
```
The above command uses the [serve](https://github.com/vercel/serve) package to start a server with all the static files of this project. You can use other packages if you want (like [reload](https://github.com/alallier/reload) for example).
Running the command above (using the [serve](https://github.com/vercel/serve) package) the following message will be shown in the terminal:

![image](https://user-images.githubusercontent.com/9096344/150695724-e1950d5d-12d3-4f3b-9008-c70d08ba54c0.png)

## 🛠 Steps to build this PWA application
The following files and folders were created or generated:
1. Static files (`index.html`, `styles.css`, `logo.png`). _Try to use 512x512 resolution for the `logo.png` file_
2. `manifest.json` file as it is be shown below
    ```json
    {
        "id": "/?home=true",
        "name": "PWA Example",
        "short_name": "PWA Example",
        "start_url": "/?home=true",
        "theme_color": "#fff",
        "background_color": "#333",
        "display": "fullscreen",
        "orientation": "portrait"
    }
    ```
3. The app icons (this is necessary for PWA applications - no too much, but still necessary). It's super simple to complete this step by using the [pwa-asset-generator](https://github.com/onderceylan/pwa-asset-generator) package.
Run on your terminal:
    ```bash
    $ npx pwa-asset-generator logo.svg icons -i ./index.html -m ./manifest.json
    ```
    This command will create all the necessary files for the app and it will import them into the `index.html` and `manifest.json` files. The icons will be available in the `icons/` folder
4. `serviceWorker.js` file

---

<p align="center">This project was created and developed with ❤ by <a href="https://github.com/victorbadaro">Victor Badaró</a></p>
