# Avaliação prática em PHP - Spassu

Antes de mais nada, obrigado pelo seu interesse em atuar em nossa equipe de desenvolvimento!

O objetivo dessa avaliação técnica é analisar sua capacidade de resolução de problemas focada na implementação em PHP, observando suas escolhas quanto à linguagem, conceitos sobre padrões de código e qualidade.

A seguir serão apresentadas as informações necessárias referentes ao teste.

## Primeiros passos

- Crie um novo repositório público no [GitLab](https://gitlab.com) para este projeto de avaliação;
- Efetue *commits* semânticos conforme for evoluindo sua solução;
- Consultas são permitidas em qualquer fonte, inclusive aos [Links úteis](#links-úteis);
- Tire suas dúvidas sobre esse teste com os entrevistadores; e
- Não se preocupe demais com a avaliação... Também já passamos por essa etapa. 😉

Sucesso com o teste!

## Características do desenvolvimento

- A aplicação criada deve conter *back-end* em PHP com qualquer versão igual ou superior a 5.6, podendo ser adotado, ou não, qualquer *framework* de sua preferência;
- O *front-end* da aplicação pode ser em [Bootstrap](https://getbootstrap.com), [Tailwind](https://tailwindcss.com) ou outro *framework*, se preferir;
- Banco de dados adotado deve ser relacional;
- Sugerimos o *PHP Storm* como sua *IDE* de desenvolvimento; e
- Faça o máximo de requisitos que puder, mas é possível cumpri-los parcialmente.

## Funcionalidades da aplicação

✔️ Listagem de antenas;
- Exibir acima da listagem o *ranking* das 5 (cinco) UFs e suas respectivas quantidade de antenas, ordenado decrescentemente por quantidade;
- Exibir todos os registros de antenas em tela de listagem;

✔️ Exibição de uma dada antena;
- Apresentar dados da antena pretendida em tela de exibição;
- Exibir imagem da foto da antena;
- Exibir mapa indicando latitude e longitude da antena;

🔒 Inclusão de nova antena;
- Exibir tela para cadastramento de nova antena;
- Combo (caixa de seleção) de UF deve exibir todas as "Sigla - Nome" em ordem de "Sigla", oriundas do consumo do serviço do IBGE: ```https://servicodados.ibge.gov.br/api/v1/localidades/estados```;
- Regras devem ser validadas, exibindo mensagem de erro se validação não for atendida;
- Campo identificador não deve ser exibido;

🔒 Alteração de antena existente;
- Exibir tela para edição de antena existente;
- Combo (caixa de seleção) de UF deve exibir todas as "Sigla - Nome" em ordem de "Sigla", oriundas do consumo do serviço do IBGE: ```https://servicodados.ibge.gov.br/api/v1/localidades/estados```;
- Regras devem ser validadas, exibindo mensagem de erro se validação não for atendida;

🔒 Exclusão de antena existente;
- Usuário deve confirmar exclusão;

📋 Carga de dados para inclusão de 100 mil registros de antenas;
- Execução de *script* de banco deve ser efetuado durante entrevista;

✔️ Registro de novo usuário;

✔️ *Login* de usuário registrado; e

🔒 *Logoff* de usuário.

##### Legenda
✔️ Acesso público;
🔒 Autenticação necessária; e
📋 Banco de dados.

### Dados

#### Antenas
> Uma antena é uma estrutura física responsável pela transmissão de ondas eletromagnéticas.

Campos e regras:
```
- Identificador (chave primária);
  - identificador universal único, obrigatório, único
- Descrição;
  - string, obrigatório, único, mínimo de 10 caracteres, máximo de 100 caracteres
- Latitude
  - obrigatório, decimal, entre -90 e 90
- Longitude
  - obrigatório, decimal, entre -180 e 180
- UF
  - obrigatório, string, 2 caracteres
- Altura (em metros);
  - decimal, obrigatório, maior que 0 
- Data de implantação; e
  - data, não obrigatório
- Foto.
  - [à sua escolha de tipo do campo], extensão png ou jpg
```

#### Usuários
> Indivíduos que acessarão o sistema.

Campos:
```
- Identificador (chave primária);
- Nome;
  - obrigatório, string
- Email; e
  - obrigatório, único, string, email válido
- Senha.
  - obrigatório, string, entre 8 e 32 caracteres
```

## Prazo

Esse teste foi projetado para ser realizado em até 12 (doze) horas, aproximadamente.

Para mantermos um paralelo entre a versão planejada e a efetivamente implementada, o prazo de entrega deve ser observado.

Ainda, conforme perfil, é possível que a complexidade e completude empregados na construção da solução tome mais tempo do que o previsto.

Então, tendo essas 12 horas como alvo, mas evitando que o esforço nesta tarefa dificulte ou atrapalhe suas costumeiras atividades, assim como o próprio teste, não ultrapasse **3 dias corridos**, contados a partir da data de comunicação dos entrevistadores ao apresentar esse material até às 23:59:59 do 3º dia seguinte; salvo se acordado outro data com os entrevistadores.

##### Exemplo
Data do envio deste texto para a prova: **sexta, 13 de setembro de 2024, às 10:30h**
Data limite de entrega do teste: **segunda, 16 de setembro de 2024, às 23:59:59h**

## Entrevista

- A aplicação deve ser executada no seu ambiente local, onde haverá tempo para a apresentação da sua solução;
- Efetuaremos a revisão de código conjuntamente;
- Atente que, possivelmente, questionaremos as justificativas de suas escolhas, observando o que você pensou, implementou, bem como as sugestões de melhorias do projeto; e
- Além do entrevistador(a) inicial, haverá a presença de um avaliador técnico.

## O que será avaliado

A correção qualitativa levará em conta os seguintes critérios:

- Entrega do repositório contendo seu projeto;
- Pontualidade da entrega, mediante prazo acordado;
- Funcionalidades do escopo;
- Conhecimento e adoção de padrões (MVC, SOLID, PSR);
- Consumo de APIs;
- Tratamento de erros;
- Qualidade do código ([*Clean Code*](https://www.hostgator.com.br/blog/clean-code-o-que-e));
- Testes unitários;
- Análise estática do código ([*PHP Stan*](https://phpstan.org));
- Modelagem e manipulação de banco de dados;
- Manutenibilidade do código;
- Segurança da aplicação;
- Documentação explicativa (*markdown*) para "subir" e rodar a aplicação;
- Suas implementações extras e/ou sugestões de melhoria na solução;
- Sua argumentação sobre as escolhas adotadas; e
- Outras questões, conforme nível do perfil.

## O que não será avaliado

- Autenticação do usuário (*login*, *logoff* e registro de usuário);
- Funcionalidades não previstas no escopo; e
- Funcionalidades exclusivas em *front-end* (mas são bem-vindas!).

## Links úteis

- [IBGE - Api de localidades](https://servicodados.ibge.gov.br/api/docs/localidades#api-UFs-estadosGet);
- [Bootstrap](https://getbootstrap.com);
- [*Clean Code*](https://www.hostgator.com.br/blog/clean-code-o-que-e);
- [*Commits* semânticos](https://github.com/iuricode/padroes-de-commits);
- [GitLab](https://gitlab.com);
- [PHP: Do jeito certo](http://br.phptherightway.com);
- [*PHP Stan*](https://phpstan.org);
- [PSR-12: Estilo de código](https://www.php-fig.org/psr/psr-12); e
- [Tailwind](https://tailwindcss.com).
