# NS_pocket
Python interface for the pocket detection method of the NanoShaper software **with volume ranking** (not native in NanoShaper)

## Requirements

- A locally installed version of NanoShaper https://gitlab.iit.it/SDecherchi/nanoshaper

OR 


- Install patchelf:

  &nbsp; e.g. sudo apt install patchelf (Ubuntu)
  
  &nbsp; Use the provided NanoShaper executable by running the install_script within *install binaries* folder.
 
If using the first option, make sure to copy NanoShaper executable in the temp folder

## Instructions

Run: python3 NS_pocketVol.py <structureName>.pqr
 
 ### Output
  A "results" folder will be created containing the structure name as a subfolder. 
  In this folder there will be:
  1. \<structureName\>.off file: SES triangulation of the structure as generated by NanoShaper.
  2. p\<number\>.off : Triangulated pocket as generated by NanoShaper.
  3. p\<number\>_atm.pqr: Structure atoms which contact the pocket (a subset of the original provided PQR).
  4. \<structureName\>_infoPockets.txt : Information on the volume of each extracted pocket.
  
  <ins>The pocket number reflects a ranking by volume.</ins>
  
  ### Advanced: 
  Modify the temp/template.prm file for finer control over NanoShaper pocket output
### Attention:
  The structure must be in PQR format
