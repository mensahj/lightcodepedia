```csv
claim,promised
campuses open on Saturday,3
```

{: .dataset #promise_b }

```csv
campus,adoption_day
Milwaukee,Saturday
Ozaukee,Saturday
Racine,Sunday
```

{: .dataset #shelters_b }

```csv
```

{: .datagrid #promise_grid source="promise_b" editable="true" height="120" title="📜 The promise" }

```csv
```

{: .datagrid #board_grid source="shelters_b" editable="true" height="160" title="🏠 The parts" }

```sql
SELECT p.claim, p.promised, c.actual
FROM promise_b p
JOIN (SELECT COUNT(*) AS actual FROM shelters_b
      WHERE adoption_day = 'Saturday') c
WHERE p.promised <> c.actual
```

{: .query source="promise_b,shelters_b" #disagreement }

```csv
```

{: .datagrid #disagreement_grid source="disagreement" height="120" title="🚨 Promise and parts disagree — should stay empty" empty="One story. Consistent." }