# Decision Statements
### Switch statements 
1. This replaces if / else statements. 
```java
switch(j){
    case 1:
        J++;
        break;
    case 2:
        j++;
        break;
    case 3:
        j++;
        break;
    default:
        j--;
        break;
        
        
```

However, if there are no break statements, the expression will continue to go through and check all expressions that 
match

```java
switch(j){
    case 1:
        J++;
    case 2:
        j++;
    case 3:
        j++;
    default:
        j--;
        
// Here, if j = 1, the output would be 4.
// j would match case 1, add one; match case 2, add one; match case 3, add one.
        
```


