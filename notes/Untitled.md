---
title: Untitled
created: '2025-01-02T07:31:30.535Z'
modified: '2025-01-02T07:51:12.655Z'
---

# Untitled
```java
    /**
     * 根据需求内码删除 需求附件
     * @param demandId
     */
    @Modifying
    @Query(value="delete from busi_demand_attach where demand_id= ?1 ", nativeQuery=true)
    void deleteByDemandId(String demandId);
```
```java
    /**
     * 根据协议内码和协议删除状态查询协议信息
     *
     * @param protocolId
     * @param haveDelete
     * @return BusiProtocolListDO
     * @Title: findByProtocolIdAndHaveDelete
     * @date 2018-02-27 13:32:15
     * @author dukezhou
     */
    @Query("select s from BusiProtocolListDO s where s.protocolId = ?1 and s.haveDelete = ?2 ")
    public BusiProtocolListDO findByProtocolIdAndHaveDelete(String protocolId, String haveDelete);
```
```java
 Pages queryCustomTaxFees(CustomTaxFeeQueryDTO queryDTO);
```
