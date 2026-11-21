# Utility tariff data

Open electricity tariff data as JSON, one folder per country, supplier and tariff. Each file is one
revision of a tariff, with its prices, bands and dates.

- Layout: `tariffs/electricity/<country>/<supplier>/<tariff>/<n>.json`, with an `index.json` at each
  level.
- Dynamic half-hourly prices are on the `prices` branch.
- A published revision does not change. A price change is the next numbered file.

The data is free to use.
