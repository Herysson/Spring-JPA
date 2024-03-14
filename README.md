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

```
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

