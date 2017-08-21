# haskell_code_insights
for those aha! moments 

https://github.com/arianvp/crdt/blob/3cad584da0a89623d061bc9cf9f7bf8e23b6c1c5/src/CRDT/IncrementOnlyCounter.hs#L35

 - Map.insertWith

```
-- | Increments the counter
increment :: Ord a => a -> IncrementOnlyCounter a -> IncrementOnlyCounter a
increment i (IncrementOnlyCounter v) =
  IncrementOnlyCounter (Map.insertWith (\a b -> a + b + 1) i 1 v)
```

https://github.com/aviaviavi/legion/blob/190f6675b2d3384099a054a7a9a97784fdbbc25e/src/Lib.hs#L65

- `$` a function 

```
-- returns a copy of the block with the hash set
setBlockHash :: Block -> Block
setBlockHash block = block {blockHash = calculateBlockHash block}

-- returns a copy of the block with a valid nonce and hash set
setNonceAndHash :: Block -> Block
setNonceAndHash block = setBlockHash $ block {nonce = findNonce block}
```
