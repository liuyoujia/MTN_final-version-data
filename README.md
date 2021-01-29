# MTN_final-version-data
all the data calculated by phenix version 1.19rc3 

e.g. 5UUi 
phenix.fetch_pdb 5UUi --mtz 
phenix.ready_set 5UUi.pdb   
phenix.refine 5UUi.updated.pdb 5UUi.mtz MTN_validate.cif refinement.input.xray_data.r_free_flags.label=R-free-flags
phenix.pdb_interpretation write_geo=True 5UUi.updated_refine_001.pdb MTN_validate.cif    
elbow.refine_geo_display 5UUi.updated_refine_001.pdb.geo "MTN N1"
phenix.polder 5UUi.pdb 5UUi.mtz solvent_exclusion_mask_selection="chain A and resname MTN and resseq 200" r_free_flags_labels=R-free-flags
