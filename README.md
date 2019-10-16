# XITN
A TeX like syntax for XML

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
