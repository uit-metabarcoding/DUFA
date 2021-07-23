In this folder, you will find all the needed files to assign taxonomic information to metabarcoding sequence reads of the COI-Leray fragment using Ecotag / MJOLNIR_THOR.

This is the list of files you need to download and copy into your taxo dir:

Reference database of sequences of COI Leray fragments in fasta format :
1.- DUFA_COLR_YYYYMMDD.fasta (Current version: 20210723)

Taxonomy database from NCBI with local taxids added with obitaxonomy (Current version:: 20210720):
2.- taxo_NCBI_YYYYMMDD.adx
3.- taxo_NCBI_YYYYMMDD.ndx
4.- taxo_NCBI_YYYYMMDD.rdx
5.- taxo_NCBI_YYYYMMDD.tdx
6.- taxo_NCBI_YYYYMMDD.ldx

Tables with higher taxonomic ranks needed by owi_add_taxonomy / MJOLNIR_THOR:
7.- order_complete.csv
8.- family_to_order.csv
9.- genus_to_family.csv

Most of these files are too big to be shared in Github. So you can download them from the following Google Drive public folder: 
https://drive.google.com/drive/folders/1gJbY-aUBBnN-2kVpd1J30e-xNz3G2sPf?usp=sharing

You have to download all the files from the Googke Drive folder and save them into a local folder in your server called (for example) "~/taxo". Then you can launch MJOLNIR_THOR from your R script using, for example:
  lib <- "ULOY" 
  cores <- 50
  mjolnir5_THOR(lib,cores,tax_dir="~/taxo",ref_db="DUFA_COLR_20210723.fasta",taxo_db="taxo_NCBI_20210720")
