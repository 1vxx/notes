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

#### 索引

```java
//唯一
@Table(name = "Safety_Type", uniqueConstraints = @UniqueConstraint(columnNames = {"code"}))
//普通
@Table(name = "Safety_Type", indexes = {@Index(columnList = "applyMemberId"), @Index(columnList = "orgUnitId")})
```

