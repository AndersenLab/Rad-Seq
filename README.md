Rad-Seq
=======

* __data/__
	* 41188.SNP.WS210.txt - WS210 snp calls in tab-delimited format.
	* WS210.txt - List of WS210 SNP sites.
	* WS245.txt - List of WS245 SNP sites.
	* 41188.WS245.txt.gz - Tabix indexed list of WS245 SNP sites.
* __supporting materials/__ - Contains methods and supplementary methods


cat 41188.SNP.WS210.txt | grep -v 'AB' | cut -f 1 | tr '_' '\t' > WS210.txt && liftover WS210.txt 210 245 1 2 > WS245.txt
bgzip -c WS245.txt > 41188.WS245.txt.gz
tabix -p vcf -f 41188.WS245.txt.gz