# Chapter 5
## Information Hiding (and Leakage)

### This chapter discusses techniques for creating deep modules

## 5.1 Information Hiding

The previous chapter discusses the theory behind and what a deep module is - the complexity is in the class and the interface is simple. This is the practical implementation and how to achieve it. 

The most important technique is informating hiding. 

Note: Althoguh I thought information hiding and encapsulation were synonymous, there is a difference:

### Aside: Informatin hiding vs Encapsulation

In 1978, Parans claims that the words encapsulation and information hiding are synonymous. But in 2001 Paul Roger showed the difference between encapsulation and information hiding with sample code. He says that we can have encapsulation without having information hiding. Encapsulation doesn't have strict rules on which access modifier to use - we cna use public, private or protected access modifiers. 

Information hiding is a programming principle that aims to prevent the direct modification of the data of a class. It also provides a strict guideline to access and modify the data of a class. Its implemented through the use of a private access modifier. This restricts access to the fields within the class only. 

In summary:
Infomration Hiding:
- A design principle to hide implementation details and unintended modification to data. Strictly uses the private access modifier and helps to achieve defensive programming. 

Encapsulation:
- An object-oriented principle that bundles data with functions operating on them. It's not strict on access modifiers and can use a public, private, or protected access modifier. It's a methodology to achieve information hiding. 
- Encapsulation is more about controlling access to the internal details rather than completely restricting it.