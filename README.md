[README.md](https://github.com/user-attachments/files/25081716/README.md)
# 🍄 Fungi Spelling Trainer - Setup Instructions

This is a fungi identification spelling trainer for PTI (Professional Tree Inspection) certification.

## 📁 File Structure

```
your-website/
├── index.html           ← Main trainer page
└── tsv/
    └── fungi_data.tsv  ← Fungi database (UPDATE THIS FILE)
```

## 🚀 How to Use

### 1. **Upload to Your Web Server**
   - Upload `index.html` to your web root
   - Upload the `tsv/` folder (with fungi_data.tsv inside) to the same location
   - The structure must be: `index.html` and `tsv/fungi_data.tsv`

### 2. **Update the Fungi Database**
   - Open `tsv/fungi_data.tsv` in a text editor or spreadsheet program
   - Add/edit/remove fungi entries
   - Each row is one fungus
   - Keep the header row (first line) intact

### 3. **TSV File Format**
   The TSV file has these columns (tab-separated):
   - `id` - Unique number
   - `active` - YES or NO (only YES entries will appear)
   - `fungusLatinName` - e.g., "Armillaria mellea"
   - `fungusCommonName` - e.g., "Honey Fungus"  
   - `clueRoots` - Description of root symptoms
   - `clueButt` - Description of butt/base symptoms
   - `clueLowerStem` - Description of lower stem symptoms
   - `clueUpperStem` - Description of upper stem symptoms
   - `clueBranches` - Description of branch symptoms
   - `clueFoliage` - Description of foliage/crown symptoms
   - `whyThisFungus` - Why this diagnosis makes sense
   - `keyDifferentiators` - How to tell it apart from similar fungi
   - `clinicalNotes` - Clinical/practical notes
   - `examTip` - Exam/spelling tips
   - `imageRef` - Reference for image file (optional)

## ✏️ Updating the Data

**Option 1: Edit in Excel/Google Sheets**
1. Open `fungi_data.tsv` in Excel or Google Sheets
2. Make your changes
3. Save/Export as TSV (Tab-Separated Values)
4. Upload the updated file back to your server

**Option 2: Edit in Text Editor**
1. Open `fungi_data.tsv` in a text editor
2. Columns are separated by TAB characters (not spaces)
3. If a field contains commas or special characters, wrap it in quotes: "like this"
4. Save and upload

## 🔄 Adding New Fungi

To add a new fungus, just add a new row to the TSV file:
1. Give it a unique `id` number
2. Set `active` to YES
3. Fill in all the columns with observation data
4. Save the file

The trainer will automatically load the new data!

## ⚙️ Features

- **Spelling Scoring**: Perfect = 10 pts, Near-perfect = 8 pts, Genus only = 4 pts
- **Progress Tracking**: Saves your progress in browser localStorage
- **Detailed Learning**: After each answer, view detailed identification notes
- **Randomized Order**: Fungi appear in random order each session

## 🌐 Browser Compatibility

Works in all modern browsers (Chrome, Firefox, Safari, Edge). Requires JavaScript enabled.

## 📝 Notes

- The TSV file must be at `./tsv/fungi_data.tsv` relative to index.html
- You can have as many or as few fungi as you want
- Set `active` to NO to temporarily disable a fungus without deleting it
- Progress is saved per browser (clearing browser data will reset progress)

## 🐛 Troubleshooting

**"Error Loading Fungi Database"**
- Check that `tsv/fungi_data.tsv` exists in the correct location
- Verify the TSV file format is correct (tabs between columns)
- Check browser console for detailed error messages

**Fungi not appearing**
- Make sure `active` column is set to "YES" (case-sensitive)
- Check there are no blank rows in the TSV file

**Changes not showing up**
- Clear your browser cache and reload
- Check you uploaded the updated TSV file to the correct location

---

Happy studying! 🍄📚
