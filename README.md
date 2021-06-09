# Fonts

DejaVu fonts can be downloaded [here](https://dejavu-fonts.github.io/).

We need a copy of `DejaVuSansCondensed.ttf` for this process.

## Generate font to add

1. Go to [fpdf.org/makefont](http://www.fpdf.org/makefont)
2. Upload `DejaVuSansCondensed.ttf` and click _Send_.
3. Download `DejaVuSansCondensed.php` and `DejaVuSansCondensed.z`
4. Add these files to the following folder: `fpdf/font` _(you may need to create this folder)_
5. Include the following code to your file:

```python
# OPTION 1: 
# Default Location in the `font` folder in the fpdf package directory
# pdf.add_font('DejaVu', '', 'DejaVuSansCondensed.ttf', uni=True)

# OPTION 2:
# Provide file location (example is MacOS location)
pdf.add_font('DejaVu', '', '/Library/Fonts/DejaVuSansCondensed.ttf', uni=True)

# Set the font
pdf.set_font('DejaVu', '', 14)
```
