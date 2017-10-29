# vue2-schoolofnet


***Procedimento para execução do projeto***

No diretório do projeto executar os comandos abaixo:

npm run dev


***Passos executados durante a configuração do projeto inicial***

Pre-requisito: ter instalados o nodejs e o npm

1) Instalar o vue-cli

npm -install -g vue-cli

2) No diretório do workspace inicializar o projeto com base em um template, neste caso webpack-simple

vue init webpack-simple vue-wp

3) Depois do projeto criado, entrar no diretório do projeto e executar npm install para instalar as dependências do projeto

npm install

4) Para executar o projeto, de forma direta e sem nenhuma alteração inicial, executar os comandos abaixo, que vão inicializar o servidor do WEbpack embutido na porta disponível

npm run dev

5) Quando necessário integração com o Bootstrap, instalar o mesmo através do npm

npm install bootstrap --save

6) Para que seja possível tratar as urls internas no css do bootstrap, é necessário instalar o url-loader

npm install url-loader --save-dev

7) É interessante instalar também um utilitário que nos permite trabalhar com estilos dentro do HTML com a tag style, sem usar a tag link

npm install style-loader --save-dev

8) Será necessário configurar o arquivo webpack.config.js para usar os loaders instalados


{
    test: /\.(woff|woff2|ttf|svg|eot)$/,
    loader: 'loader-url'
}

9) Necessário adicionar um plugin para o jQuery

plugins: [
    new webpack.ProviderPlugin({
        'jQuery': 'jquery'
    })
  ],


10) Instalar a biblioteca lodash para ordenação

npm install lodash --save
