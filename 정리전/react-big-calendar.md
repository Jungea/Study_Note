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



rbc-calendar
	rbc-toolbar
	rbc-month-view
		rbc-month-header
		rbc-month-row  --한주
			rbc-row-bg  --한주(배경)
				rbc-day-bg --하루(배경)     rbc-today(오늘 배경)   rbc-off-range-bg(다음달)
			
				
		
		