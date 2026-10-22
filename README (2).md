# CBG Plant Process Control Room

An interactive website that walks through converting farm and kitchen waste into compressed biogas (CBG): receiving, sorting, shredding, mixing, anaerobic digestion, desulfurisation, upgrading, compression and digestate separation. A simulator shows how process settings and prices change output, profit and loss.

## Run locally

Open `index.html` in a browser. There is no build step and no dependencies (fonts load from Google Fonts, with system fallbacks).

## Publish on GitHub Pages

1. Push this folder to a repository.
2. Go to Settings, then Pages, choose the `main` branch and the root folder.
3. Your site appears at `https://<username>.github.io/<repository>/`.

## Simulator model (simplified)

- Biogas yield per tonne: dung 30 m³, kitchen waste 85 m³, crop residue 110 m³, scaled by temperature (best at 37 °C), retention time and uptime.
- Methane share 58%, upgraded to 95%, minus methane slip.
- Profit per day = CBG sales + FOM sales - feedstock - running cost - capital charge (15% of net capital a year).
- Optional MNRE support: ₹4 crore per 4,800 kg/day, capped at ₹10 crore.

These are planning estimates. Replace the constants in `calc()` with measured plant data before using results for decisions.

## Ideas to extend

- Add a monthly cash-flow chart and loan schedule.
- Add a live data panel fed by a sensor API.
- Save scenarios and compare them.
