# ROCmLibs-for-gfx1103-AMD780M-APU

 ROCm Library Files for` gfx1103` also update with more other arch  based  on AMD GPUs for use in Windows and linux 

This repo was created to host ROCm Library files for use in the ZLUDA CUDA Wrapper for AMD GPUs or others for ROCm use.

Make sure download HIP SDK (On windows),ROCm (on Linux) first.

Download` ROCmLibs.zip` and place them into` %HIP_PATH\bin\rocblas\` after renaming the libary folder there to something else (eg "oldlibrary").

Put `rocblas.dll ` under rocblas\library folder (eg,` C:\Program Files\AMD\ROCm\5.7\bin`) replace the origial one 

Rename ` rocblas\library `to something else, like `origlibrary`

Download` rocm gfx1103 phoenixV3.7z` ( original `ROCmLibsgfx1103.zip`)

Open the zip file.

Drag and drop the library folder from` ROCmLibs.zip` into` %HIP_PATH%bin\rocblas` (The folder you opened in step 1).

Reboot PC or not .

Then it should be fine .

Currently , it has test on`ollama, llama.cpp, sd next ( stable diffusion ),stalbe diffusion directml,webui forge amd in zluda way `,its works well . Can be 2-3 times faster than` directml `. also supported on  [LM Studio](https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/wiki/LM-Studio-ROCm-Supported-On-Unsupported-AMD-GPU)

However, gfx 1103 is not official support on ROCm . There maybe have some upredictable clashes or other risks . 

1st edition 

	ROCmLibs-for-gfx1103.v1.7z (gfx1101,gfx1103)

2nd edition 

	rocm gfx1103 phoenix.7z (gfx1101,gfx1103)

3rd edition ,latest with only gfx1103,remove gfx1101
		
	rocm gfx1103 AMD780M phoenix V3.7z (gfx1103)


2nd edition , only for gfx1035
		
	gfx1035 amd680 rembrandt V2.7z ( 2nd edition , only for gfx1035)

gfx803
 
 	rocblas for gfx803 (override with vega10).7z 
 
 gfx902
 
 	rocblas for gfx902.7z

gfx940,gfx941,gfx942

	rocblas for gfx940_ gfx941_ gfx942.7z

gfx90c
 
 	rocblas for gfx90c workable.7z

gfx90c:xnack-
 
 	rocblas for gfx90c:xnack- V2.7z

gfx906
 
 	rocblas for gfx906.7z

gfx1010:xnack-
 
 	rocblas for gfx1010:xnack- with building guide.7z

gfx1012:xnack-
 
 	rocblas for gfx1012:xnack- with building guide.7z


other gpus add for `gfx803、gfx900、gfx1010、gfx1031、gfx1032`

	rocBLAS-HIP5.7.1-win.rar

add more gpu for `gfx1010;gfx1101;gfx1012;gfx1031;gfx1032;gfx1033;gfx1034;gfx1035;gfx1036;gfx1103`( large, over 1.4G)

	rocBLAS-HIP5.7.0-win.7z
add more gpu for `gfx1010;gfx1011;gfx1012;gfx1030;gfx1031;gfx1032;gfx1034;gfx1035;gfx1036;gfx1100;gfx1101;gfx1102;gfx1103`
( 20MB , unzipped up to over 1.65G , recommend if you want to incorporate into an existing rocm project ,if you want add more gpu with the package ,follow the wiki method to add more gpu ,make sure you have at least 64ram otherwise ,it's may easiy crash during the build )

	Rocm rocblas HIP5.7.0.V2.7z
 
 (You'll need to install 7-zip or WinRAR to extract this archive.)


`rocm for Linux available on relesae page (only test on ubutun for ROCm 6.1,for gfx1103,1100)`

Note: Linux version availalbe ,However ,it is not recommended . There easier approach is using HSA_OVERRIDE_GFX_VERSION eg, export HSA_OVERRIDE_GFX_VERSION=11.0.0 overide with support gpu.

For amd780m roblab ,use the phoenix one `.rocm gfx1103 phoenix.7z `or rocm `gfx1103 AMD780M phoenix V3.7z`

Others please seclect base on your amd arch . 

### Note:Don't creat issue on this repo for other reasons. eg, the ollama-for-amd , instead creat an issue over there ,otherwise, it's will creat more complex for us .
