# CRIAR E CONFIGURAR O LAZY LOAD NO ANGULAR

1. Instale a extensão Angular Schematics em seu VsCode, pesquisando o nome 'Angular Schematics' e clicando em install(EUA) OU Instalar(BRA).
![image](https://user-images.githubusercontent.com/65187931/191623675-019fd785-6091-43c5-8ebe-dcf746fcc9d4.png)

2. Ao criar um projeto angular, crie a pasta com o nome modulos na do diretório app/ 
![image](https://user-images.githubusercontent.com/65187931/191624403-9c99395a-8904-4629-b70a-17ef3db3e8a9.png)


3. Clique com o botão direito do mouse em cima dessa pasta e navege até a opção 'Angular: Generate a Module'.
![image](https://user-images.githubusercontent.com/65187931/191624685-6c945ee4-9c3f-47d2-9276-f2d0307454cc.png)
> Se a extensão já estiver instalada, e a opção 'Angular: Generate a Module' não aparecer, para solucionar o problema tente reinstalar a extensão 
 'Angular Schematics', e em seguida rode o comando no terminal prompt de comando ou gitbash dentro do diretório do projeto angular criado: 
```
npm install
```
![image](https://user-images.githubusercontent.com/65187931/191627110-19028a4f-ff75-4a10-9360-843824a9e47b.png)

4. Digite um nome para este módulo:
![image](https://user-images.githubusercontent.com/65187931/191625348-36f706e9-456e-4738-b743-b0ecb898d660.png)

5. Depois, escolha a opção 'Lazy-loaded module of pages':
![image](https://user-images.githubusercontent.com/65187931/191625532-6321e4ef-092e-480b-960c-854593e116d1.png)
>Se o módulo for criado corretamente, deverá aparecer no explorador de arquivos do VsCode a pasta com o nome escolhido, nesse exemplo a pasta com 
o nome 'inicial' dentro da pasta modulos contendo os 6 arquivos gerados automáticamentes com o a criação do módulo.
![image](https://user-images.githubusercontent.com/65187931/191627666-abf81575-52d6-4e68-ac4c-6b142c7dd966.png)

6.Crie um componente para testar o carregamento Lazy Load. Para isso, 
clicar com o botão direito em cima da pasta app no explorador de arquivos e navegar até a opção 'Angular: Generate a Component' e escolher o diretório e o nome do      componente, neste exemplo, será criado um componente com o nome home e criado com o diretório app/views/home.


