---
layout: default
title: 条件节点
parent: 节点说明
nav_order: 3
---

# 条件节点

## 节点说明

条件节点用于根据 if / else / else if 条件将工作流拆分成多个分支路径。该节点适用于需要执行条件判断逻辑、动态控制工作流走向的场景。

## 节点配置

条件节点的配置主要包括条件设置、判断流程与分支路径。

![条件节点场景](../assets/images/条件节点场景.png)

### 条件机制

条件分支的运行机制支持如下六种路径控制：

* IF 条件：选择变量，设置条件类型和匹配的目标值；
* IF 条件判断为 `True`，执行 IF 路径；
* IF 条件判断为 `False`，执行 ELSE 路径（如存在）；
* ELSE IF 条件判断为 `True`，执行 ELSE IF 路径；
* ELSE IF 条件判断为 `False`，继续判断下一个 ELSE IF 条件；
* 所有条件均不满足时，执行最后的 ELSE 路径（如配置）。

### 条件类型

条件判断支持以下类型：

* 等于（Equal to）
* 不等于（Not equal to）
* 长度大于（Length greater than）
* 长度大于等于（Length greater than or equal to）
* 长度小于（Length less than）
* 长度小于等于（Length less than or equal to）
* 包含（Contains）
* 不包含（Not contains）
* 开头为（Start with）
* 结尾为（End with）
* 为空（Is empty）
* 不为空（Is not empty）
* 为 null（Is null）
* 不为 null（Is not null）

### 多重条件判断

当条件逻辑较为复杂时，可以通过添加多个条件，并在其之间设置 **AND** 或 **OR**，实现交集（所有条件成立）或并集（任一条件成立）的组合判断。

![条件节点多重判断](../assets/images/条件节点多重判断.png)

## 常见使用场景

以下是一个典型的使用示例 —— 文本总结工作流：

* IF 条件：选择代码节点中的 `key0` 变量，设置条件为 **包含** `hello`；
* 若条件为 True，走 IF 路径；
* 若为 False，判断 ELSE IF：若 `key0` 不包含 `hello`，继续判断 `key1` 是否为空或 `key21` 是否等于 `hello`；
* 若 ELSE IF 条件仍不满足，最终走 ELSE 路径。

通过条件节点，工作流可灵活应对多种判断场景，实现清晰、可控的分支流程。
