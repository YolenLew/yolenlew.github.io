# 备忘录

## 0522_mybatis-plus

### mybatis-plus

- [ ] 所有自定义方法，加上`@ResultMap("mybatis-plus_Person")`注解；或者在xml配置文件中，加上如下类型转换器

```xml
<result property="roleRange" column="role_range" typeHandler="com.baomidou.mybatisplus.extension.handlers.JacksonTypeHandler"/>
```

- [ ]  MybatisPlus处理Mysql的json类型：在[实体类](https://so.csdn.net/so/search?q=实体类&spm=1001.2101.3001.7020)加上@TableName(autoResultMap = true)、在JSON字段映射的属性加上@TableField(typeHandler = JacksonTypeHandler.class)；

> https://blog.csdn.net/qq_35098526/article/details/117912886
