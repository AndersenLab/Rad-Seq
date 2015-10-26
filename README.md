Rad-Seq
=======

* __data/__
	* 41188.SNP.WS220.txt - WS220 snp calls in tab-delimited format.
	* WS220.txt - List of WS220 SNP sites.
	* WS245.txt - List of WS245 SNP sites.
* __supporting materials/__ - Contains methods and supplementary methods


cat 41188.SNP.WS220.txt | grep -v 'AB' | cut -f 1 | tr '_' '\t' > WS220.txt && liftover WS220.txt 220 245 1 2 > WS245.txt 