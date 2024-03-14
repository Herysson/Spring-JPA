# **Spring JPA Annotations** 

## **O que é JPA?**
JPA, que significa Java Persistence API, não é uma ferramenta ou framework por si só; 
em vez disso, ele fornece um conjunto de conceitos e diretrizes que implementam diretamente 
como gerenciar dados relacionais em aplicativos Java. Metadados de anotações são fornecidos 
pelo JPA para definir uma relação entre objetos e bancos de dados relacionais.

## **O que é Annotation**
A anotação é uma informação suplementar sobre o programa. Os desenvolvedores usam anotações 
para informar o JPA.

## **JPA Annotations**
As anotações JPA são usadas no mapeamento de objetos Java para tabelas de banco de dados. 
O Hibernate é a biblioteca ORM mais popular que utiliza as especificações JPA e fornece algumas 
anotações adicionais. As anotações podem ser adicionadas ao código-fonte e permitidas a serem 
retidas pelo JVM em tempo de execução.

<div align="center">
    
![Principais Annotations](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*Z91sIw81eeIsjEnLEtseaQ.jpeg)

</div>

Essas são algumas das anotações mais comumente usadas em JPA/Hibernate e suas respectivas funções:

- `@Id`: Indica que o campo anotado é a chave primária da entidade.
- `@GeneratedValue`: Especifica a estratégia de geração de valores para a chave primária automaticamente.
- `@Table`: Permite definir informações adicionais sobre a tabela associada à entidade.
- `@Entity`: Marca a classe como uma entidade persistente.
- `@Column`: Permite definir informações adicionais sobre a coluna associada ao campo.
- `@Transient`: Indica que o campo não deve ser persistido no banco de dados.
- `@Temporal`: Especifica o tipo de dado temporal (data, hora etc.) de um campo de data/hora.
- `@Embedded`: Marca um campo como embutido, ou seja, parte de outra entidade.
- `@Embeddable`: Marca uma classe como embutível, ou seja, pode ser parte de outra entidade.
- `@ElementCollection`: Mapeia uma coleção de tipos básicos ou embeddables.
- `@OneToMany`: Estabelece uma relação de um-para-muitos entre duas entidades.
- `@ManyToOne`: Estabelece uma relação de muitos-para-um entre duas entidades.
- `@ManyToMany`: Estabelece uma relação muitos-para-muitos entre duas entidades.
- `@OneToOne`: Estabelece uma relação um-para-um entre duas entidades.
- `@Lob`: Indica que o campo contém um objeto grande (Large Object), como um blob ou clob.
- `@JoinColumn`: Permite definir informações adicionais sobre a coluna que é usada para a junção de entidades em relacionamentos.

Essas anotações são essenciais para mapear entidades Java para tabelas de banco de dados e 
para definir o comportamento de persistência.

## **@Id Annotation**
A anotação `@Id` é usada em Java para marcar um campo como a chave primária de uma entidade. 
Geralmente é utilizada em conjunto com um framework ORM (Object-Relational Mapping) como o Hibernate, 
que mapeia objetos Java para tabelas de banco de dados relacionais.

A anotação `@Id` pode ser usada com vários parâmetros para especificar detalhes sobre a chave primária. 
Aqui está um exemplo de como a anotação @Id pode ser usada com parâmetros:

``` java
@Entity
@Table(name = "students")
public class Student {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    @Column(name = "id")
    private Long id;
    // other fields and methods
}
```
## **@Generated Annotation**
A anotação ``@GeneratedValue`` é usada em Java para gerar automaticamente valores para colunas de chave primária em uma tabela de banco de dados. Esta anotação é tipicamente usada em conjunto com a anotação ``@Id`` para indicar que um campo específico é a chave primária para uma tabela.

A anotação ``@GeneratedValue`` pode receber um dos quatro parâmetros:

- ``strategy``: Este parâmetro especifica a estratégia a ser usada para gerar a chave primária. Existem quatro estratégias disponíveis: AUTO, IDENTITY, SEQUENCE e TABLE.
- ``generator``: Este parâmetro especifica o nome do gerador a ser usado para gerar a chave primária.

Aqui está um exemplo de como usar a anotação ``@GeneratedValue`` com o parâmetro ``strategy``:

``` java
@Entity
public class User {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    private String username;
    private String password;
    // other fields and methods omitted for brevity
}
```
