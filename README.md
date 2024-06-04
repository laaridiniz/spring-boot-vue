### Proposta

Utilize os projetos contidos nos repositórios https://github.com/mineda/springboot3app e https://github.com/mineda/vue3app e crie uma nova página para gerenciar Vocábulos, consumindo
serviços de VocabuloController, que:

1) Possua um link de acesso na barra de navegação com o texto "Gerencie Vocábulos" que direcione à nova página;

2) Abra uma lista contendo todos os vocábulos cadastrados no banco de dados ao ser aberta. Cada vocábulo deve apresentar somente id, termo, significado, versão e situação. A situação deve ser
preenchida de acordo com a coluna “voc_data_hora_desativacao”, assumindo valor “desativado” se estiver preenchida ou “ativo” se possuir valor nulo;

3) Permita o cadastro de um novo vocábulo. Após o cadastro, a lista do item 2 deve ser atualizada e os "inputs" devem ser limpos;

4) Permita a consulta de um vocábulo usando termo e versão. O resultado deve ser apresentado na mesma lista do item 2. Caso nenhum vocábulo com as características buscadas exista, substitua a
lista por uma mensagem (exemplo: “Nenhum vocábulo foi encontrado para os critérios fornecidos”).

Dicas:
- Em caso de erro por diferença de versões do Java, use o comando "mvn clean" no terminal;
- Não esqueça de criar o banco de dados antes de executar o backend;
- Para entradas do tipo "datetime" é possíve utilizar o tipo "datetime-local" de "input" (https://www.w3schools.com/tags/att_input_type_datetime-local.asp).

### Resultados

1. Teste do método GET:

<div align="center">
  <img width="960" alt="get" src="https://github.com/laaridiniz/spring-boot-vue/assets/86115352/628df8eb-99b5-462b-81b2-e82ca2b5aafc">
  <br>
</div>   

2. Cadastro:

<div align="center">
  <img width="959" alt="cadastro" src="https://github.com/laaridiniz/spring-boot-vue/assets/86115352/8847b408-5457-4171-b802-dbbe0caf133c">
  <br>
</div>

3. Consulta:

<div align="center">
  <img width="960" alt="consulta" src="https://github.com/laaridiniz/spring-boot-vue/assets/86115352/dde93a29-dd8e-439a-ba20-bcecf68081f6">
  <br>
</div>


4. Listagem:

<div align="center">
  <img width="959" alt="listagem" src="https://github.com/laaridiniz/spring-boot-vue/assets/86115352/65d01b0c-d75d-4ef9-a3e0-3d3ae4cea604">
  <br>
</div>
