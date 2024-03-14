# **Spring JPA Annotations** 

## **O que é JPA?**
JPA, que significa Java Persistence API, não é uma ferramenta ou framework por si só; 
em vez disso, ele fornece um conjunto de conceitos e diretrizes que implementam diretamente 
como gerenciar dados relacionais em aplicativos Java. Metadados de anotações são fornecidos 
pelo JPA para definir uma relação entre objetos e bancos de dados relacionais.

## **O que é Anottation**
A anotação é uma informação suplementar sobre o programa. Os desenvolvedores usam anotações 
para informar o JPA.

`
@Entity
@Table(name = "students")
public class Student {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    @Column(name = "id")
    private Long id;
    // other fields and methods
}
`
