# gateway_postfilter_if

## What I Learned
- to check the return type of the method I'm using
- result is not returned if the type doesn't match
- even if there's only one value in the list

## error code
```java
  return chain.filter(exchange).then(Mono.fromRunnable(() -> {
      System.out.println(headers.get("mydata"));
      if(headers.containsKey("mydata") && headers.get("mydata").equals("test")) {
          log.info("FilterB: return only if there is 'test' value under 'mydata'");
      }else{

      }
  }));
```



## fixed code
```java
  return chain.filter(exchange).then(Mono.fromRunnable(() -> {
      System.out.println(headers.get("mydata"));
      if(headers.containsKey("mydata") && headers.get("mydata").**get(0)**.equals("test")) {
          log.info("FilterB: return only if there is 'test' value under 'mydata'");
      }else{

      }
  }));
```
    
