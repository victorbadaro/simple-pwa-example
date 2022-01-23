# 📱 simple-pwa-example
Este é um simples projeto como exemplo de contrução de uma aplicação **PWA** (Progressive Web App).

## ✨ Demo
![demo](https://user-images.githubusercontent.com/9096344/150696033-be1e48ec-14f2-4441-b990-739175ea24c8.gif)

## 👌 Instalação
Faça o clone do projeto para um diretório de sua preferência:
```bash
$ git clone https://github.com/victorbadaro/simple-pwa-example
```

## 🚀 Execução
Acesse o diretório do projeto:
```bash
$ cd simple-pwa-example
```
Execute o projeto:
```bash
$ npx serve
```
O comando acima utiliza o pacote [serve](https://github.com/vercel/serve) para iniciar um servidor com os arquivos estáticos da aplicação, mas você pode utilizar outros se quiser (como o [reload](https://github.com/alallier/reload) por exemplo).
Executando o comando acima (utilizando o pacote [serve](https://github.com/vercel/serve)) a seguinte mensagem aparecerá no terminal:

![image](https://user-images.githubusercontent.com/9096344/150695724-e1950d5d-12d3-4f3b-9008-c70d08ba54c0.png)

## 🛠 Passos para construir essa aplicação PWA
1. Criação dos arquivos estáticos (`index.html`, `styles.css`, `logo.png`). _Para o arquivo `logo.png` tente utilizar uma resolução de 512x512_
2. Criação do arquivo `manifest.json` com a seguinte configuração
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
3. Criação dos ícones (necessário para aplicações PWA). Para facilitar a execução desse passo foi utilizado o pacote NPM [pwa-asset-generator](https://github.com/onderceylan/pwa-asset-generator)
    ```bash
    $ npx pwa-asset-generator logo.svg icons -i ./index.html -m ./manifest.json
    ```
    Esse comando irá criar os todos os ícones necessários para a aplicação e irá importá-los dentro dos arquivos `index.html` e `manifest.json`. Os ícones serão disponibilizados dentro da pasta `icons`
4. Criação do arquivo `serviceWorker.js`

---

<p align="center">Este projeto foi criado e desenvolvido com ❤ por <a href="https://github.com/victorbadaro">Victor Badaró</a></p>