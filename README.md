# Sualih Journal

A beautiful animated trade journal for MT5 gold/XAUUSD tracking.

## Quick Setup

1. Open `index.html` in your browser (local file)  
   → https://github.com/Sualih/sualih-journal/raw/main/index.html

2. Or view live: `https://sualih.github.io/sualih-journal/`

---

## How to Use

### Import MT5 Trades
1. In MT5: **Reports → Trade → Export History**
2. Save the `.csv` file
3. Drag it into the page or use the file picker
4. Trades auto-populate in localStorage

### Trades & Stats
- **Balance**: Auto-calculated ($200 start)
- **P&L**: Real-time profit/loss
- **Win Rate**: % of winning trades
- **Profit Factor**: Gross wins / gross losses
- **Profit Curve**: Visual equity line

### Manual Entry (optional)
Open browser console and type:
```js
trades.push({
  time: Date.now(),
  symbol: 'XAUUSD',
  direction: 1,  // 1=Buy, -1=Sell
  open_price: 4400,
  stop_loss: 4385,
  take_profit: 4450,
  size: 1,
  profit: 25,
  notes: 'Entry note'
})
render()
```

---

## GitHub Pages Deployment (Manual)

```bash
# 1. Clone or create repo
git clone https://github.com/your-username/sualih-journal.git
cd sua

lip-journal
git remote set-url origin https://github.com/YOUR-USERNAME/sualih-journal.git
git push -u origin main
```

---

## Customize

Edit `index.html`:
- Line 127: `INITIAL_BALANCE = 200`
- Add your logo in the sidebar
- Change `--accent` color in `:root`

---

## Notes

- Data stored in browser `localStorage`
- Export/Import via JSON button
- Clear all with the trash button

---

MIT License • Made by Sualih