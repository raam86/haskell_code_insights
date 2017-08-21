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

