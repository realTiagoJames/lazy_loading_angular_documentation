<h1 align="center">CRIAR E CONFIGURAR O LAZY LOAD NO ANGULAR</h1>

1. Instale a extensão Angular Schematics em seu VsCode, pesquisando o nome 'Angular Schematics' e clicando em install(EUA) OU Instalar(BRA).
![image](https://user-images.githubusercontent.com/65187931/191623675-019fd785-6091-43c5-8ebe-dcf746fcc9d4.png)

2. Ao criar um projeto angular corretamente, crie a pasta com o nome modulos na do diretório app/ 
![image](https://user-images.githubusercontent.com/65187931/191624403-9c99395a-8904-4629-b70a-17ef3db3e8a9.png)


3. Clique com o botão direito do mouse em cima dessa pasta e navege até a opção 'Angular: Generate a Module'.
![image](https://user-images.githubusercontent.com/65187931/191624685-6c945ee4-9c3f-47d2-9276-f2d0307454cc.png)
> Se a extensão já estiver instalada, e a opção 'Angular: Generate a Module' não aparecer, para solucionar o problema tente reinstalar a extensão 
 'Angular Schematics', e em seguida rode o comando no terminal prompt de comando ou gitbash dentro do diretório do projeto angular criado: 
```
npm install
```
![image](https://user-images.githubusercontent.com/65187931/191627110-19028a4f-ff75-4a10-9360-843824a9e47b.png)

4. Digite um nome para este módulo e pressione enter:
![image](https://user-images.githubusercontent.com/65187931/191625348-36f706e9-456e-4738-b743-b0ecb898d660.png)

5. Depois, escolha a opção 'Lazy-loaded module of pages' pressione enter e depois confirme:
![image](https://user-images.githubusercontent.com/65187931/191625532-6321e4ef-092e-480b-960c-854593e116d1.png)
>Se o módulo for criado corretamente, deverá aparecer no explorador de arquivos do VsCode a pasta com o nome escolhido, nesse exemplo a pasta com 
o nome 'inicial' dentro da pasta modulos contendo os 6 arquivos gerados automáticamentes com o a criação do módulo.
![image](https://user-images.githubusercontent.com/65187931/191627666-abf81575-52d6-4e68-ac4c-6b142c7dd966.png)

6. Crie um componente para testar o carregamento Lazy Load. Para isso, 
clicar com o botão direito em cima da pasta app no explorador de arquivos e navegar até a opção 'Angular: Generate a Component' e escolher o diretório e o nome do      componente, neste exemplo, será criado um componente com o nome home e criado com o diretório app/views/home e pressionado enter.
![image](https://user-images.githubusercontent.com/65187931/191628705-3e74cb82-9182-47e2-99cc-43772c7a31c3.png)

7. Escolha a opção padrão 'Default component' e depois confirme:
![image](https://user-images.githubusercontent.com/65187931/191628928-9b4fe613-3732-4ae7-865a-382a8f37b7b3.png)

8. Transferir(recortar e colar) 'HomeComponent' de declarations e o import {HomeComponent} de app.module.ts para o inicial.module.ts, ficando assim:
> Ao fazer isso, certificar-se de que apagou essa respectiva declarações e import de app.module.ts para que fique somente em inicial.module.ts.
![image](https://user-images.githubusercontent.com/65187931/191629638-9c662579-0327-4eef-ad71-48567910ff3a.png)

9. No arquivo inicial-routing.module.ts substitua a chamada do componente InicialComponent para o 'HomeComponent' e importe o este componente nos imports acima no formato import { HomeComponent } from ......  , em seguida apague o importe do componente InicialComponent que não será utilizado. Ficando assim:
![image](https://user-images.githubusercontent.com/65187931/191630289-b6826e41-c595-4b5e-b9c5-1b3d4431f5bb.png)

10. Edite o arquivo app-routing.module.ts para quando o endereço estiver vazio depois de '/'(barra), carregar o módulo 'inicial':
![image](https://user-images.githubusercontent.com/65187931/191630805-2988d285-7f36-4d60-b0d8-f460b7dae740.png)
```
  {
    path: '',
    redirectTo: '/inicial',
    pathMatch: 'full'
  }
```
11. Em seguida, no arquivo app.component.html exclua todo o código gerado automático com a criação do projeto angular, cole o código abaixo e salve:
```
<router-outlet></router-outlet>
```
>Nesse ponto a aplicação já está configurada para mostrar o componente home quando uando o endereço estiver vazio depois de '/'(barra).

12. Então para iniciar o servidor da aplicação, rode o comando no terminal prompt de comando ou gitbash dentro do diretório do projeto angular criado:
```
ng serve
```
Se não estiver rodando nenhuma outra aplicação, o projeto abrirá na porta padrão http://localhost:4200/ no browser.
![image](https://user-images.githubusercontent.com/65187931/191631490-5da0fef2-42bd-4d44-8fe9-c39cf1e17d43.png)

Nesse ponto deve aparecer a página home com a mensagem 'home works!' ao abrir http://localhost:4200/  no browser.
![image](https://user-images.githubusercontent.com/65187931/191632449-45e3f10c-107b-45cb-9f36-8286aad250d1.png)


# Links úteis:

- Baixar o [VS Code](https://code.visualstudio.com/download);
- Orientações do marketplace.visualstudio para [Angular Schematics](https://marketplace.visualstudio.com/items?itemName=cyrilletuzi.angular-schematics);
- Requirementos and solução de porblemas da extentsão [troubleshooting](https://github.com/cyrilletuzi/vscode-angular-schematics/blob/main/walkthroughs/troubleshooting.md);
- Instalação do NodeJs com gerenciador de versões [NVM](https://github.com/coreybutler/nvm-windows/edit/master/README.md);
- Instalação do [Angular CLI](https://angular.io/cli);
- Documentação oficial do [Lazy-Loading](https://angular.io/guide/lazy-loading-ngmodules);




