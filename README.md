# MTN_final-version-data
all the data calculated by phenix version 1.19rc3-4024

e.g. 5UUi 
1. phenix.fetch_pdb 5UUi --mtz 
2. phenix.ready_set 5UUi.pdb   
3. phenix.refine 5UUi.updated.pdb 5UUi.mtz MTN_validate.cif refinement.input.xray_data.r_free_flags.label=R-free-flags(for 2XGA, 5G27 and 6N87: refinement.input.xray_data.r_free_flags.labels="IOBS,SIGIOBS")
4. phenix.pdb_interpretation write_geo=True 5UUi.updated_refine_001.pdb MTN_validate.cif    
5. elbow.refine_geo_display 5UUi.updated_refine_001.pdb.geo "MTN N1" (get MTN structure parameters about N1)
6. phenix.polder 5UUi.pdb 5UUi.mtz solvent_exclusion_mask_selection="chain A and resname MTN and resseq 200" 

