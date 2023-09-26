Name: Jeydin Pham

Date: 9/25/2023

Period: 5

# Unit 4 Notes: Maps

- Maps - Store pairs of <u>keys</u> + <u>values</u>

  - Each key-value pair is unique
  - Duplicates are not allowed

- A map is an interface

```java
Map hash = new HashMap();
Map tree = new TreeMap();

Map<String, String> hash;
hash = new HashMap<String, String>();
// Map<String, String> = new HashMap<String, String>();
```

- Hash Sets + Maps use Hash tables to store information

- Tree Sets + Maps use binary trees to store + sort information

## Methods

- put(x, y) - Adds <x, y> to map
- get(x) - Gets value for key x
- size() - # of items (pairs) in set
- remove() - Removes key from map
- keySet() - Returns set of all keys
- containsKey() - Checks for key x in map

```java
Map<Integer, String> map;
map = new TreeMap<Integer, String>();
map.put(1, "apple");
map.put(2, "orange");
map.put(3, "pear");
```

| Key | Value  |
| --- | ------ |
| 1   | apple  |
| 2   | orange |
| 3   | pear   |

```java
map.get(1);
```

| Output |
| ------ |
| apple  |
