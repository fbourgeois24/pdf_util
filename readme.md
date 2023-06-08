# pdf_util

```python
pdf = pdf_util.PDF(orientation="P", unit="mm")
# orientation P = portait, L = paysage
pdf.add_page()

pdf.cell(w=0, h=0, txt="Texte", align='C')
# w et h sont spécifiés selon l'unité précisée à l'instansiation de la classe (par défaut mm)
# align défini l'alignement, valeurs possibles: C, 


pdf.create_table(table_data, title='', data_size = 10, title_size=12, align_data='L', align_header='L', cell_width='even', x_start='x_default', \
		emphasize_data=[], emphasize_style=None,emphasize_color=(0,0,0), border=0)
"""
table_data: 
			list of lists with first element being list of headers
title: 
			(Optional) title of table (optional)
data_size: 
			the font size of table data
title_size: 
			the font size fo the title of the table
align_data: 
			align table data
			L = left align
			C = center align
			R = right align
align_header: 
			align table data
			L = left align
			C = center align
			R = right align
cell_width: 
			even: evenly distribute cell/column width
			uneven: base cell size on lenght of cell/column items
			int: int value for width of each cell/column
			list of ints: list equal to number of columns with the widht of each cell / column
x_start: 
			where the left edge of table should start
emphasize_data:  
			which data elements are to be emphasized - pass as list 
			emphasize_style: the font style you want emphaized data to take
			emphasize_color: emphasize color (if other than black) 

"""

pdf.output(filename)
```