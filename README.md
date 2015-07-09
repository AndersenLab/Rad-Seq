Rad-Seq
=======

* __data/__
	* 41188SNPset.txt - WS210 snp calls in tab-delimited format.
	* andersen08.ws235.bcf - WS235, lifted over and converted to a bcf format for use with bcftools.
* __supporting materials/__ - Contains methods and supplementary methods


#### 2015-07-09

* Added Allele frequency to vcf files and changed
format to be `.vcf.gz`

	bcftools view andersen08.ws245.bcf | vcffixup - | bcftools view -O z > andersen08.ws245.vcf.gz && bcftools index andersen08.ws245.vcf.gz 
