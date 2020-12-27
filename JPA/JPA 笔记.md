# JPA 笔记

> 1V



#### 一对多关联

```java
@Data
@Entity
@Table
@Accessors(chain = true)
public class ViUser {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    
    @OneToMany(mappedBy = "user", cascade = CascadeType.ALL, fetch = FetchType.EAGER, orphanRemoval = true)
    private List<ViRole> roles;
}
```

```java
@Data
@Entity
@Table
@Accessors(chain = true)
public class ViRole {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;

    @ManyToOne
    @JsonBackReference
    private ViUser user;
}
```