# Estudo Orientado

Material produzido na disciplina Estudo Orientado no semestre 2018.2 do Doutorado.

# Objetivo do trabalho do doutorado
Qual o objetivo do trabalho?

Esse trabalho propõe o CCRNet, que é um modelo de conversão de consultas a bancos de dados relacionais escritas em linguagem natural para queries SQL, independente do modelo de dados utilizado, ou seja, capaz de ser utilizado para a realização de consultas em modelos de dados de diferentes áreas de conhecimento (database agnostic). Além disso, para o idioma português é proposto um plugin (CCRNetBR) que tem como objetivo otimizar os resultados para o idioma específico.

Esse modelo será avaliado pelos resultados obtidos nas suas execuções frente a diferentes datasets (https://atlas.cern/tags/open-data, WikiSQL - MAS, IMDB e YELP). 

Como os outros modelos funcionam? O que proporei de diferente para o meu modelo?

Para responder essa pergunta preciso verificar os tipos de solução. Acredito que os surveys apresentam arquiteturas com os tipos de soluções. Preciso descobrir em qual tipo de solução os modelos NL2SQL se encaixam. Dessa forma, consigo encaixar os artigos antigos com os artigos atuais que tratam o WikiSQL.

Também é importante encaixar o modelo síntese automática de queries SQL.

# Tarefas
https://gitlab.com/riquebueno/doutorado/boards

# Reuniões
Reunião 1 - 15/08/2018
- Primeira reunião de alinhamento.
- Proposta do estudo orientado deve ser entregue até 14/09.
- Próxima reunião 29/08.
- Tarefas:
- Testar acesso ao DGX.
- Checar como o artigo que propõe o WikiSQL faz a validação da forma lógica.
- Interessante tentar publicar no WikiSQL e continuar com a ideia do gerador.
- Quais são os pontos problemáticos deles? Comparações entre eles? Quero propor uma coisa nova, por exemplo, queries com join? O que diferem e o que falham? Existem modelos que não utilizam redes neurais? Aprendizado de sequência? Olhar outros datasets?
- Técnica de pesquisa bibliográfica Snowballing (https://research-methodology.net/sampling-in-primary-data-collection/snowball-sampling/)
- Fazer pesquisa bibliográfica, por exemplo, existe um survey? Que tal publicar? SQLizer: Query Synthesis from Natural Language
- Algum estudo considera join?

Reunião 2 - 05/09/2018
- Criar linha do tempo para falar sobre a evolução dos NLIDBs.
- Meu problema vai especializar em SQL. Pode até utilizar outras fontes para enriquecer o pré-processamento do texto de entrada, mas isso não será usado dentro da rede ou como fonte de dados.
- Síntese de programas também é chamado de indução de programas.
- Avançar com o levantamento + especificar corretamente o problema que quero resolver (entradas e saídas, quem já se propõe a resolvê-lo hoje, quais as técnicas aplicadas e quais pretendo aplicar, tenho alguma ideia "fora da caixa"). Com isso tenho uma visão melhor dos desafios.
- Preocupação com o dataset de exemplos. Como vou obter? É importante começar a pensar nisso agora.
- O Estudo Orientado pode gerar um artigo.
- Preocupação com o acesso ao DGX. Acessar logo!
- QUAL PROBLEMA QUERO RESOLVER? NL para SQL para qq tipo de SGBD (ansi-SQL). A proposta será para um modelo específico (indústria de petróleo, por exemplo) ou poderá ser aplicado a outros contextos? Quero poder aplicar a outros contextos mas precisarei da base de treinamento. Assim, é importante criar o modelo genérico sem qq referência à indústria de petróleo. Quais são os problemas relacionados e quais são as técnicas aplicadas?
- Posso pensar em uma solução genérica e ao aplicar ao português não encontrar resultados interessantes. Temos uma hipótese que converter do inglês para SQL seja mais fácil. Mas se o resultado em português não for tão bom, podemos acoplar algum componente para melhorar os resultados em português. Isso não faz com que a proposta deixe de ser genérica.
- Prestar atenção à diferença entre técnica e problema. Por exemplo, qual a relação entre NLIDB, SEQ2SEQ e NL2SQL? SEQ2SEQ é uma técnica, NL2SQL é uma instância de NLIDB.
- Pensar na solução de forma abstrata mesmo sem conhecer a fundo todas as técnicas aplicadas. Será que fora da caixa não consigo pensar em alguma alternativa?
- Apresentei um resumo do survey "Natural Language Interfaces to Databases - An Introduction (Androutsopoulos, G.D. Ritchie, P. Thanisch)". Segue link da apresentação: https://docs.google.com/presentation/d/1RMKBPriAfI2kgn2xnIO78njdmjZ-0xuBqyVIhRxzRQU/edit?usp=sharing

Reunião 3 - 19/09/2018
- Escrever com segurança: "Quais são os tipos de técnicas existentes e como funcionam?".
- Para cada um dos tipos, escrever exemplos e citar os artigos. Acho que é uma boa estrutura para começar o survey. Mas antes é importante falar que apesar de existir hadoop, ..., ainda existem muitos dados em bancos relacionais que os usuários querem ter liberdade de explorar (democratização da informação).
- Tirar a palavra "modelo" de dados do objetivo. Trocar por schema (schema agnostic).
- Trocar plugin por recurso linguístico. Outra ideia é utilizar o Tesauro de Tulsa. Esse recurso adicional pode ser genérico para um idioma ou específico para um nicho de informação.
- Escrever o texto em inglês.
- http://qualis.ic.ufmt.br/: Site para pesquisar conferências e periódicos.
 - Quais palavras chave usei para a pesquisa bibliográfica? Guardar para citar depois. Pesquisar quem referencia o survey de 95 e olhar esses artigos (snow balling). Algumas pessoas fazer uma revisão sistemática.
 - Começar a falar sobre QA e especializar para NLIDB.
 - Primeiro classificar o problema que vou tratar. Entrada não estruturada e saída estruturada.
 - Segundo estruturar as categorias das soluções para esse problema. Estou revisitando a taxonomia do artigo de 95. É muito importante!

# Material Interessante (Acho que tenho que criar um BIBTEX com isso tudo - tipo criar um latex com a estrutura da tese e já colocar as coisas que estou escrevendo)
- Livro Speech and Language Processing (3rd ed. draft) https://web.stanford.edu/~jurafsky/slp3/
- http://www.statmt.org/moses/
- Boom do Deep Learning = GERAÇÃO E ARMAZENAMENTO DE GRANDES VOLUMES DE DADOS + GRANDE EVOLUÇÃO DE HARDWARE DE PROCESSAMENTO (GPU) + MODELOS DE MACHINE LEARNING MAIS MADUROS.
- https://www.amazon.com.br/Natural-Language-Data-Management-Interfaces/dp/1681734087?tag=goog0ef-20&smid=A1ZZFT5FULY4LN&ascsubtag=eceb0337-4b24-4bab-93c6-4f818ed3a9d6
- https://paulhcleverley.com/2018/09/06/search-is-on-the-move/
- https://anniebruton.wordpress.com/2013/09/21/dear-new-phd-student/
- http://www.theexclusive.org/tag/stress%20in%20research/
- http://deeplearningbook.com.br/capitulos/
- https://www.technologyreview.com/s/611568/evolutionary-algorithm-outperforms-deep-learning-machines-at-video-games/
- https://blog.openai.com/
- https://github.com/sebastianruder/NLP-progress
- Gardner, Matt, et al. "Allennlp: A deep semantic natural language processing platform." arXiv preprint arXiv:1803.07640 (2018).
- http://www.deeplearningbook.org/
- https://web.stanford.edu/~jurafsky/slp3/

