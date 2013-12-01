Excel Formulae
==============

### Number of guests in a row

Count the number of guests in a row based on the number of names or the use of & in the title, e.g. "Mr. & Mrs."

	=COUNTA(D2,G2) + IF(REGEXMATCH(C2, "&"),1,0) + LEN(H2)-LEN(SUBSTITUTE(H2," ",""))
    
- `COUNTA` counts the two name columns
- `IF` statement counts +1 if title contains `&`
- `REGEXMATCH` finds the string "&" in a cell
- `LEN` and `SUBSTITUTE` Count number of words in a cell [*Source: Google Product Forums*](http://productforums.google.com/d/msg/docs/PUkTBR_Bm30/iv-0UC1-DsAJ)

### Total number of invited guests 

	=SUMIF(Addresses!H:H,"Name",Addresses!A:A)
    
"Name" would be a string value from sheet Addresses

### Combine long form names

	=CONCATENATE(Addresses!B10," ", Addresses!C10," ", Addresses!D10," ", Addresses!E10," ", Addresses!F10," ", Addresses!G10)

### Combine Address 1 & 2

	=CONCATENATE(Addresses!H2, " ",Addresses!I2)
	
### Combine City State ZIP

	=CONCATENATE(Addresses!J2, ", ",Addresses!K2, "  ",Addresses!L2)