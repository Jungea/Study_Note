```ts
const {defaultDate} = useMemo(() => ({
  defaultDate: new Date(2015, 3, 13)
}), [])
//...
<Calendar defaultDate={defaultDate} {...otherProps} />
```

```ts
const onView = useCallback((newView) => setView(newView), [setView])
<Calendar onView={onView} {...otherProps} />
```


https://wild-at-develop.tistory.com/3