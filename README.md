# Digital Skills Hub: website prototype

- `index.html`: the prototype. Arabic-first, with an English switch. It contains the scroll-driven 3D hero, the majlis simulator, WhatsApp booking and the company sections.
- `plan.html`: the creative-direction plan and its revisions.
- `assets/`: textures (`assets/tex`) and 3D models (`assets/m`, glTF saved as `.json`).

## Run it locally

The page loads its 3D files with `fetch`, so it has to be served over http. Double-clicking `index.html` won't load the models. From this folder:

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Put it online

Upload the whole folder, keeping the same structure, to any static host (for example Netlify, Vercel, GitHub Pages or your own server).

The page needs internet access for two things:
- **three.js 0.160.0**, loaded from `cdn.jsdelivr.net`.
- **Fonts**, loaded from Google Fonts: Alexandria and IBM Plex Sans Arabic, both under the SIL Open Font License.

## Settings you may want to change

- **WhatsApp number:** `WA_NUM` in `index.html`. It's currently `966502095291`. The number also appears in the `wa.me` links and the contact section.
- **Example values:** the time, temperatures and prayer times are examples for Riyadh in mid-August. The inside temperature is a rough simulation, not a measurement.
- **Test hook:** `window.__dsh` is a helper used for automated testing. You can delete it before launch.

## Asset credits

All textures and models below come from [Poly Haven](https://polyhaven.com) under **CC0**: free for any use, with no credit required. They're listed here as a courtesy. Textures were colour-graded for this room.

| Asset | Used as | Author(s) |
|---|---|---|
| marble_01 | Floor tiles | Rob Tuytel |
| plastered_wall_04 | Walls and ceiling | Rob Tuytel |
| rough_linen | Sofa fabric (re-coloured) | colormass, Rico Cilliers |
| american_walnut_veneer | Fluted wall, door, panel side (re-coloured) | Jenelle van Heerden |
| beige_wall_001 | Courtyard wall outside | Dimitrios Savva, Rico Cilliers |
| coffee_table_round_01 | Coffee table | Ulan Cabanilla |
| wooden_bowl_02 | Dates bowl | Kuutti Siitonen |
| potted_plant_02 | Corner plant | Rico Cilliers |
| ceramic_vase_01, ceramic_vase_02 | Floor vases | James Ray Cock |
| side_table_tall_01 | Entrance side table | James Ray Cock |
| brass_vase_02 | Brass ewer | Rico Cilliers |
| throw_pillows_01 | Cushion shapes (re-covered in a Sadu-style pattern) | Serhii Khromov |

Everything else was modelled in code for this project: the panel, the sofas, the dallah and finjan cups, the curtains, the wall system, the electrical-board modules, the room and the Sadu-style patterns. The smart panel is unbranded on purpose.
