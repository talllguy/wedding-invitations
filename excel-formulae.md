Excel Formulae
==============


count number of guests in a row based on the number of names or the use of & in the title, e.g. "Mr. & Mrs."
    =COUNTA(D2,G2) +IF(REGEXMATCH(C2, "&"),1,0)
COUNTA counts the two name columns, IF statement counts +1 if title contains `&`

count total number of invited guests in list 
	=SUMIF(Addresses!H:H,"Name",Addresses!A:A)
"Name" would be a string value from sheet Addresses