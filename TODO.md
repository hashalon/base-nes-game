# TODO

Encoding of position on 16bits

```
0000000000000000
|    |  | |  |
|    |  | |  +-- 8 sub-pixels
|    |  | +-- 1 tile / 8 pixels
|	 |	+- 1 metatile / 4 tiles
|	 +-- 1 screen / 8 metatiles
+---- 32 screens
```


benefits of this layout:
- good sub-pixel precision
- metatile coords are grouped in the same byte
- metatile coords are diretly accessible with bits 7 & 6
- plenty of room for large levels

## Notes

32 × 8 × 7 metatiles is still 0x700 bytes of data
meaning we can store at most 12 levels like that
we may need more optimized solutions to store levels...
