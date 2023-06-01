## Extension

Plain index files structure
```
Extension	Description
.spa		stores document attributes in row-wise mode
.spb		stores blob attributes in row-wise mode: strings, MVA, json
.spc		stores document attributes in columnar mode
.spd		stores matching document ID lists for each word ID
.sph		stores index header information
.sphi		stores histograms of attribute values
.spi		stores word lists (word IDs and pointers to .spd file)
.spk		stores kill-lists
.spl		lock file
.spm		stores a bitmap of killed documents
.spp		stores hit (aka posting, aka word occurrence) lists for each word ID
.spt		stores additional data structures to speed up lookups by document ids
.spe		stores skip-lists to speed up doc-list filtering
.spds		stores document texts
.tmp*		temporary files during index_settings_and_status
.new.sp*	new version of a plain index before rotation
.old.sp*	old version of a plain index after rotation
```
