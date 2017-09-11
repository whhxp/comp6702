# COMP 6702 Computation theory

```
#include <>

```

# 2017年9月11日，第一课

* computation theory
    * mathmatical fundation
* computation Complexity Theory
    * This topic focuses on complexity of problem, the efficiency


# Theme of the Course 主题

## Studies **intrinsic complexity** of computational problems

## Absolute Questions:

### How much time is needed to solve the problem?

### How much resources will be needed?

## Relative Questions:

###More difficult than other problems?

### Are there “most difficult” problems?

## (Surprisingly: Many **relative** answers, only few **absolute** ones ...)

## **Rigorous** treatment:

### Mathematical formalisms, minimize “hand-waving”


### Precise definitions

### Theorems should be proved (if time allowed)


这是一个理论课程，没屁用（hopeless for job）

Tips：
* 写文章的时候需要准确描述
* 正式的符号

# Components of the Course
Computation Theory
* Question: “What can be computed (at all)?”
* Provides models of computation
* Explores their strength (expressiveness)

Basic Complexity Theory
* Question: “What can be efficiently computed?”
* Finds meaningful measures of efficiency
* Classifies and relates problems

Advanced Complexity Theory
* Deterministic answers ⇒ Probabilistic answers
* “Solution exists or not?” ⇒ “How many solutions?”
* “One machine works alone” ⇒ “Two machines interact”

# Outline
1 Computation Model
* Turing Machine, Decidability

2 Complexity Classes
* Time and Space Complexity

3 P vs. NP
* Reductions, NP-Hard and NP-Complete（解决问题的时候一般先考虑是NP-Hard还是NP-complete）

4 Probabilistic Complexity Classes
* Probabilistic TM; RP, coRP, ZPP, BPP

5 Complexity of Counting
* #P, #P-Complete

6 Iterative Proof Systems
* IP, probabilistically checkable proof

# Assessments
* Examination: 40%
    * Date to be announced
* Assignments: 60%
    * Computation Model: 15%
    * Basic Complexity: 30%
    * Advanced Complexity: 15%
    * Again, use Learn@PolyU to download and submit

# Reason for this course

1. 看文章让人觉得专业
1. 解决或者思考问题更系统


# Lecture 1: Computation Mode

OutLine:

* Formal Languages
* Model of Computation: [Turing Machine](https://zh.wikipedia.org/wiki/%E5%9B%BE%E7%81%B5%E6%9C%BA),有很多，可以参考维基百科
* Decidability, Undecidability, Semi-Decidability


# Problems as formal Languages


$\epsilon$


# Model of computation

输入输出模式太麻烦，应该有一个更简单更好用的模型来描述计算模型。

所有的可解决的（solvable）问题都可以通过ppt上写的模型来解决。

----------
polynomial多项式


# 图灵机 Turing machine

* 最简单的图灵机是一个带子（磁带？），上面可以读和写。
    * 用于输入输出和临时储存
    * 双向无限长（我觉得挺坑，硬盘不够大啊）

* 然后有一个**头（head）（个人感觉类似磁带磁头）**
    * 可以改变现有位置的符号
    * 可以一步一步移动
* 有限状态机


有限状态机：
* state（状态）是**有限的**
* 每个状态可以改变
* 每次改变状态由读取磁带上的符号决定


* $Q$ a finite set of states
* $\Gamma$ the tape alphabet including the blank: $\square \in \Gamma$
* $q0$ the initial state $q0 \in Q$
* $F$ the set of Final states, $F \subset Q$
* $\delta$: the transition function, $(Q-F) \times \Gamma \to Q \times \Gamma \times \{R,N,L\}$<br>
$Q-F$所有状态减去最终状态<br>
R: Right<br>
N: Don't Move<br>
L: Left<br>
you read some symbol you jump to some symbol
___________


Exersice 1:


$$L(W)=\{O^n1^n|n\ge1\}$$

exercise 2:

$$L(M)=\{W\subset W|W\in\{a,b\}^*\}$$




$$\in$$
$$\not\in$$