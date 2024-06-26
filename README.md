# Sistema para avaliação de disciplinas
Trabalho da disciplina Prática em Desenvolvimento de Software 

## Membros:
> Gabriela Moraes Miserani de Freitas - 2020006566 -> fullstack

> Isabella Vignoli Gonçalves - 2020006655 -> fullstack

> Raissa Miranda Maciel - 2020006965 -> fullstack

> Maria Luiza Leão Silva - 2020100953 -> fullstack

## Escopo
Criar um ambiente para avaliar as matérias ofertadas e os professores do Departamento de Ciencia da Computação(DCC) que as lecionaram em relação a vários atributos interessantes para os alunos no momento da escolha de disciplinas a se cursar no semestre. Este sistema evita a necessidade de procurar por outros estudantes que já cursaram a disciplina ao sumarizar as avaliações em uma só página.

## Principais features
> Página de cadastro/login

> Avaliar uma materia em relação a:
> * nota geral para disciplina (1 a 5 estrelas)
> * esforço extraclasse (pouco/médio/muito)
> * cobrança de presença
> * tipo de avaliação
> * didática/coerência do professor

> Filtrar as materias de acordo com horario/classificação/professor

> Ordenar matérias mais bem avaliadas 

## Tecnologias
> JavaScript

> NodeJS

> React

> MySQL

> Typescript

## Backlog do produto
> Como usuário, eu gostaria de me cadastrar no sistema

> Como usuário, eu gostaria de logar na minha conta

> Como usuário, eu gostaria de visualizar uma página para adicionar uma avaliação de uma disciplina (formulário)

> Como usuário, eu gostaria de avaliar a disciplina em relação à se cobra presença(sim ou não), didatica do professor(ruim, media, boa, otima), provas(fácil, médio, difícil), trabalhos(fácil, médio, difícil), tempo de dedicação extraclasse(pouco, medio, alto), nota geral da disciplina(1 a 5 estrelas)

> Como usuário, eu gostaria de deletar minha avaliação

> Como usuário, eu gostaria de ver a lista das disciplinas disponíveis

> Como usuário, eu gostaria de filtrar as materias por periodo

> Como usuário, eu gostaria de filtrar as materias por professor

> Como usuário, eu gostaria de filtrar as materias por dia e horário

> Como usuário, eu gostaria de ordenar as materias por avaliação

> Como usuário, eu gostaria de visualizar uma página com a visão geral de cada disciplina

> Como usuário, eu gostaria de poder adicionar um comentário ao final da minha avaliação

> Como usuário, eu gostaria de visualizar a resposta mais frequente para cada categoria da avaliação de uma disciplina

> Como usuário, eu gostaria de visualizar uma página com as informações gerais do professor

>  Como usuário, eu gostaria de ter um perfil

> Como usuário, eu gostaria de atualizar meu perfil

## Backlog da próxima sprint
### História #1: Como usuário, eu gostaria de me cadastrar no sistema
>>Tarefas e responsáveis:
>>>Instalar banco de dados e criar primeiras tabelas [Gabriela]
>>
>>>Instalar node.js [Gabriela]
>>
>>>Configurar o mySQL [Gabriela]
>>
>>>Criar e testar uma primeira rota usando o node.js [Maria]
>>
>>>Implementar versão inicial da tela de cadastro [Isabella]
>>
>>>Implementar no backend a lógica de criar uma nova conta [Maria]

### História #2: Como usuário, eu gostaria de logar na minha conta
>>Tarefas e responsáveis:
>>>Implementar versão inicial da tela de login [Raissa]
>>
>>>Implementar no backend a lógica de realizar login [Maria]
>>
>>>Integrar tela de login com a respectiva lógica no backend [Isabella]

### História #3: Como usuário, eu gostaria de ver a lista das disciplinas disponíveis
>>Tarefas e responsáveis:
>>>Implementar versão inicial da tela com as disciplinas disponíveis [Isabella]
>>
>>>Implementar no backend a lógica listagem das matérias [Gabriela]
>>
>>>Integrar tela com as disciplinas disponíveis com a respectiva lógica no backend [Raissa]
  
### História #4: Como usuário, eu gostaria de visualizar uma página com a visão geral de cada disciplina
>>Tarefas e responsáveis:
>>>Implementar versão inicial da tela geral da disciplina [Isabella]
>>
>>>Adicionar ementa, nome do professor, foto do professor, horário e link para página da máteria no DCC [Raissa]
>>
>>>Implementar no backend a lógica listagem das matérias [Maria]
>>
>>>Integrar tela com a respectiva lógica no backend [Isabella]

### História #5: Como usuário, eu gostaria de visualizar uma página para adicionar uma avaliação de uma disciplina 
>>Tarefas e responsáveis:
>>>Implementar versão inicial da tela de adicionar uma nova avaliação [Raissa]
>>
>>>Implementar no backend uma rota para uma página de nova avaliação [Gabriela]
>>
>>>Integrar tela de nova avaliação com a respectiva lógica no backend [Isabella]

### História #6: Como usuário, eu gostaria de avaliar a disciplina em relação à se cobra presença(sim ou não), didatica do professor(ruim, media, boa, otima), provas(fácil, médio, difícil), trabalhos(fácil, médio, difícil), tempo de dedicação extraclasse(pouco, medio, alto), nota geral da disciplina(1 a 5 estralas)
>>Tarefas e responsáveis:
>>>Implementar formulário [Raissa]
>>
>>>Implementar no backend a lógica de preecher o formulario com o backend/banco de dados [Maria]
>>
>>>Implementar a associação do formulario com o backend[Isabella]

### História #7: Como usuário, eu gostaria de visualizar a resposta mais frequente para cada categoria da avaliação de uma disciplina
>>Tarefas e responsáveis:
>>>Implementar na tela da disciplina uma tabela onde as respostas mais frequntes serão mostrados [Raissa]
>>
>>>Implementar no backend a lógica do cálculo para computar a resposta mais frequente [Gabriela]
>>
>>>Integrar a tabela com a respectiva lógica no backend [Isabella]

### História #8: Como usuário, eu gostaria de ordenar as materias por avaliação
>>Tarefas e responsáveis:
>>>Implementar na tela de listagem das disciplinas disponíveis um filtro para ordenação por nota de avaliação [Isabella]
>>
>>>Implementar no backend a lógica de ordenação por nota de avaliação [Maria]
>>
>>>Integrar filtro de ordenação com a respectiva lógica no backend [Raissa]

## Arquitetura adotada no Projeto

### Arquitetura Hexagonal

Para estabelecer uma separação clara entre o domínio e o restante do sistema e garantir uma melhor testabilidade o backend foi organizado em subpastas. Assim, foi criada a pasta domain para agrupar todas as classes de domínio, sendo elas: user, subject, teacher e review. Cada uma dessas classes foi desenvolvida dentro de uma pasta que separava a implementação dos controllores, do repository e do service. Dessa forma, a estrutura final do workspace com a arquitetura hexagonal implementada ficou da seguinte maneira:

![image](https://github.com/gmiserani/trabalho_pratico_pds/assets/62564311/a3aa8d05-49fe-4c2a-a4b4-68a04442abea)

#### Repository
Os repositories são responsáveis por realizar operações de acesso a dados, como criação e recuperação de registros, encapsulando a lógica de interação com o banco de dados. Um exemplo de como a implementação foi feita é mostrado a seguir:

![image](https://github.com/gmiserani/trabalho_pratico_pds/assets/62564311/15dc2bd8-dbfc-416b-81a0-496f71cb109d)

#### Controller
Os controllers recebem as requisições do cliente, invocam os serviços para processar os dados e retornam as respostas adequadas, gerenciando o fluxo de dados de entrada e saída. Um exemplo de como a implementação foi feita é mostrado a seguir:

![image](https://github.com/gmiserani/trabalho_pratico_pds/assets/62564311/6fcfcac8-60f9-4de2-86e6-7db78b7e40dd)

#### Service
Os services contêm a lógica de negócios da aplicação. Eles recebem dados dos controllers, aplicam as regras de negócios e utilizam os repositories para acessar ou manipular os dados no banco de dados. A separação da lógica de negócios nos services facilita a reutilização de código e a manutenção do sistema. Um exemplo de como a implementação foi feita é mostrado a seguir:

![image](https://github.com/gmiserani/trabalho_pratico_pds/assets/62564311/e7ac6231-3352-4e04-8f35-3ddec01f4048)

### Por que o sistema está adotando essa arquitetura?

O sistema está adotando essa arquitetura pois ela promove um desacoplamento e melhor flexibilidade no projeto, uma vez que a lógica de negócios se torna independente dos frameworks e interfaces utlizadas. Assim, a manutenção do código a testabilidade são melhoradas, tornando a criação de testes de unidade e de integração mais fácil. Além disso, a organização do projeto utilizando a arquitetura hexagonal permite que adaptadores e outros componentes sejam reutilizados ao longo da evolução do código e até mesmo em outros projetos.

### Quais são as portas e adaptadores? Qual o objetivo deles?

Na arquitetura hexagonal do projeto, os portos (interfaces) e adaptadores (implementações) desempenham papéis essenciais para garantir a modularidade e independência tecnológica. Os portos, representados pelos serviços (por exemplo, ReviewService.ts, SubjectService.ts), definem operações da lógica de negócios, permitindo que esta permaneça independente de detalhes técnicos. Já os adaptadores, como os controladores (ex.: ReviewController.ts, SubjectController.ts) e repositórios (ex.: ReviewRepository.ts, SubjectRepository.ts), implementam essas interfaces, traduzindo interações externas e persistência de dados para o domínio central.

O objetivo dos portos é garantir que a lógica de negócios esteja isolada das mudanças tecnológicas, enquanto os adaptadores permitem a comunicação com sistemas externos, como bancos de dados e interfaces de usuário. Essa estrutura promove um design de software mais flexível, testável e fácil de manter, facilitando a adição de novas funcionalidades sem impactar o núcleo do sistema.

![image](https://github.com/gmiserani/trabalho_pratico_pds/assets/62564311/5f983339-30fa-4553-819c-a0e2514d9b60)

## Backlog da Sprint (atualizado)

### História #1: Como usuário, eu gostaria de me cadastrar no sistema
>>Tarefas e responsáveis:
>>>Instalar banco de dados e criar primeiras tabelas [Gabriela]
>>
>>>Instalar node.js [Gabriela]
>>
>>>Configurar o mySQL [Gabriela]
>>
>>>Criar e testar uma primeira rota usando o node.js [Maria]
>>
>>>Implementar versão inicial da tela de cadastro [Isabella]
>>
>>>Implementar no backend a lógica de criar uma nova conta [Maria]

### História #2: Como usuário, eu gostaria de logar na minha conta
>>Tarefas e responsáveis:
>>>Implementar versão inicial da tela de login [Raissa]
>>
>>>Implementar no backend a lógica de realizar login [Maria]
>>
>>>Integrar tela de login com a respectiva lógica no backend [Isabella]

### História #3: Como usuário, eu gostaria de ver a lista das disciplinas disponíveis
>>Tarefas e responsáveis:
>>>Implementar versão inicial da tela com as disciplinas disponíveis [Isabella]
>>
>>>Implementar no backend a lógica listagem das matérias [Gabriela]
>>
>>>Integrar tela com as disciplinas disponíveis com a respectiva lógica no backend [Raissa]
  
### História #4: Como usuário, eu gostaria de visualizar uma página com a visão geral de cada disciplina
>>Tarefas e responsáveis:
>>>Implementar versão inicial da tela geral da disciplina [Isabella]
>>
>>>Adicionar ementa, nome do professor, foto do professor, horário e link para página da máteria no DCC [Raissa]
>>
>>>Implementar no backend a lógica listagem das matérias [Maria]
>>
>>>Integrar tela com a respectiva lógica no backend [Isabella]

### História #5: Como usuário, eu gostaria de visualizar uma página para adicionar uma avaliação de uma disciplina 
>>Tarefas e responsáveis:
>>>Implementar versão inicial da tela de adicionar uma nova avaliação [Raissa]
>>
>>>Implementar no backend uma rota para uma página de nova avaliação [Gabriela]
>>
>>>Integrar tela de nova avaliação com a respectiva lógica no backend [Isabella]

### História #6: Como usuário, eu gostaria de avaliar a disciplina em relação à se cobra presença(sim ou não), didatica do professor(ruim, media, boa, otima), provas(fácil, médio, difícil), trabalhos(fácil, médio, difícil), tempo de dedicação extraclasse(pouco, medio, alto), nota geral da disciplina(1 a 5 estralas)
>>Tarefas e responsáveis:
>>>Implementar formulário [Raissa]
>>
>>>Implementar no backend a lógica de preecher o formulario com o backend/banco de dados [Maria]
>>
>>>Implementar a associação do formulario com o backend [Isabella]

### História #7: Como usuário, eu gostaria de visualizar a resposta mais frequente para cada categoria da avaliação de uma disciplina
>>Tarefas e responsáveis:
>>>Implementar na tela da disciplina uma tabela onde as respostas mais frequntes serão mostrados [Raissa]
>>
>>>Implementar no backend a lógica do cálculo para computar a resposta mais frequente [Gabriela]
>>
>>>Integrar a tabela com a respectiva lógica no backend [Isabella]

### História #8: Como usuário, eu gostaria de ordenar as materias por avaliação
>>Tarefas e responsáveis:
>>>Implementar na tela de listagem das disciplinas disponíveis um filtro para ordenação por nota de avaliação [Isabella]
>>
>>>Implementar no backend a lógica de ordenação por nota de avaliação [Maria]
>>
>>>Integrar filtro de ordenação com a respectiva lógica no backend [Raissa]
