# LifeFit Gym Planner

**Live:** https://eashari1.github.io/lifefit-gym-planner/

A single-page tool for planning home and commercial gyms. You enter or speak the floor area and the zones you want, and it draws four scaled layout options. It fills each zone with equipment from your catalogue and builds a priced equipment list.

## Updating the site

Edit or replace `index.html` or `equipment.csv` in this repository (Add file → Upload files, or the pencil icon). GitHub Pages republishes automatically within a minute or two.

On the hosted version, voice commands, downloads (PNG, SVG, CSV) and printing all work. Voice needs Chrome, Edge or Safari and microphone permission.

## Your equipment database

- **Easiest:** replace `equipment.csv` in the repository with your own LifeFit list, using the same column headers. The planner loads it automatically every time it opens.
- **From Excel:** open the **Equipment database** tab and choose **Import spreadsheet** (.xlsx, .csv or .json). You can also copy rows from Excel and use **Paste rows**.
- **From Google Sheets:** set sharing to "Anyone with the link", then paste the link into **Load from link**.
- **From your website:** if the site can serve a CSV or JSON file of your products, paste its URL into **Load from link**. The site must allow cross-site access (CORS). If it doesn't, put the file in this repository as `equipment.csv` instead.

Column names don't have to match exactly. The planner recognises common names such as "Product Name", "Category", "Width (mm)" and "MRP", and converts mm, cm, inches or metres to feet.

| Column | Meaning |
|---|---|
| name | Product name (required) |
| short | 2–3 letter label drawn on the plan |
| brand, model, sku | Shown in the equipment list |
| zone | cardio, strength, resistance, plate, functional, bootcamp, crossfit, yoga, group, spin, combat, stretch, pt, kids, reception, lockers, washroom, storage. Separate several with `\|` |
| use | home, commercial or both |
| width_ft / length_ft | Footprint: side-to-side and front-to-back (required) |
| side / front / rear clearance | Free space needed around the machine |
| price | Unit price |
| max_per_zone | Cap on how many go in one zone (blank means no cap) |
| mix_weight | Higher numbers appear more often when a zone is auto-filled |
| keywords | Words to match in voice commands, e.g. "treadmill" |

Treat the sizes and prices in the included `equipment.csv` as sample placeholders and replace them with your real catalogue.

## Voice / typed commands

- `Client name is Mehta Residence`
- `Commercial gym 4000 square feet` · `room 50 by 80`
- `Cardio 800, strength 1000, yoga 400 and boot camp 600`
- `Cardio 25 percent` · `spin 40 square metres`
- `Add 6 treadmills and 4 upright bikes`
- `Remove the spin zone` · `clear all zones` · `suggest zones`
- `Entrance on the left` · `aisle 5 feet` · `spacious spacing`
- `Show layout 2` · `export equipment list` · `print`

Projects save as `.json` files (**Save project / Open project**). The planner also remembers your last project and catalogue in your browser.
