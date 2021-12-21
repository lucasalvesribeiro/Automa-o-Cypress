**Passo-a-passo Implantação Cypress**
---

1. Criar pasta no C\ 

2. Criar outra pasta dentro da criada anteriormente

3. Entrar dentro da pasta pelo git bash

4. Executar comando ‘npm init’ - serve para criar o pacote do nosso projeto ou
 ‘npm init -y’ - jeito rápido de criar pacote do projeto 

5. Na opção ‘test command': colocar o comando que vc quer para que sempre que for executar os testes ele deve ser chamado e abrir o cypress

6. Acessar url do projeto do git de automação

7. Clonar projeto com o comando 'git clone'

8. Colocar usuário e senha do gitlab quando for solicitado; Obs: o código de verificação deve estar desativado para isso.

9. Dar o comando ‘Code  .’ para entrar no projeto pelo Visual Studio e deve estar já criada uma pasta chamada  ‘package.json’

10. Executar o comando que foi colocado executar os testes e abrir o cypress

11. O sistema irá  criar a pasta do cypress automaticamente

12. No git bash, dar o comando ‘git checkout end-to-end’

13. Feito!

14. Ignorar arquivos do Projeto que sobrecarregam o repositório com informações que não precisam ser guardadas

15. Criar arquivo na pasta raiz do projeto com o nome ‘.gitgnore’

16. Dentro desse arquivo, colocar os seguintes itens:

- .Ds_Store
- cypress.env.json
- cypress/screenshots
- cypress/videos
- node_modules 

16.1. Explicação dos itens colocados no arquivo:

- .Ds_Store - Diz para englobar as config da sua máquina 
- cypress.env.json - Arquivo dos dados sensíveis 
- cypress/screenshots - Caminho aonde grava video q pega a pasta screenshots
- cypress/videos - Caminho aonde grava video q pega a pasta videos
- node_modules 

17. Criar pasta chamada ‘cypress.env.json’ onde se coloca os dados sensíveis, exemplo é seu usuário e senha do portal.

18. Na pasta ‘cypress.json’ que já vem criada, colocar os dados de confg padrões do cypress:

- “baseUrl”: “url do site”
- “defaultCommandTimeout”: “colocar o tempo” 
- “viewportHeight”: “Colocar tamanho”
- “viewportWidth”: “Colocar tamanho”
	
18.1. Explicação dos itens acima:

- “baseUrl”: “url do site” - Especifica a URL que vai ser testada
- “defaultCommandTimeout”: “colocar o tempo” - serve para especificar o tempo que o cypress vai ter para fazer as ações, se colocado 40000, ele vai tentar por 4seg fazer aquela ação, senão vai dar erro
- “viewportHeight”: “Colocar tamanho” - Serve para colocar o tamanho da tela do cypress 
- “viewportWidth”: “Colocar tamanho” - Serve para colocar o tamanho da tela do cypress 

19. Dentro da pasta ‘integrations’, criar um arquivo chamado ‘nomeqtuquer.spec.js’, que seria onde vai ficar os cenários de teste propriamente ditos da tela que tu via especificar no nome do arquivo. Obs: Como já foi clonado o projeto, esses arquivos já estão criados.

20. Dentro das novas pastas criadas, sempre iniciar colocando:

'/// <reference types=”Cypress” />'
 
21. Depois disso, é só criar suas estruturas de teste.
 
22. Dentro da pasta ‘index.js’, colocar:
 
- import ‘./nomedasuapastadecomandos’

Obs: ela importa seus comandos customizados para que possam ser usados nos cenários de teste.
 
Fim!

