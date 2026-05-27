# Industrial Weighbridge Real-Time Database

## Enter Database

```bash
dbctl enter weightcollect
```

## Query Real-Time Vehicle Data

```bash
box.space.TrackWeight:select('CAR72')
```

---

# TrackWeight Status Description

| Status | Description |
|---|---|
| 0 | Initial State |
| 1 | Vehicle Entered |
| 2 | Weight Unstable |
| 3 | Weight Stable |
| 4 | Vehicle Leaving |

---

# Weight State Description

| State | Description |
|---|---|
| 0 | Stable |
| 1 | Unstable |
| 2 | Empty Scale |
| 3 | Overload |
| 4 | Empty Scale Alarm |
