```csv
name,fee,campus
Scout,180,Milwauke
Biscuit,150,MKE
Nova,180,Downtown
```

{: .dataset #dogs save="../module_00/dogs.yaml" }

## 🦮 Dogs
```csv
```

{: .datagrid #wired source="dogs" height="200" title="🏠 Our dogs, by campus" empty="Nothing arrives here yet." }

## 📊 Fees
```csv
```

{: .chart #fees type="bar" x="name" y="fee" source="adoptions" height="260" empty="Nothing arrives here yet — this chart is listening for a part that does not exist." }