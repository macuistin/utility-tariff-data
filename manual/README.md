# Prices typed by hand

Each file here holds prices a person or an assistant typed from a published document that a script
cannot read: a PDF of page images, or a site that refuses a script. A sync source in
`macuistin/utility-tariffs` reads the file, checks it as it would a live answer, and writes the
tariff files under `tariffs/`.

| File | Read by | Typed from |
| --- | --- | --- |
| `ceb-tariff-2026-05.txt` | `mu_ceb` | Mauritius Government Gazette, General Notice No. 473 of 2026 (CEB tariffs) |
| `pln-tariff-2026-q4.txt` | `id_pln` | PLN's tariff adjustment notice for October to December 2026 |
| `pge-dystrybucja-G11-2026.txt` | `pl_pge` | PGE Dystrybucja's 2026 tariff in the URE bulletin, group G11 |
| `vsd-cennik-D-2026.txt` | `sk_vsd` | Východoslovenská distribučná's 2026 price list for households |
| `au-sa-water.json` | `au_sa_water` | SA Water's residential water prices page, 2026-27 |
| `sg-pub-water.json` | `sg_pub_water` | PUB's water price page |

Rules:

- Type only a figure that is on the named document. Never an average and never an estimate.
- A `.json` file names its page, the day it was read (`read_on`) and the day the price is due to
  change (`check_by`). For a `.txt` file the source module in the code repository holds the link and
  those two dates.
- From `check_by` the sync asks for a person and opens an issue, so the next document is read.
- To update a price, read the document again and change the figures and the dates together.
