# Teste Programador Backend Sênior
Teste destinado aos candidatos a vaga de Programador Backend <b>Sênior</b>. Se o seu nível é outro, por favor, dê uma olhada nos demais repositórios e escolha o que se adequa a sua skill. 

## Descrição
Um cliente chamado Bruce Wayne nos contratou para fazer um sistema com o objetivo de catalogar os super-heróis existentes.
</br>
Parece uma missão difícil, mas, não se preocupe, o seu papel não será o de sair por aí procurando por heróis, vamos deixar isso para o Sr. Wayne...
</br>
Seu papel é desenvolver uma API com as operações básicas de cadastro de um herói e algum mago (coff, coff) do front-end fará as telas.
</br>

## Requisitos
Bom, aqui começa a explicação do que você terá que nos entregar. Leia com atenção.
</br>
Ah, o Alfred (acho que ele é tipo um mordono do Sr. Wayne) começou o projeto para nós e o esqueleto do projeto já existe.
</br>Dito isso vamos deixar uma lista com as tarefas:
- [x] Criar endpoint de criação de heróis respeitando os campos obrigatórios. ***Olhe o script SQL dentro do projeto para saber quais são os campos obrigatórios.***;
- [x] Criar endpoint de busca de heróis por ID. ***Caso não encontre o herói o sistema deve retornar um erro 404 (Not Found)***;
- [x] Criar endpoint de busca de heróis por filtro, nesse caso o filtro será apenas o nome. ***Caso não encontre nenhum herói o sistema deve retornar um sucesso 200 com o body vazio***;
- [x] Criar endpoint de atualização de heróis, todos os campos poderão ser atualizados. ***Caso não encontre o herói o sistema deve retornar um erro 404 (Not Found)***;
- [x] Criar endpoint de exclusão de heróis. A exclusão será física, ok? (Física?! É, deleta o registro da base). ***Caso não encontre o herói o sistema deve retornar um erro 404 (Not Found)***;
- [x] Criar testes unitários e de integração das funcionalidades desenvolvidas. ***As classes de teste unitário terminam com o prefixo `Test.js` e as classes de teste de integração terminam com `IT.js`. Temos um modelo de classe de exemplo dentro do projeto***;
- [x] O sistema deverá ter no mínimo 2 instâncias com carga balanceada através de alguma técnica de Round Robin;
- [x] As máquinas do cluster devem ser passíveis de monitoramento. (Ex: express-healthcheck);
- [x] As chamadas para o banco de dados deverão ser cacheadas por alguma ferramenta de cache distribuído; 
- [x] Criar um `docker-compose.yml` funcional para execução da aplicação. (Banco de Dados + API).

Ah, tem algo mais! O Sr. Wayne nos pediu para criar um endpoint onde ele possa selecionar dois heróis e comparar seus atributos força, agilidade, dextreza e inteligência. Como resultado, o sistema deve retornar um objeto contendo os id's e a diferença dos atributos (positivo se maior, negativo se menor) de cada herói. Dá uma pensada em como vai ficar esse objeto e o caminho do endpoint, tudo bem?
<p>
Agora sim, terminamos! Se você nos entregar isso que pedimos garanto que o Sr. Wayne vai pirar!!!

## Considerações
Leia essas instruções para ganhar tempo no desenvolvimento, ok? ;)
</br>
#### Primeiro Passo
Como primeiro passo faça um ***fork*** desse projeto na sua conta do GitHub é assim que iremos avaliar sua prova!</br>
***Não iremos avaliar provas que não estejam nesse padrão, então MUITA ATENÇÃO nessa dica.***
#### Configurações
- NodeJS 12.16+ instalado;
- NPM na versão 6.13+ instalado;
- IDE pode ser o de preferência, mas gostamos bastante do Visual Studio Code ou WebStorm;
- Docker e docker-compose instalados.

#### Testes
Para rodar os testes (unitários e de integração) utilize o comando a seguir:
```
npm run test
```

#### Bônus
Será considerado um plus os candidatos que entregarem:
- Uso de linter com bom padrão
- Bom uso dos padrões de REST;
- Uso de BDD para escrever os testes de integração;
- Uso de algum API Gateway para controle de rotas, trafêgo e resiliência da aplicação;
- O sistema ser capaz de se recuperar de falhas. (Circuit-Breaker);
- Monitoramento da aplicação por alguma ferramenta (Ex: Grafana);
