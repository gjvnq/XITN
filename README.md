# XITN
A TeX like syntax for XML

A slash ```\``` is for creating elements
and a hash ```#``` is used for macros.

## Examples

### Basics

```xitn
\h1[id=title,style="font-family: Times New Roman",color=green]{My Title}
\hr Copyright
```

```xml
<h1 id="title" style="font-family: Times New Roman" color="green">
  My Title
</h1>
<hr/>
Copyright
```

### Spaces and pretty print

```xitn
\span#myId.class1.class2{Lorem Ipsum}
\span#myId.class1.class2{ Lorem Ipsum}
\span#myId.class1.class2{ Lorem Ipsum }
```

```xml
<span id="myId">Lorem Ipsum</p>
<span id="myId">
  Lorem Ipsum</p>
<span id="myId">Lorem Ipsum </p>
<span id="myId">
  Lorem Ipsum
</p>
```

### Macros

```xml
#!DEF(title, 1, \h1.small-caps{#1})
#!DEF(title, 2,
  #title(#1) by \h2.small-caps{#2})
#!DEF(pcounter, 1)
#!DEF(p, 1,
  \p{\span.counter{#pcounter} #1}
  #!INCR{#pcounter})
```
