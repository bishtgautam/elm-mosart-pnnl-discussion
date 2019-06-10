# Apr 29, 2019

- Generation of ELM's surface dataset
  - Tian: 
    - Different compsets have different types of surface datasets. Do we need to support all of the different surface datasets through official E3SM scripts? 
    - MOSART also has different parameter files for different compsets. Do we need to support all of different parameter files through official E3SM scripts?
    
  - Process of adding new surface dataset
    - Confluence page describing the surface dataset generation is available [here](https://acme-climate.atlassian.net/wiki/spaces/ED/pages/17498263/CLM4.5+dataset+for+year+1850+at+ne120np4+resolution)
    - Generate 16 mapping files via ESMF_RegridWeightGen
    - Generate surface dataset mksurfdata_map

  - What are the new dataset we adding in surface dataset for v2?
    - Irrigation fraction (for ELM irrigation/crop module)
    - Sediment transport model:
      - slope (for sediment transport) -- raw data not available
      - Soil gravel content -- raw data available
      - 3 spatially heterogenous parameters -- raw data not available
      - Soil depth -- raw data available

  - Should we create a standard method for creating netcdf file for MOSART?
   - River network parameters (resolution specific)
     - Elevation profile (New for V2)
   - Res. parameters (New for V2) (resolution specific)

- Code review process (DID NOT GET TO IT)

- Running tests on Constance (DID NOT GET TO IT)

# May 13, 2019

- Code review process:
	- Website: https://acme-climate.atlassian.net/wiki/spaces/ED/pages/29754189/Code+Review+Process+Implementation
	- Zeli: Do we need to have new physics working for a global grid when we issue a new PR?
		- Yes.

- Running tests on Constance (DID NOT GET TO IT)

# June 10, 2019

- V2 PRs
	- Zeli: 
		- Soil erosion transport for ELM
		- Status:
			- Code review started: https://acme-climate.atlassian.net/wiki/spaces/ED/pages/976486494/B1+Soil+Erosion
			- Baseline tests
			- Need to run some global simulation for performance
			- Creating surface datasets to run global
				- Have generated the raw datasets
				- Issue with a netcdf file on NERSC
			- Next step: Run mksurfdata_map on constance instead of Cori.

	- Tian: 
		- 	Water managment for MOSART
			-  Two features:
				-  MOSART-WM 
				-  MOSART-WM 
			-  MOSART-innundation
			-  Code review page created https://acme-climate.atlassian.net/wiki/spaces/ED/pages/981074560/W3+Water+management+and+flood+inundation
			-  Running I-tests
			-  Have a branch

		-  2-way ELM-MOSART coupling for irrigation
			-  Still need to work on this one

	- Hong-Yi: 
		- 	Sediment transport for MOSART
		-  MOSART Heat (more ready)
		-  Did not modify any ELM code
		-  Has not create the code review yet
		-  Work depends more on Tian's branch than Zeli's branch
		-  Will coordinate offline with Tian

	-  Teklu, Micheal:
		-  Atm. downscaling (P, T, othes) for ELM. Code is implemented, but need to test the new code
		-  Working on read/write of new dimension in surface dataset (topo-unit dim.)
		-  Issue: Changing the structure/dim of variables that is being used by other subroutines. How to ensure the changes don't break other code.
		-  One PR will be issued
		-  A code review page needs to be created

	- Yilin 
		- Plant hydraulics
		- Code is ready for PR
		- Code review page: https://acme-climate.atlassian.net/wiki/spaces/ED/pages/976946346/W2+-+Plant+Hydraulics


- Data structure refactor



















