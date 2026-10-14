# OSS RDTR Zoning MCP (Indonesia)

Connect your AI assistant to [BumiAtlas](https://bumiatlas.com) for Indonesian zoning research through the Model Context Protocol.

This listing is a focused entry point for:

- RDTR (Rencana Detail Tata Ruang) detailed spatial plans, as used by OSS for KKPR checks
- Zone and sub-zone at any coordinate (e.g. R-2 high-density housing, K-1 trade and services)
- Protected vs cultivation zones and the planning hierarchy (planning area, sub-area, block)
- Special provisions: disaster-prone areas, protected food farmland (LP2B), airport safety zones, cultural heritage, TOD and more
- The plan's regional regulation (Perda/Perkada) and a link to it
- Zoned area by zone and sub-zone for a village or regency/city

The MCP connection is provided by BumiAtlas. This repository does not run a separate server. For parcels, HGU, mining and zoning in one connection, use [BumiAtlas MCP](https://github.com/BumiAtlas/bumiatlas-mcp).

## Connect

```
https://bumiatlas.com/mcp/zoning
```

Add it as a custom connector in any MCP client and sign in with Google. More: [bumiatlas.com/mcp-docs](https://bumiatlas.com/mcp-docs).

## Tools

| Tool | Description |
|---|---|
| `Zoning_get` | RDTR zones at a `latitude, longitude` or by zone id: zone and sub-zone codes and names, protected or not, planning hierarchy, special provisions, plan and regulation |
| `Zoning_summary` | Area by zone and sub-zone for a village (BPN code) or regency/city, and the share covered by RDTR plans |
| `Parcel_find_village` | Look up BPN village codes by name |
| `Parcel_search` | Find land parcels at a coordinate, to check the zoning of a specific plot |

## Example prompts

- *"What is the zoning at -8.6705, 115.2126?"*
- *"Can I build a villa here? What zone and sub-zone is this location?"*
- *"Is this land protected food farmland (LP2B) or in a disaster-prone zone?"*
- *"How much of Kota Denpasar is zoned for housing vs trade and services?"*
- *"Which RDTR regulation covers this area?"*

## Data source

RDTR detailed spatial plans published by ATR/BPN (GISTARU / OSS RDTR). Plans cover planning areas, mostly towns and their surroundings; no zone at a place usually means no RDTR plan there, and the regional plan (RTRW) applies.
