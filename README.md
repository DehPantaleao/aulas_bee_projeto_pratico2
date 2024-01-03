# Instrucoes para clonar o projeto
Seguir as instruçõe de fork que estão no doc descritivo do projeto2 no mural da aula
  
# Crie uma branch com seu nome
git checkout -b emerson

#Fazer as alterações

git add .

git commit -m "Adicione uma descrição concisa das alterações aqui"

git push origin emerson

#Pull Request

Acessar https://github.com/EmerF/aulas_bee_projeto_pratico2/pull/new/emerson

criar um pull request de sua branch para a branch master


#1 - Estrutura: 
  Clonar projeto https://github.com/EmerF/aulas_bee_projeto_pratico2
  Adicionar as dependências conforme aulas anteriores
-JPA
-mongo

#2 - Erros e exceções: criar um controller com endpoints: 
-endereço /api/nome/{nome} que:
    ao receber um nome=erro
    dispara uma custom Exception com um código de retorno 400(Bad Request) e uma mensagem: “erro no serviço”
    endereço /api/generic que:
    ao ser acessado
    dispara uma Exception com código 500(Internal Server Error) 
    
#3 - Herança e Polimorfismo
-Criar classes para representar produtos com 
  id, descricao, preco(geral)
  Cerveja
  comAlcool (true/false)
  Refrigerante
  comAcucar (true/false)
  Composição e Interfaces

#4 - Classes para representar funcionários com
  nome, cpf, telefone, salário(geral)
  os funcionários devem implementar os contratos:
  cálculo da Ajuda Custo
  Gerente: 5 % sobre o salário
  Dev: 10 % sobre o salaŕio
  imposto de renda
  Gerente: 10 % sobre o salário
  Dev: 5 % sobre o salário

#5 - o funcionário deverá conter um objeto Endereco com os seguintes campos:
  Rua
  Bairro
  Cidade

#MongoDB(JPA)
criar um controller para salvar um produto no banco de dados
endereço: /api/produtos que recebe um Produto(modelo do item 3 acima) como parâmetro e
chama a classe de serviço e salva o produto no banco de dados
criar a estrutura repository(usar o nome ProdutoRepository), service e controller conforme exemplo feito na aula.

#Verificação:
Tem um teste de integração no ProdutoControllerTest para a verificação dos controllers. Descomentar essa classe, ajustar os possíveis erros e depois fazer o pull request para o repositório.

**Obs: atenção para os nomes de atributos, repository e api. 
