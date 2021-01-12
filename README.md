# KIBANA KQL CHEAT SHEET (v7.4)

1. To select documents with 'value' in any field

```
value
```

2. To select documents in which field (exists)

```
field :*
```

3. To select documents with field having value (equals)

```
field:value
```

4. To select documents with a phrase in the field with words in order

```
field:"Quick brown fox"
```

5. To select documents with a phrase in a field with words not in order and one or more words are present

```
field:Quick brown fox
```

The above condition is also equivalent to

```
field:(Quick or brown or fox)
```

6. To select documents with a phrase in a field with words not in order and all words must be persent

```
field:(Quick and brown and fox)
```

NOTE: Conditions can be joined by using brackets

7. Combining 2 conditions

   1. AND

   ```
   field1:value1 and field2:value2
   ```

   2. OR

   ```
   field1:value1 or field2:value2
   ```

8. Negation

```
not field:value
```

9. WildCard Statements

   1. Wildcard for Values

   ```
   operating_system: Win*
   ```

   2. Wildcard for Fields

   ```
   Kubernetes.*: vwo-app
   ```

10. Ranges
    1. Less than
    ```
    field < 100
    ```
    2. Greater than
    ```
    field > 100
    ```
    3. Less Than Or Equal to
    ```
    field <= 100
    ```
    4. Greater Than Or Equal to
    ```
    field >= 100
    ```

## NOTES

1. Kibana while searching strips off punctuations and special characters and thus cant be used to search for values
2. Use Parenthesis in queries for optimized results
