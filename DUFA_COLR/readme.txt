In this folder, you will find all the needed files to assign metabarcoding sequence reads of the COI Leray fragment using Ecotag / MJOLNIR_THOR.
This is the list of files you need to download and copy into the taxo dir:

Reference database un COI Leray fragments in fasta format :
- DUFA_COLR_YYYYMMDD.fasta (Current version: 20210723)

Taxonomy database from NCBI with local taxids added with obitaxonomy (Current version:: 20210720):
- taxo_NCBI_YYYYMMDD.adx
- taxo_NCBI_YYYYMMDD.ndx
- taxo_NCBI_YYYYMMDD.rdx
- taxo_NCBI_YYYYMMDD.tdx
- taxo_NCBI_YYYYMMDD.ldx

Tables with higher taxonomic ranks needed by owi_add_taxonomy / MJOLNIR_THOR:
- order_complete.csv
- family_to_order.csv
- genus_to_family.csv

You have to download all files and save them into a folder called (for example) "~/taxo". Then you can launch MJOLNIR_THOR using, for example:
  lib <- "ULOY" 
  cores <- 50
  mjolnir5_THOR(lib,cores,tax_dir="~/taxo",ref_db="DUFA_COLR_20210723.fasta",taxo_db="taxo_NCBI_20210720")
