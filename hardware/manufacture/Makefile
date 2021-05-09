cat ../reDIP-64.kicad_sch | sed 's/"Mfg"/"Manufacturer"/' | sed 's/"PN"/"PartNumber"/' > reDIP-64-kikit.kicad_sch
kikit fab pcbway --assembly --schematic reDIP-64-kikit.kicad_sch --ignore "JP1,J6,#LOGO1" ../reDIP-64.kicad_pcb .
rm reDIP-64-kikit.sch
sed -Ei 's/(TYPE-C-31-M-12.*),thru-hole,/\1,SMD,/' bom.csv 
sed -Ei 's/\\//' bom.csv 
