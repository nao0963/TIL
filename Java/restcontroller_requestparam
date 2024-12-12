# RestController와 @RequestParam

## What I Learned
- While configuring `@PostMapping` in `RestController`,
- I found out that I omitted `@RequestBody` for input data
- Thinking that `@RequestBody` is automatically deployed for `RestController`
- But instead `@ResponseBody` is automatically deployed, not `@RequestBody`

## Recap
- Learned not to confuse `@RequestBody` and `@ResponseBody`
- And how to use both properly in `RestController` setting

## Error Code
```java
@PostMapping("/insert")
public ResponseEntity<?> insert(BoardDTO board)
        throws IllegalStateException, IOException {
    log.info(board.toString());
    service.insert(board);

    return ResponseEntity.ok(HttpStatus.OK);
}
```

## Fixed Code
```java
@PostMapping("/insert")
public ResponseEntity<?> insert(@RequestBody BoardDTO board)
        throws IllegalStateException, IOException {
    log.info(board.toString());
    service.insert(board);

    return ResponseEntity.ok(HttpStatus.OK);
}
```
