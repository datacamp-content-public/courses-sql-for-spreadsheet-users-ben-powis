---
title: 'Chapter 1'
description: 'How is my marketing campaign performing?'
---

## Adding new columns

```yaml
type: TabExercise
key: 1b2ad87ec0
xp: 100
```

Let's drill down to single campaign and see if we can make some decisions on it's feedback using SQL. Imagine our marketing team have asked you to feedback on performance of the `late_summer_deals` campaign.

`@pre_exercise_code`
```{python}
connect('postgresql', 'database')
set_options(visible_tables = ['sample'])
```

***

```yaml
type: NormalExercise
key: 77ea0690c2
xp: 100
```

`@instructions`
We can see how many clicks and sales our ads generated, but it would be helpful to see this ratio in a single column, let's add a conversion rate to our results!

`@hint`


`@sample_code`
```{python}
SELECT 
date,
campaign_name,
sum(clicks),
sum(conversions),
# create 'conversion_rate'
sum(___)/sum(___) AS conversion_rate
FROM sample
```

`@solution`
```{python}
SELECT 
date,
campaign_name,
sum(clicks),
sum(conversions),
# create 'conversion_rate'
sum(conversions)/sum(clicks) AS conversion_rate
FROM sample
```

`@sct`
```{python}

```

---

## Insert exercise title here

```yaml
type: NormalExercise
key: ce3375db2d
xp: 100
```



`@instructions`


`@hint`


`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}

```

`@solution`
```{python}

```

`@sct`
```{python}

```
