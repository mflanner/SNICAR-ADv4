20260612: Updated the diffuse reflectances file (now v2) to fix a bug that slightly affected the diffuse reflectance for upwelling radiation on the ice-air interface.  Also updated the refractive index file (now v2) so that it includes complete data for CO2 ice.  The code for CO2 ice is now fully functional.

# SNICAR-ADv4 

This code uses a two-stream approximation to calculate snow and ice spectral albedo and radiative fluxes at the interfaces of any number of snow or ice layers with distinct properties.

For comprehensive descriptions of the model, please see: 
- Whicker, C. A., Flanner, M. G., Dang, C., Zender, C. S., Cook, J. M., and Gardner, A. S.: SNICAR-ADv4: a physically based radiative transfer model to represent the spectral albedo of glacier ice, The Cryosphere, 16, 1197–1220, https://doi.org/10.5194/tc-16-1197-2022, 2022.
- Flanner, M. G., Arnheim, J. B., Cook, J. M., Dang, C., He, C., Huang, X., Singh, D., Skiles, S. M., Whicker, C. A., and Zender, C. S.: SNICAR-ADv3: a community tool for modeling spectral snow albedo, Geosci. Model Dev., 14, 7673–7704, https://doi.org/10.5194/gmd-14-7673-2021, 2021

Other versions of the model can be found at:
http://snow.engin.umich.edu and https://github.com/mflanner/SNICARv3 

Optical properties needed to run the model are available at: http://snow.engin.umich.edu/opticalprops/snicar_adv4_202606/ 


# To download the model:
1) Download the model (snicarAD_v4.m) and model driver (snicarAD_v4_drv.m)
2) Download one of the following sets of optical properties from the above link:
   - snicar_adv4_OP.tar.gz if you want to run with snow algae. This compressed file is 7.3 GB and contains many thousands of files.
   - snicar_adv4_OP_no_snoalgae.tar.gz if you don't need snow algae. This compressed file is less than 1 GB.
3) Unpack the compressed file, e.g., with "tar xvfz snicar_adv4_OP_no_snoalgae.tar.gz". You should now have a directory titled "snicar_480band"

# To run the model: 
1) In snicarAD_v4.m, set variable "dir_op_root" to the directory where you unpacked the optics library
2) Open snicarAD_v4_drv.m to edit the snow and ice column properties.  Run snicarAD_v4_drv.m
