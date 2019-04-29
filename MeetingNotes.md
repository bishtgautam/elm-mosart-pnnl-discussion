# Apr 29, 2019

- Generation of ELM's surface dataset
  - Tian: 
    - Different compsets have different types of surface datasets. Do we need to support all of the different surface datasets through official E3SM scripts? 
    - MOSART also has different parameter files for different compsets. Do we need to support all of different parameter files through official E3SM scripts?
    
  - Process of adding new surface dataset
    - Generate 16 mapping files via ESMF_RegridWeightGen
    - Generate surface dataset mksurfdata_map

  - What are the new dataset we adding in surface dataset for v2?
    - Irrigation fraction (for ELM irrigation/crop module)
    - Sediment transport model:
      - slope (for sediment transport)
      - Soil gravel content
      - 3 spatially heterogenous parameters
      - Soil depth

  - Should we create a standard method for creating netcdf file for MOSART?
   - River network parameters (resolution specific)
     - Elevation profile (New for V2)
   - Res. parameters (New for V2) (resolution specific)

- Code review process (DID NOT GET TO IT)

- Running tests on Constance (DID NOT GET TO IT)
