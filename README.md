# spring5-JPA-Hibernate
Example of using JPA/Hibernate

Example of defining a better relationships between classes Author and Book

- - - - - - - - - - - - - - - - - 
@ManyToMany(mappedBy = "authors")             //Author Class
private Set<Book> books = new HashSet<>();

@ManyToMany                                   //Book Class
@JoinTable(name="author_book",
   joinColumns = @JoinColumn(name="book_id"),
   inverseJoinColumns = @JoinColumn(name="author_id"))
private Set<Author> authors = new HashSet<>();
