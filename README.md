# zzj-framework
**<font color=red>为中小企业数字化转型尽微薄之力</font>**</br>
**<font color=red>目前还在开发中... 先不要考虑使用的情况了。由于我们都是打工人，请给我们点时间……谢谢支持</font>**

致力于为中小型团队，提供一些比较 core 而又 basic 的服务。
**注意是中小型，且数据规模不是很大的情况。因为当数据量比较大了，那我们必须会做一些特定的场景才能优化。
所以，针对于此，此项目的大多数组件可能都不适合你，除非你在此基础上进行二次开发。**

这些服务能够保证他们可以快速的上手，将更多的精力用在业务上的开发。

同样，我们也要更为友好的支持他们能够进行二次开发，用以保证其定制化的场景 致力于为中小型团队，提供一些比较 core 而又 basic 的服务。
这些服务能够保证他们可以快速的上手，将更多的精力放在业务上的开发。
同样，我们也会更为友好的支持他们能够进行二次开发，用以保证其定制化的场景。

## zzj-oauth2
这是一个基本的 **权限验证** 框架，其内部集成了 spring-security，我们通过一些固定的表结构设计，已经实现了基本的 权限验证 的相关
功能。

当用户想要使用该组件时：
1. 只需要创建对应的表，然后录入初始数据（可以在 zzj-oauth2-web 中向库里插入数据）。
2. 在基本的项目中使用拦截器、或者 aop 调用我们暴露出去的接口，即可实现权限相关的功能逻辑

通过这种方式，我们让开发人员忽略了这部分功能的开发，从而大大的提高其工作效率。让其有更多的精力放在业务的开发商。

项目设计之初，我们期望该组件最起码要有以下的优点：
1. 数据库要支持常见的 mysql，oracle 等常见的库
2. 实体和字段之间的映射要方便，如果开发人员在进行二次开发，甚至表名，字段名都和实体不一致时，我们也要尽量友好的支持
3. 支持 角色，权限，人 的关联配置。甚至是后期要将 **数据权限** 考虑在内

## zzj-oauth2-web
主要提供对 zzj-oauth2 组件的一些数据管理能力。注意，它提供的能力不应该面向 C 端，只是常用作后台用户类相关的数据管理而已。
如果有需要对 后台的 基本登录用户信息做数据统计等相关功能，后期可能会考虑加进去，也可能会交给 **开发人员** 端自行实现。
