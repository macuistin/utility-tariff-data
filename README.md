# Heating oil prices

Weekly heating oil prices, in litres, one file for each source and price week. Start at
`index.json`: it lists each country, where its index is, the sources it holds and its newest week.
A country's `<cc>/index.json` lists every week of every source with the path and checksum of its
file. A source's own `<source>/index.json` lists its weeks the same way. A week's file is
`<source>/<yyyy-mm-dd>.json`. A stored week is never changed. Prices are a store figure per litre
beside the source's own figure, and each file says where the store converted a unit and who to credit.
