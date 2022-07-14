# Data Vault Standards

## Hubs

A unique list of business keys

### Hub Columns

* Hash Key - Optional Surrogate Key
* Business Key - Required
* Load Date - Optional
* Source System Code - Required

## Links

Two (2) or more Hub primary keys.  A relationship, transaction or a hierarchy.

### Link Columns

* Hash Key - Optional
* Business Keys from contributing hubs (2 or more)
* Load Date - Optional
* Source System Code - Required

## Satellites

Historical record of the descriptive data for a (single) hub or link.

### Satellite Columns

* Surrogate Key - Optional
* Primary key of the related Hub or Link
* Load Date Timestamp (part of the primary key)
* 1 or more descriptive attributes

## Entity Naming Conventions

## Raw DV

| Entity Type | Prefix |
| ----------- | ------ |
| Hub         | HUB    |
| Link        | LNK    |
| Satellite   | SAT    |

## Business DV

| Entity Type        | Prefix |
| ------------------ | ------ |
| Business Hub       | BHUB   |
| Business Link      | BLNK   |
| Business Satellite | BSAT   |

### Special Links

| Entity Type   | Prefix |
| ------------- | ------ |
| Same-As Link  | SAL    |
| Point-in-Time | PIT    |
| Bridge        | BRG    |

### Star

| Entity Type | Prefix |
| ----------- | ------ |
| Fact        | FCT    |
| Dimension   | DIM    |

## Column Naming Conventions

| Attribute Type     | Abbrev     |
| ------------------ | ---------- |
| Source System Code | src_sys_cd |
| Hash Key           | _hk        |
| Load Date          | load_dt    |
| Load Datetime      | load_dttm  |
