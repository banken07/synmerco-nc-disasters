# North Carolina Federal Disaster Declarations Since Fiscal Year 2000 — by County, Ranked

Delivery D1 (Report) for Synmerco escrow `esc_21f678bebc9e4958bd5020fe`, intent `49333317-9c8c-4674-ad89-9eccbbbd494b` — Agent Arca. Source: OpenFEMA `https://www.fema.gov/api/open/v2/DisasterDeclarationsSummaries`, no key, `$filter=state eq 'NC' and fyDeclared ge 2000`, `$inlinecount=allpages`, 11 kept fields, paged with `$top=1000` + `$skip` until rows held equalled the count. All tallies below are from PULL 3, the last pull that succeeded, unless stated otherwise.

## Data files

| File | Pull | Rows | SHA-256 |
|---|---|---|---|
| [nc-disasters-pull1.csv](https://raw.githubusercontent.com/banken07/synmerco-nc-disasters/2d2a2ac4cabff3ea5ba11ed48a3e901c97e735ef/nc-disasters-pull1.csv) | PULL 1 (D2) | 1770 | `714bec8cd2bd7514507e2c317684e3e86c92fb698bdbff8bf1797297e60b91ca` |
| [nc-disasters-pull2.csv](https://raw.githubusercontent.com/banken07/synmerco-nc-disasters/2d2a2ac4cabff3ea5ba11ed48a3e901c97e735ef/nc-disasters-pull2.csv) | PULL 2 (D3) | 1770 | `cd9f28ddaad6fa4fec1e48ae81ca0bc124240dfcce5069c065bb890cfbf4f7fb` |
| [nc-disasters-pull3.csv](https://raw.githubusercontent.com/banken07/synmerco-nc-disasters/2d2a2ac4cabff3ea5ba11ed48a3e901c97e735ef/nc-disasters-pull3.csv) | PULL 3 (D4) | 1770 | `cd9f28ddaad6fa4fec1e48ae81ca0bc124240dfcce5069c065bb890cfbf4f7fb` |

Each CSV has exactly the 11 columns `id, femaDeclarationString, disasterNumber, declarationType, incidentType, declarationTitle, designatedArea, fipsCountyCode, declarationDate, incidentBeginDate, incidentEndDate`, one row per declaration row returned, sorted by declarationDate, then id; key column id.

## synmerco-data

```synmerco-data
714bec8cd2bd7514507e2c317684e3e86c92fb698bdbff8bf1797297e60b91ca nc-disasters-pull1.csv
cd9f28ddaad6fa4fec1e48ae81ca0bc124240dfcce5069c065bb890cfbf4f7fb nc-disasters-pull2.csv
cd9f28ddaad6fa4fec1e48ae81ca0bc124240dfcce5069c065bb890cfbf4f7fb nc-disasters-pull3.csv
```

## Summary counts (PULL 3)

- Rows: **1770**. Distinct disaster numbers: **51** (distinct major-disaster (DR) numbers: **29**).
- By declaration type: DR 707, EM 1049, FM 14.
- Declaration dates run 2000-01-31 to 2026-01-24. 100 counties plus 6 other designated areas (tribal areas, listed in the table below).

## County table

One row per designated area. County rows are those whose designatedArea ends in `(County)`; the county name is that area with the ending removed. Every other row is tallied on its own by its designatedArea (the 6 tribal areas are included in the table, marked as non-county areas). Columns: total rows, DR rows, most recent declaration date (as returned), and the row count by incident type. Sorted by DR rows descending, then area name.

| Area | Rows | DR | Most recent declaration | By incident type |
|---|---:|---:|---|---|
| Brunswick | 26 | 12 | 2026-01-24T00:00:00.000Z | Biological: 2, Fire: 1, Hurricane: 17, Severe Storm: 2, Tropical Storm: 3, Winter Storm: 1 |
| Ashe | 19 | 11 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 2, Hurricane: 9, Severe Storm: 3, Tropical Storm: 2, Winter Storm: 1 |
| New Hanover | 24 | 11 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 16, Severe Storm: 2, Tropical Storm: 3, Winter Storm: 1 |
| Onslow | 24 | 11 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 16, Severe Storm: 2, Tropical Storm: 3, Winter Storm: 1 |
| Alamance | 20 | 10 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 9, Severe Ice Storm: 3, Severe Storm: 2, Tropical Depression: 1, Tropical Storm: 2, Winter Storm: 1 |
| Beaufort | 23 | 10 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 15, Severe Storm: 3, Tropical Storm: 2, Winter Storm: 1 |
| Craven | 23 | 10 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 16, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Pender | 23 | 10 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 16, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Person | 20 | 10 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 9, Severe Ice Storm: 3, Severe Storm: 2, Tropical Depression: 1, Tropical Storm: 2, Winter Storm: 1 |
| Carteret | 22 | 9 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 16, Tropical Storm: 3, Winter Storm: 1 |
| Dare | 22 | 9 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 16, Tropical Storm: 3, Winter Storm: 1 |
| Davidson | 19 | 9 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 10, Severe Ice Storm: 2, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Hyde | 23 | 9 | 2026-01-24T00:00:00.000Z | Biological: 2, Fire: 1, Hurricane: 17, Tropical Storm: 2, Winter Storm: 1 |
| Jones | 22 | 9 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 16, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Madison | 17 | 9 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 1, Hurricane: 9, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Orange | 19 | 9 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 9, Severe Ice Storm: 3, Severe Storm: 1, Tropical Depression: 1, Tropical Storm: 2, Winter Storm: 1 |
| Pitt | 22 | 9 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 15, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Wilson | 21 | 9 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 12, Severe Ice Storm: 1, Severe Storm: 3, Tropical Storm: 2, Winter Storm: 1 |
| Yancey | 17 | 9 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 1, Hurricane: 9, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Alleghany | 17 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 1, Hurricane: 8, Severe Storm: 2, Tropical Storm: 3, Winter Storm: 1 |
| Avery | 16 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 2, Hurricane: 8, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Bertie | 21 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 14, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Bladen | 20 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Fire: 1, Hurricane: 13, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Burke | 17 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Fire: 1, Flood: 1, Hurricane: 7, Severe Ice Storm: 1, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Caldwell | 16 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 1, Hurricane: 7, Severe Ice Storm: 1, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Columbus | 21 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 16, Tropical Storm: 2, Winter Storm: 1 |
| Granville | 18 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 9, Severe Ice Storm: 3, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Guilford | 18 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 8, Severe Ice Storm: 3, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Hertford | 21 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 13, Severe Storm: 3, Tropical Storm: 2, Winter Storm: 1 |
| Johnston | 20 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 12, Severe Ice Storm: 1, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| McDowell | 16 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 9, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Mitchell | 16 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 1, Hurricane: 8, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Pamlico | 21 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 16, Tropical Storm: 2, Winter Storm: 1 |
| Polk | 17 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Fire: 1, Flood: 1, Hurricane: 8, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Randolph | 18 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 9, Severe Ice Storm: 2, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Robeson | 18 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 11, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Sampson | 19 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 12, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Tyrrell | 22 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Fire: 1, Hurricane: 14, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Watauga | 16 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 2, Hurricane: 8, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Wayne | 20 | 8 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 13, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Buncombe | 16 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Fire: 1, Flood: 1, Hurricane: 8, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Caswell | 17 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 8, Severe Ice Storm: 2, Severe Storm: 1, Tropical Depression: 1, Tropical Storm: 2, Winter Storm: 1 |
| Chatham | 17 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 9, Severe Ice Storm: 1, Severe Storm: 1, Tropical Depression: 1, Tropical Storm: 2, Winter Storm: 1 |
| Duplin | 20 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 14, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Eastern Band of Cherokee Indians (non-county area) | 14 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 1, Hurricane: 5, Mud/Landslide: 1, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Edgecombe | 20 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 12, Severe Ice Storm: 1, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Greene | 20 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 14, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Halifax | 20 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 12, Severe Ice Storm: 1, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Harnett | 17 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 9, Severe Ice Storm: 1, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Hoke | 17 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 10, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Jackson | 15 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 1, Hurricane: 8, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Lee | 17 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 8, Severe Ice Storm: 1, Severe Storm: 2, Tropical Storm: 3, Winter Storm: 1 |
| Lenoir | 20 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 15, Tropical Storm: 2, Winter Storm: 1 |
| Nash | 19 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 11, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 3, Winter Storm: 1 |
| Stokes | 17 | 7 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 8, Severe Ice Storm: 1, Severe Storm: 2, Tropical Storm: 3, Winter Storm: 1 |
| Alexander | 14 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 6, Severe Ice Storm: 1, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Anson | 16 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 9, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Cabarrus | 15 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 7, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 3, Winter Storm: 1 |
| Camden | 19 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 13, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Chowan | 19 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 14, Tropical Storm: 2, Winter Storm: 1 |
| Cumberland | 18 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Fire: 1, Hurricane: 11, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Currituck | 19 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 13, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Durham | 16 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 8, Severe Ice Storm: 1, Severe Storm: 1, Tropical Depression: 1, Tropical Storm: 2, Winter Storm: 1 |
| Forsyth | 16 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 8, Severe Ice Storm: 2, Tropical Storm: 3, Winter Storm: 1 |
| Haywood | 14 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 8, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Iredell | 15 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 7, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 3, Winter Storm: 1 |
| Montgomery | 16 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 9, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Moore | 16 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 8, Severe Ice Storm: 1, Severe Storm: 1, Tropical Depression: 1, Tropical Storm: 2, Winter Storm: 1 |
| Northampton | 19 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 12, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Perquimans | 19 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 13, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Rockingham | 16 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 8, Severe Ice Storm: 1, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Rutherford | 15 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Fire: 1, Hurricane: 7, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Stanly | 15 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 6, Severe Ice Storm: 1, Severe Storm: 2, Tropical Storm: 3, Winter Storm: 1 |
| Union | 15 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 7, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 3, Winter Storm: 1 |
| Vance | 16 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 9, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Wake | 16 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 8, Severe Ice Storm: 1, Severe Storm: 2, Tropical Storm: 2, Winter Storm: 1 |
| Warren | 16 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 9, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Washington | 20 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Fire: 1, Hurricane: 13, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Wilkes | 15 | 6 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 1, Hurricane: 7, Severe Storm: 1, Tropical Storm: 3, Winter Storm: 1 |
| Catawba | 13 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 1, Hurricane: 6, Severe Ice Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Cleveland | 13 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 6, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Davie | 15 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 7, Severe Ice Storm: 2, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Franklin | 15 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 8, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Gaston | 13 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 6, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Graham | 13 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 7, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Lincoln | 13 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 1, Hurricane: 6, Severe Ice Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Macon | 13 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Flood: 1, Hurricane: 7, Tropical Storm: 2, Winter Storm: 1 |
| Martin | 18 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 12, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Mecklenburg | 14 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 6, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 3, Winter Storm: 1 |
| Pasquotank | 18 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 13, Tropical Storm: 2, Winter Storm: 1 |
| Richmond | 15 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 8, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Rowan | 14 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 6, Severe Ice Storm: 1, Severe Storm: 1, Tropical Storm: 3, Winter Storm: 1 |
| Scotland | 15 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 9, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Transylvania | 14 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Fire: 1, Hurricane: 8, Tropical Storm: 2, Winter Storm: 1 |
| Yadkin | 15 | 5 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 7, Severe Storm: 2, Tropical Storm: 3, Winter Storm: 1 |
| Gates | 17 | 4 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 12, Tropical Storm: 2, Winter Storm: 1 |
| Henderson | 13 | 4 | 2026-01-24T00:00:00.000Z | Biological: 2, Fire: 1, Hurricane: 7, Tropical Storm: 2, Winter Storm: 1 |
| Swain | 14 | 4 | 2026-01-24T00:00:00.000Z | Biological: 2, Fire: 2, Hurricane: 6, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Cherokee | 11 | 3 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 5, Severe Storm: 1, Tropical Storm: 2, Winter Storm: 1 |
| Surry | 13 | 3 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 7, Tropical Storm: 3, Winter Storm: 1 |
| Clay | 10 | 2 | 2026-01-24T00:00:00.000Z | Biological: 2, Hurricane: 5, Tropical Storm: 2, Winter Storm: 1 |
| Coharie (TDSA) (non-county area) | 1 | 1 | 2020-03-25T00:00:00.000Z | Biological: 1 |
| Haliwa-Saponi (TDSA) (non-county area) | 1 | 1 | 2020-03-25T00:00:00.000Z | Biological: 1 |
| Lumbee (TDSA) (non-county area) | 2 | 1 | 2026-01-24T00:00:00.000Z | Biological: 1, Winter Storm: 1 |
| Meherrin (TDSA) (non-county area) | 1 | 1 | 2020-03-25T00:00:00.000Z | Biological: 1 |
| Waccamaw Siouan (TDSA) (non-county area) | 1 | 1 | 2020-03-25T00:00:00.000Z | Biological: 1 |

## County ranking — top 15 by DR declarations (ties: area name)

| Rank | County | DR declarations | Total rows | Most recent declaration |
|---:|---|---:|---:|---|
| 1 | Brunswick | 12 | 26 | 2026-01-24T00:00:00.000Z |
| 2 | Ashe | 11 | 19 | 2026-01-24T00:00:00.000Z |
| 3 | New Hanover | 11 | 24 | 2026-01-24T00:00:00.000Z |
| 4 | Onslow | 11 | 24 | 2026-01-24T00:00:00.000Z |
| 5 | Alamance | 10 | 20 | 2026-01-24T00:00:00.000Z |
| 6 | Beaufort | 10 | 23 | 2026-01-24T00:00:00.000Z |
| 7 | Craven | 10 | 23 | 2026-01-24T00:00:00.000Z |
| 8 | Pender | 10 | 23 | 2026-01-24T00:00:00.000Z |
| 9 | Person | 10 | 20 | 2026-01-24T00:00:00.000Z |
| 10 | Carteret | 9 | 22 | 2026-01-24T00:00:00.000Z |
| 11 | Dare | 9 | 22 | 2026-01-24T00:00:00.000Z |
| 12 | Davidson | 9 | 19 | 2026-01-24T00:00:00.000Z |
| 13 | Hyde | 9 | 23 | 2026-01-24T00:00:00.000Z |
| 14 | Jones | 9 | 22 | 2026-01-24T00:00:00.000Z |
| 15 | Madison | 9 | 17 | 2026-01-24T00:00:00.000Z |

Top-ranked county: **Brunswick** with 12 DR declarations. 10 counties have 9 DR declarations; the tie-break by name takes Carteret, Dare, Davidson, Hyde, Jones and Madison into the top 15, ahead of Orange, Pitt, Wilson and Yancey (also 9 each).

## Distinct DR disaster numbers by federal fiscal year

Federal fiscal year starts 1 October; the year is taken from declarationDate. Every fiscal year from 2000 to 2026 is listed, including years with no DR disaster.

| Federal fiscal year | Distinct DR disaster numbers |
|---:|---:|
| 2000 | 1 |
| 2001 | 0 |
| 2002 | 0 |
| 2003 | 3 |
| 2004 | 2 |
| 2005 | 0 |
| 2006 | 1 |
| 2007 | 0 |
| 2008 | 0 |
| 2009 | 1 |
| 2010 | 1 |
| 2011 | 3 |
| 2012 | 0 |
| 2013 | 2 |
| 2014 | 2 |
| 2015 | 0 |
| 2016 | 0 |
| 2017 | 1 |
| 2018 | 2 |
| 2019 | 1 |
| 2020 | 3 |
| 2021 | 3 |
| 2022 | 0 |
| 2023 | 0 |
| 2024 | 1 |
| 2025 | 2 |
| 2026 | 0 |
| **Total** | **29** |

## Distinct DR disaster numbers by incident type

| Incident type | Distinct DR disaster numbers |
|---|---:|
| Hurricane | 11 |
| Severe Storm | 8 |
| Severe Ice Storm | 3 |
| Flood | 2 |
| Tropical Storm | 2 |
| Biological | 1 |
| Mud/Landslide | 1 |
| Tropical Depression | 1 |
| **Total** | **29** |

## Disasters lasting a month or more

Per distinct disaster number (all declaration types): earliest incidentBeginDate across its rows and latest incidentEndDate across its rows. Listed when the latest end falls on or after the same day of the following month counted from the earliest begin (if that month has no such day, its last day). A disaster with no end date on any row is listed as open.

| Disaster number | Declaration types | Incident types | Earliest begin | Latest end |
|---:|---|---|---|---|
| 2773 | FM | Fire | 2008-06-13 | open |
| 2936 | FM | Fire | 2011-07-04 | open |
| 3222 | EM | Hurricane | 2005-08-29 | 2005-10-01 |
| 3471 | EM | Biological | 2020-01-20 | 2023-05-11 |
| 3617 | EM | Tropical Storm | 2024-09-25 | 2024-12-18 |
| 4487 | DR | Biological | 2020-01-20 | 2023-05-11 |
| 4827 | DR | Tropical Storm | 2024-09-25 | 2024-12-18 |
| 5574 | FM | Fire | 2025-03-19 | open |
| 5577 | FM | Fire | 2025-03-25 | open |
| 5578 | FM | Fire | 2025-03-26 | open |
| 5580 | FM | Fire | 2025-04-18 | open |
| 5582 | FM | Fire | 2025-05-02 | open |

Total: **12** disaster numbers (7 open, all Fire / FM; 5 closed).

## Changes — PULL 2 vs PULL 1

- New: **102** (key only in the later pull). Gone: **102** (key only in the earlier pull). Changed: **0** (same key, a column after id differs).
- Rows: 1770 (PULL 1) → 1770 (PULL 2). Check: 1770 + 102 − 102 = 1770 (matches the later row count).
- New keys:
  - `0274aa49-7545-49ef-8d48-b64982ac92fb`
  - `02b3d532-0952-46ed-9e59-b43aa3d80ab0`
  - `0b50bab2-c505-4850-b043-4779c9cb9768`
  - `0b91ae83-6739-4bc1-adef-30404a8496de`
  - `0ef27e88-ab15-451b-8fde-d86583b32060`
  - `0f79462d-8bc3-4b3d-8b61-55f9e5e9d67a`
  - `10d0cecb-1973-4a9d-a5a6-c9bec2635954`
  - `12bbb123-f59e-4bd3-a6f0-7e467423ba01`
  - `12dc79e6-abc1-4d62-aaf6-725e06e0e5b8`
  - `14593bc0-7af3-4e21-96f8-d8775c737690`
  - `15820ad2-4212-4bc1-a8bf-534a929d42da`
  - `166d85af-629a-4eb4-a496-62248782ac8e`
  - `197d6ef1-edbc-4538-9b53-d346f72b323d`
  - `1bd76a29-4d1f-476b-84ef-2ea95c699042`
  - `1be3365f-684a-43f2-9e12-09db50a93923`
  - `1d6ca9f1-3374-4231-bda9-14b177a8d8c5`
  - `2a320a69-443d-496e-b5a6-608ba0df6dc7`
  - `2ee001ae-1a40-42d8-8b76-442a9174535e`
  - `3039e745-2739-4ea6-9f6d-5b72c04fc19f`
  - `30a1e893-5744-4f08-8aab-784dc1076f8b`
  - `33a0b979-b6be-4377-8b63-9246164e8520`
  - `3a964a7b-61b3-4b0d-bcaf-2ca75456359e`
  - `3ad58fcb-cf9e-4bb1-8b40-80ba73ab0be1`
  - `3c6b0958-d232-49af-a320-dc6740a3629d`
  - `3c8605ab-c92b-42e7-8d2a-fcf1be6d25e1`
  - `41f36181-2249-4533-be38-f77341564fc3`
  - `434f75db-0ef4-4f15-b899-7fdb50f5f321`
  - `44d06dd7-0c39-4e6d-8fd5-a7ca7a0f4513`
  - `4715e5e9-f635-4c7d-9b4f-0520ce567bdf`
  - `49b6a89b-82b8-457b-bd47-312bf3f2dcf5`
  - `4c20ae2c-72b2-445c-a43b-91fc5700be1b`
  - `4ff7ec87-e2a0-41e0-bbd6-3dd63a472857`
  - `501aba55-2f07-4c17-bd2d-55f2731d3e6b`
  - `57fa36e6-5d11-4412-ae39-6c58145dfcfc`
  - `58d3dc12-4fb6-45b9-be73-5d9255bb553a`
  - `59effcce-ac04-4bd3-8dac-8d18c1578a0b`
  - `5b61d910-7170-486d-9d9a-9df3795ad114`
  - `655141e0-50d0-4905-bb3e-3f0279e184a9`
  - `672f487f-4c0b-423d-ba5b-ebecb83a7a49`
  - `761e1fb8-0c29-4700-b096-9e7f7b3e6199`
  - `762a1266-24f8-4b38-af10-a130c77d4ab9`
  - `77e59d2c-530c-4838-80c2-f837cdc87771`
  - `7b1b8f50-8807-4cfd-86b2-3f322a8738d7`
  - `7d62ae86-6405-4f4c-9add-d5562618cdf2`
  - `8295b85d-f376-4605-a51f-fa67cc64aee6`
  - `83b82253-0705-4b7b-bc9a-30f890f996ad`
  - `8dc43e4a-9dc1-4a61-8c56-454ec05e09c8`
  - `91baec04-26fd-4b68-b3d9-019c1bdc626b`
  - `966f821c-73f0-45ec-a07e-81c0a9bf9ff3`
  - `96d6f1bd-8db0-4f7e-a9f4-50fbec270766`
  - `9a3702dd-ba5c-4d3b-ba05-c541f40a4947`
  - `9ff90fd5-8bff-4228-8f3c-002c78251f85`
  - `a25437ae-5394-4c41-b496-788ee9b5ac57`
  - `a6a5b2d1-95d2-475f-afae-d2c9d1105a8d`
  - `a7df691d-cb95-46ec-9fa0-f0844c5772f8`
  - `b1e16000-0dfa-4b90-9a31-07103c4470d3`
  - `b215cdfc-83e2-44b8-8090-0a04c3d1aa80`
  - `b23caaa7-280d-4d4d-9120-55742308fd26`
  - `b33bb7c3-d0a4-46cb-8c98-711beeede1d4`
  - `b3535b94-6233-4533-8da4-a0d8d8ae89d9`
  - `b6a96b6d-afeb-444c-a2d1-dafcdde865a4`
  - `b7a0de19-fbed-46f5-8cfa-56c8feb8066c`
  - `bab38cfa-35d0-4b71-8a5e-fdd5fb45701d`
  - `bb1a3084-d42d-4665-bd54-b623901e6059`
  - `bb6b7af0-ba92-41bf-8f15-fe26f5615faa`
  - `bdae6995-94bb-487f-8bfd-991fcab54960`
  - `be5f5c9e-037f-44ef-ba74-e91f1b09d21f`
  - `c223f09f-c478-4949-9977-e6b73c941a69`
  - `c2c25d6d-faa8-48c3-b582-38c8fd1454ae`
  - `c4ecf85c-b216-453d-a866-1193b534b1b6`
  - `c534a570-98ef-4dd6-874c-90f410c9c5c3`
  - `c932f486-f1d6-4225-90e9-22d5f5279cef`
  - `c9564af1-a7a2-43a3-b632-d206e5cba227`
  - `cb0ccd43-293d-4a45-980b-9997d022cc91`
  - `cb16420d-c396-45e7-9da6-31bc97daa00a`
  - `ccbddcac-dc70-410a-85aa-d030f1329345`
  - `cd28a8ec-6c6a-422b-8868-ac96e50bb28d`
  - `cf30e0c0-3a92-4d1c-b2cf-f742439aa977`
  - `cfaee83d-0384-4600-aebb-12d53a3ac174`
  - `d019f33f-aee5-428a-82b6-8f4739b51b29`
  - `d0409800-3651-4562-96ad-a25b57e64a3a`
  - `d30e9074-abe5-4442-84a6-db7b59fed82b`
  - `d4282f41-e1d4-4924-80af-e01f54651d80`
  - `d6ae4daa-1eb2-4bc6-8850-057986721cab`
  - `d8820a1f-992d-4f64-a1e9-4cb9cbc90e11`
  - `db6cfe76-deec-4666-976c-57ed398eed32`
  - `dc20e19d-5845-43e7-9222-10a88f95c50c`
  - `dd53674c-4a86-4551-89d2-98260a77825a`
  - `e1ad6099-12f4-4669-aecb-b74f05ec255a`
  - `e4321322-7a30-4a81-9cc8-019dadc355ad`
  - `e43f704c-dee9-4eb1-9a30-53eb9e5db948`
  - `e4bfe9f4-cd0e-445d-8146-3c52ea8385f3`
  - `ea72acb5-39cb-425e-b597-005a84ec97ea`
  - `ed021a73-bf53-4398-bf25-1045b586650e`
  - `ef91b360-e96f-43b7-b254-aa039d36a6c3`
  - `efddf377-a6c0-4d1e-9b32-9ab1a6ebb9c1`
  - `f08a190a-b3b8-4e7a-a216-aa5c54c5e7dd`
  - `f16fcc07-aa7d-456f-906f-059d53c2deb6`
  - `f6ed3715-436e-4775-9899-28a60aec873c`
  - `f76c7b2e-6ee1-4d2a-aeb4-059a36b3d469`
  - `fad8cbe1-4a0d-4c43-8784-27dfda96b9ff`
  - `fb51b7b8-df2b-450e-8622-53c3adc46c31`
- Gone keys:
  - `018d4354-9bae-4499-9fcd-e7c7d26dba3b`
  - `06e40808-f1cb-4119-bc17-0cd07abb76da`
  - `0cc0c639-409f-4370-be81-7b83966f3280`
  - `0d73e76d-f77b-44a3-b01e-7b83b29b0254`
  - `1073b0c6-1a4c-4e92-a17b-75ed24859c79`
  - `1a1f242a-4438-4166-8332-2cb276e43efd`
  - `1e731c96-b08e-4587-a2f9-50fe07fdf7bb`
  - `20e4d73a-46e2-4214-86c6-89859f3f1ba4`
  - `22089fa4-d7a2-47c4-9475-1af15d359c45`
  - `2383fe17-1374-4f02-8b08-4858b51141d7`
  - `23a87afa-b044-4396-b859-61df4647d966`
  - `23b1eae6-1cf9-4d92-8838-57c06ee1b4e2`
  - `29931745-3ade-4a1c-ab19-1362796957ef`
  - `2e3f6598-6020-4c58-a87a-6b7ac510990e`
  - `2e8c15af-9b9a-430d-ab11-25d2ce09e08e`
  - `2f7290cd-ec62-47a0-b064-7904279a9c44`
  - `308e015d-b014-4f6f-b71d-d47eac23d43d`
  - `3887d060-3587-4d9b-810c-a18ed7b14419`
  - `3b0521c2-a67f-4d81-9260-5ee3e9e7eed4`
  - `3d9403a6-b641-4dfb-bff9-841ac972544e`
  - `3ee1695f-b426-4fdf-82be-e781e86c2956`
  - `3fb40016-1f39-4d9b-8bcc-71ab0e111c4f`
  - `404cc41c-27f8-4f22-9edd-e49223b0aaa1`
  - `40ebac7b-5155-4097-9e01-976bde95f0f3`
  - `41a8acb5-5a4d-4320-957f-cdf178b729ed`
  - `440a4a6e-bbd9-45f1-b551-477eb25318c6`
  - `4527a4c8-8ebb-4970-9122-eaab25a3404c`
  - `45ee0aa6-5826-4315-bb13-123d411da3dc`
  - `48978496-4708-44a7-b977-1b81398e7835`
  - `4ec013f9-46eb-4f62-a3db-ebfdf91b0c01`
  - `4f709b9d-424d-4273-833f-f4623ea27b8f`
  - `51451555-cefb-4ded-ad4b-1cbe10537c58`
  - `514569eb-e51c-4b6b-8c54-d5121ad2f077`
  - `51e1bf0c-1e50-4a5c-ae07-b2ad77a63a93`
  - `5328d491-e844-4c27-837d-f0f33a0025fd`
  - `54e351ba-5b1e-4d64-afe6-1b8f9516794b`
  - `554ab68f-1328-4e4d-9db7-bfa1f8b41c87`
  - `55b86ab7-1cbb-4109-939c-2fd6dc8fdabb`
  - `5fff1ade-33b9-4ba8-a2b8-c1d9b9357f6f`
  - `691c9134-b059-4ec9-9c04-d986465aaa57`
  - `6a9f525b-1387-40f1-a25e-b2049784b334`
  - `6dd7d5fa-5caf-4db9-8fa2-4ceaf10f278d`
  - `6eb4986a-74c7-481f-9a85-328050894c48`
  - `70a89abf-e6bb-4ac1-bee5-6cb7b4335544`
  - `712e42e2-2947-45ac-a01b-1d0b46d27476`
  - `74114e9a-e617-40e2-a8a8-868637710a00`
  - `767f6313-6d68-4910-9343-99041c9ba4cd`
  - `77f035ee-8761-45a3-a4cf-553f7bd7226b`
  - `78cfa7f2-2f43-4363-a9c0-0381b2d6f8b7`
  - `7c236b07-f78f-4887-b539-16b3e3bca18c`
  - `7d09083f-19a7-43b5-baf1-8d48e027456e`
  - `859c7093-8b30-473a-bfc8-ee27cc76e694`
  - `85b9abb5-2372-4b11-8546-d716e2570dd9`
  - `8709f376-5cfd-4e6a-ac60-648348e83e91`
  - `87df60c3-dd67-4531-82ae-d2ff723e4491`
  - `8bc7d862-52e3-4691-9521-068e3b848452`
  - `8c20932b-97a6-475a-b284-58b5c81354d1`
  - `8ecb4e8a-8f13-42a0-b4f5-88f9e3e84fd2`
  - `904b9d83-6ddb-473a-95c8-59a41c574441`
  - `945d480d-7ff8-48d5-894a-f7675ca7374a`
  - `96bfa236-1833-4cf2-ad54-391982b4ca57`
  - `9872e500-d90d-4d34-a9aa-28704275d625`
  - `9ae28373-1aff-4d94-9f17-33e05f7e38ec`
  - `9e083327-10e3-4ed0-aa94-b307e436f4a8`
  - `a0e18a16-cdfa-4540-b93a-e3aab20945b4`
  - `a1c92847-bbff-4690-b1d7-c4dd4faaedac`
  - `aa472bda-2755-4612-8572-8ea7c0fff5b1`
  - `aafb7445-41f0-449f-948f-c1950fa1b3e1`
  - `af73fd91-d63a-4cb6-928d-d9bfbdb2b5d3`
  - `b018c4b7-da68-45ac-ba18-225b23b339de`
  - `b07d25cb-6129-44c5-9bf9-74fd62641c90`
  - `b2515c32-e856-4f3a-8542-b78a5b969c3b`
  - `b578737b-c53a-4601-97bb-94af11626ec4`
  - `b6d020cf-b419-4dd2-ab2f-1d6a07df802d`
  - `b8a4ffef-3f15-4b48-a143-b26d700b8fef`
  - `baeb2d2e-a453-4437-97db-80bd73068638`
  - `bdb37f38-ed69-451f-82c1-49f19ef3d45a`
  - `c180a125-100d-49e9-b071-b37ef9f4eaa4`
  - `c37c89fc-ed56-438b-852d-5175c5faadfc`
  - `c3afcc6f-a582-4e1f-8a2f-8a5247aa4979`
  - `cacd83d0-d1f7-4003-9375-711adc3529b6`
  - `d48f51cc-7362-4721-a0af-9dffb105e449`
  - `d588606f-0763-4105-aa1c-8084654e24bf`
  - `db53774f-e5b4-4ef1-b15a-f7091d9e1706`
  - `dff80d92-076c-4799-9df0-647acca2d39d`
  - `e290f0a2-5e8c-48fa-838d-381b845b8297`
  - `e6e0c415-2a41-4c62-9a5c-8336844c4b62`
  - `e8750d0b-2539-411b-ba9e-ebac4b29db5f`
  - `eaaba696-3c61-484d-a81b-b8cf9107d36f`
  - `eb2b014d-529e-4cbc-a7a3-18fe941dc4a1`
  - `eb6b3e04-0a6c-493d-9ef6-ed7afbb3d97a`
  - `ed531694-d6c4-4db4-a215-e9cd9f1aa2d3`
  - `ed8e9f8e-a9b1-47e8-b534-5c0f1d7a3ded`
  - `f0d92f6f-151d-4d15-83c7-f8c7f8aff4a1`
  - `f7f6cff7-166f-48e6-81e4-75fd471ee5d6`
  - `f810f445-d937-4f29-864e-415bbdcfa386`
  - `fa929c6f-c336-402b-883d-3d0bc25725e4`
  - `fcdd0487-6cd2-4c1b-a7b5-255ddc1d2719`
  - `fe0c9d04-0415-40de-9768-fe18fa2e8e60`
  - `ff2be4b4-f1ae-4ed6-9834-1e35f8051758`
  - `ff61ee51-f7bd-42ab-a3b9-ba82c531dfd8`
  - `ffcaa459-f36f-46e5-a0aa-81e95520a6a1`
- Changed: none.

Note on PULL 2 vs PULL 1: the 102 new rows and the 102 gone rows match exactly on every column except id — the same 102 declarations re-issued by the source under new row ids between the two pulls. No shared key changed any value.

## Changes — PULL 3 vs PULL 2

- New: **0** (key only in the later pull). Gone: **0** (key only in the earlier pull). Changed: **0** (same key, a column after id differs).
- Rows: 1770 (PULL 2) → 1770 (PULL 3). Check: 1770 + 0 − 0 = 1770 (matches the later row count).
- **No change** — both pulls hold 1770 rows with identical SHA-256.

## PROOF

One line per request: the full request URL, the UTC time it was made, and the HTTP status. Under each pull, its first response's Date header line copied exactly (the pull's source time), then each response's metadata object with its count, word for word as returned.

### PULL 1

Source time (first response Date header): `Tue, 24 Nov 2026 20:17:40 GMT`

1. `https://www.fema.gov/api/open/v2/DisasterDeclarationsSummaries?$filter=state%20eq%20'NC'%20and%20fyDeclared%20ge%202000&$inlinecount=allpages&$select=id,femaDeclarationString,disasterNumber,declarationType,incidentType,declarationTitle,designatedArea,fipsCountyCode,declarationDate,incidentBeginDate,incidentEndDate&$top=1000&$skip=0` — UTC 2026-11-24T20:17:37.865Z — HTTP 200
2. `https://www.fema.gov/api/open/v2/DisasterDeclarationsSummaries?$filter=state%20eq%20'NC'%20and%20fyDeclared%20ge%202000&$inlinecount=allpages&$select=id,femaDeclarationString,disasterNumber,declarationType,incidentType,declarationTitle,designatedArea,fipsCountyCode,declarationDate,incidentBeginDate,incidentEndDate&$top=1000&$skip=1000` — UTC 2026-11-24T20:17:39.575Z — HTTP 200

Metadata, response 1 (count 1770):
`{"skip": 0, "select": "id, femaDeclarationString, disasterNumber, declarationType, incidentType, declarationTitle, designatedArea, fipsCountyCode, declarationDate, incidentBeginDate, incidentEndDate", "rundate": "2026-11-24T20:17:40.136Z", "top": 1000, "filter": "state eq 'NC' and fyDeclared ge 2000", "format": "json", "metadata": true, "orderby": "", "entityname": "DisasterDeclarationsSummaries", "version": "v2", "url": "/api/open/v2/DisasterDeclarationsSummaries?$filter=state%20eq%20%27NC%27%20and%20fyDeclared%20ge%202000&$inlinecount=allpages&$select=id,femaDeclarationString,disasterNumber,declarationType,incidentType,declarationTitle,designatedArea,fipsCountyCode,declarationDate,incidentBeginDate,incidentEndDate&$top=1000&$skip=0", "count": 1770}`

Metadata, response 2 (count 1770):
`{"skip": 1000, "select": "id, femaDeclarationString, disasterNumber, declarationType, incidentType, declarationTitle, designatedArea, fipsCountyCode, declarationDate, incidentBeginDate, incidentEndDate", "rundate": "2026-11-24T20:17:41.085Z", "top": 1000, "filter": "state eq 'NC' and fyDeclared ge 2000", "format": "json", "metadata": true, "orderby": "", "entityname": "DisasterDeclarationsSummaries", "version": "v2", "url": "/api/open/v2/DisasterDeclarationsSummaries?$filter=state%20eq%20%27NC%27%20and%20fyDeclared%20ge%202000&$inlinecount=allpages&$select=id,femaDeclarationString,disasterNumber,declarationType,incidentType,declarationTitle,designatedArea,fipsCountyCode,declarationDate,incidentBeginDate,incidentEndDate&$top=1000&$skip=1000", "count": 1770}`

### PULL 2

Source time (first response Date header): `Fri, 27 Nov 2026 01:19:13 GMT`

1. `https://www.fema.gov/api/open/v2/DisasterDeclarationsSummaries?$filter=state%20eq%20'NC'%20and%20fyDeclared%20ge%202000&$inlinecount=allpages&$select=id,femaDeclarationString,disasterNumber,declarationType,incidentType,declarationTitle,designatedArea,fipsCountyCode,declarationDate,incidentBeginDate,incidentEndDate&$top=1000&$skip=0` — UTC 2026-11-27T01:19:10.768Z — HTTP 200
2. `https://www.fema.gov/api/open/v2/DisasterDeclarationsSummaries?$filter=state%20eq%20'NC'%20and%20fyDeclared%20ge%202000&$inlinecount=allpages&$select=id,femaDeclarationString,disasterNumber,declarationType,incidentType,declarationTitle,designatedArea,fipsCountyCode,declarationDate,incidentBeginDate,incidentEndDate&$top=1000&$skip=1000` — UTC 2026-11-27T01:19:12.593Z — HTTP 200

Metadata, response 1 (count 1770):
`{"skip": 0, "select": "id, femaDeclarationString, disasterNumber, declarationType, incidentType, declarationTitle, designatedArea, fipsCountyCode, declarationDate, incidentBeginDate, incidentEndDate", "rundate": "2026-11-27T01:19:13.163Z", "top": 1000, "filter": "state eq 'NC' and fyDeclared ge 2000", "format": "json", "metadata": true, "orderby": "", "entityname": "DisasterDeclarationsSummaries", "version": "v2", "url": "/api/open/v2/DisasterDeclarationsSummaries?$filter=state%20eq%20%27NC%27%20and%20fyDeclared%20ge%202000&$inlinecount=allpages&$select=id,femaDeclarationString,disasterNumber,declarationType,incidentType,declarationTitle,designatedArea,fipsCountyCode,declarationDate,incidentBeginDate,incidentEndDate&$top=1000&$skip=0", "count": 1770}`

Metadata, response 2 (count 1770):
`{"skip": 1000, "select": "id, femaDeclarationString, disasterNumber, declarationType, incidentType, declarationTitle, designatedArea, fipsCountyCode, declarationDate, incidentBeginDate, incidentEndDate", "rundate": "2026-11-27T01:19:13.957Z", "top": 1000, "filter": "state eq 'NC' and fyDeclared ge 2000", "format": "json", "metadata": true, "orderby": "", "entityname": "DisasterDeclarationsSummaries", "version": "v2", "url": "/api/open/v2/DisasterDeclarationsSummaries?$filter=state%20eq%20%27NC%27%20and%20fyDeclared%20ge%202000&$inlinecount=allpages&$select=id,femaDeclarationString,disasterNumber,declarationType,incidentType,declarationTitle,designatedArea,fipsCountyCode,declarationDate,incidentBeginDate,incidentEndDate&$top=1000&$skip=1000", "count": 1770}`

### PULL 3

Source time (first response Date header): `Sat, 28 Nov 2026 01:29:20 GMT`

1. `https://www.fema.gov/api/open/v2/DisasterDeclarationsSummaries?$filter=state%20eq%20'NC'%20and%20fyDeclared%20ge%202000&$inlinecount=allpages&$select=id,femaDeclarationString,disasterNumber,declarationType,incidentType,declarationTitle,designatedArea,fipsCountyCode,declarationDate,incidentBeginDate,incidentEndDate&$top=1000&$skip=0` — UTC 2026-11-28T01:29:17.657Z — HTTP 200
2. `https://www.fema.gov/api/open/v2/DisasterDeclarationsSummaries?$filter=state%20eq%20'NC'%20and%20fyDeclared%20ge%202000&$inlinecount=allpages&$select=id,femaDeclarationString,disasterNumber,declarationType,incidentType,declarationTitle,designatedArea,fipsCountyCode,declarationDate,incidentBeginDate,incidentEndDate&$top=1000&$skip=1000` — UTC 2026-11-28T01:29:20.417Z — HTTP 200

Metadata, response 1 (count 1770):
`{"skip": 0, "select": "id, femaDeclarationString, disasterNumber, declarationType, incidentType, declarationTitle, designatedArea, fipsCountyCode, declarationDate, incidentBeginDate, incidentEndDate", "rundate": "2026-11-28T01:29:20.609Z", "top": 1000, "filter": "state eq 'NC' and fyDeclared ge 2000", "format": "json", "metadata": true, "orderby": "", "entityname": "DisasterDeclarationsSummaries", "version": "v2", "url": "/api/open/v2/DisasterDeclarationsSummaries?$filter=state%20eq%20%27NC%27%20and%20fyDeclared%20ge%202000&$inlinecount=allpages&$select=id,femaDeclarationString,disasterNumber,declarationType,incidentType,declarationTitle,designatedArea,fipsCountyCode,declarationDate,incidentBeginDate,incidentEndDate&$top=1000&$skip=0", "count": 1770}`

Metadata, response 2 (count 1770):
`{"skip": 1000, "select": "id, femaDeclarationString, disasterNumber, declarationType, incidentType, declarationTitle, designatedArea, fipsCountyCode, declarationDate, incidentBeginDate, incidentEndDate", "rundate": "2026-11-28T01:29:22.338Z", "top": 1000, "filter": "state eq 'NC' and fyDeclared ge 2000", "format": "json", "metadata": true, "orderby": "", "entityname": "DisasterDeclarationsSummaries", "version": "v2", "url": "/api/open/v2/DisasterDeclarationsSummaries?$filter=state%20eq%20%27NC%27%20and%20fyDeclared%20ge%202000&$inlinecount=allpages&$select=id,femaDeclarationString,disasterNumber,declarationType,incidentType,declarationTitle,designatedArea,fipsCountyCode,declarationDate,incidentBeginDate,incidentEndDate&$top=1000&$skip=1000", "count": 1770}`

### Top-ranked county DR rows (PULL 3, as returned)

The DR rows of the top-ranked county, Brunswick (12 rows), from nc-disasters-pull3.csv, one per line, in the CSV's order (declarationDate, then id):

aff3ddd8-3595-4c7f-a400-41093069a8fb,DR-1490-NC,1490,DR,Hurricane,HURRICANE ISABEL,Brunswick (County),019,2003-09-18T00:00:00.000Z,2003-09-18T00:00:00.000Z,2003-09-26T00:00:00.000Z
cee84c25-88d5-4a15-a4c8-04d9970de19e,DR-1608-NC,1608,DR,Hurricane,HURRICANE OPHELIA,Brunswick (County),019,2005-10-07T00:00:00.000Z,2005-09-11T00:00:00.000Z,2005-09-17T00:00:00.000Z
784a3c93-9a88-4711-9d8f-eadb36b706c3,DR-1801-NC,1801,DR,Severe Storm,TROPICAL STORM HANNA,Brunswick (County),019,2008-10-08T00:00:00.000Z,2008-09-04T00:00:00.000Z,2008-09-15T00:00:00.000Z
f1029242-eb0a-444c-b54b-2e5ec355987a,DR-1942-NC,1942,DR,Severe Storm,SEVERE STORMS, FLOODING, AND STRAIGHT-LINE WINDS,Brunswick (County),019,2010-10-14T00:00:00.000Z,2010-09-27T00:00:00.000Z,2010-10-01T00:00:00.000Z
0d877597-2b99-413f-86b1-ef13c72a460b,DR-4019-NC,4019,DR,Hurricane,HURRICANE IRENE,Brunswick (County),019,2011-08-31T00:00:00.000Z,2011-08-25T00:00:00.000Z,2011-09-01T00:00:00.000Z
9f5bb37c-24c4-4d6a-a529-915c570e9c4f,DR-4285-NC,4285,DR,Hurricane,HURRICANE MATTHEW,Brunswick (County),019,2016-10-10T00:00:00.000Z,2016-10-04T00:00:00.000Z,2016-10-24T00:00:00.000Z
a7b7a579-8baf-42aa-94a8-8f264e73421e,DR-4393-NC,4393,DR,Hurricane,HURRICANE FLORENCE,Brunswick (County),019,2018-09-14T00:00:00.000Z,2018-09-07T00:00:00.000Z,2018-09-29T00:00:00.000Z
be8e35d1-0f37-4cfa-b97b-9dea92c3d015,DR-4412-NC,4412,DR,Hurricane,TROPICAL STORM MICHAEL,Brunswick (County),019,2019-01-31T00:00:00.000Z,2018-10-10T00:00:00.000Z,2018-10-12T00:00:00.000Z
99e0c00d-66bb-4d77-a343-a06d7ddf7692,DR-4465-NC,4465,DR,Hurricane,HURRICANE DORIAN,Brunswick (County),019,2019-10-04T00:00:00.000Z,2019-09-01T00:00:00.000Z,2019-09-09T00:00:00.000Z
3c0e575d-5895-49f2-9ac9-f8c33e9ec8ef,DR-4487-NC,4487,DR,Biological,COVID-19 PANDEMIC,Brunswick (County),019,2020-03-25T00:00:00.000Z,2020-01-20T00:00:00.000Z,2023-05-11T00:00:00.000Z
7b2d4ae5-3699-45ab-be56-2140411eefdb,DR-4568-NC,4568,DR,Hurricane,HURRICANE ISAIAS,Brunswick (County),019,2020-10-14T00:00:00.000Z,2020-07-31T00:00:00.000Z,2020-08-04T00:00:00.000Z
ac8eb6c5-324c-4607-92ca-19ffbe75a50b,DR-4837-NC,4837,DR,Tropical Storm,POTENTIAL TROPICAL CYCLONE EIGHT,Brunswick (County),019,2024-10-19T00:00:00.000Z,2024-09-16T00:00:00.000Z,2024-09-20T00:00:00.000Z

## Method and pull notes

- County: designatedArea ending in `(County)`, name with that ending removed; all other areas tallied on their own by designatedArea.
- Federal fiscal year: 1 October start, taken from declarationDate.
- Month-long rule: per distinct disaster number, earliest incidentBeginDate to latest incidentEndDate; listed at one calendar month or more (month-end clamped); no end date on any row means open.
- PULL 1 note filed 2026-11-24T20:18:37Z (1,770 rows, SHA-256 714bec8cd2bd7514507e2c317684e3e86c92fb698bdbff8bf1797297e60b91ca).
- PULL 2 was first filed 2026-11-25T19:50:34Z (1,770 rows, SHA-256 cd9f28ddaad6fa4fec1e48ae81ca0bc124240dfcce5069c065bb890cfbf4f7fb), 28 minutes short of the 24-hour wait; a corrected note, `Corrected PULL 2:`, was filed 2026-11-25T23:46:05Z with the same data and SHA-256. The first delivery built on those pulls was held, not judged: the platform measures the note starting `PULL 2:` and does not count a `Corrected PULL 2:` note.
- Per the platform's instruction, PULL 2 was pulled again and a new note starting `PULL 2:` was filed 2026-11-27T01:19:35Z (1,770 rows, same SHA-256 — the source data is unchanged). A first PULL 3 note was filed 2026-11-26T23:51:18Z and was superseded by the re-pull: PULL 3 was pulled again with a new note filed 2026-11-28T01:30:17Z (1,770 rows, same SHA-256), 24 hours 10 minutes after the re-filed PULL 2 note. This report is built on the re-pulled PULL 2 and PULL 3. Each good pull's source time is later than the previous good pull's.
- Retrieval times (UTC): PULL 1 on 2026-11-24 ~20:17, PULL 2 on 2026-11-27 ~01:19, PULL 3 on 2026-11-28 ~01:29; see the PROOF request lines for the exact times.
