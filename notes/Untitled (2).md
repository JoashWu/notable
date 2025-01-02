---
title: Untitled (2)
created: '2025-01-02T08:03:08.101Z'
modified: '2025-01-02T08:38:44.748Z'
---

# Untitled (2)
```java
@Entity
@Table(name = "BUSI_TEMPLATE_INFO")
public class BusiTemplateInfoDO implements Serializable {

}

```

```java
public interface TemplateService {

}
```
```java
@Service
public class TemplateServiceImpl implements TemplateService {

}
```
```java
public interface BusiTemplateInfoDao
        extends JpaSpecificationExecutor<BusiTemplateInfoDO>, JpaRepository<BusiTemplateInfoDO, Long> {
}
```
