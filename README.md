# ROCmLibs-for-gfx1103-AMD780M-APU

 ROCm Library Files for` gfx1101， gfx1103` based  on AMD GPUs for use in Windows. 

This repo was created to host ROCm Library files for use in the ZLUDA CUDA Wrapper for AMD GPUs
Download` ROCmLibs.zip` and place them into` %HIP_PATH\bin\rocblas\` after renaming the libary folder there to something else (eg "oldlibrary").

Put rocblas.dll  under rocblas\library folder (eg,` C:\Program Files\AMD\ROCm\5.7\bin`) replace the origial one 

Rename library to something else, like origlibrary

Download` rocm gfx1103 phoenixV3.7z` ( original `ROCmLibsgfx1103.zip`)

Open the zip file.

Drag and drop the library folder from` ROCmLibs.zip` into` %HIP_PATH%bin\rocblas` (The folder you opened in step 1).
Reboot PC

Then it should be fine .

Currently , it has test on` sd next ( stable diffusion ),stalbe diffusion directml,webui forge amd `in zluda way,its works well . Can be 2-3 times faster than` directml `.

However, gfx 1103 is not official support on ROCM . There maybe have some upredictable clash or other risk . 

For sd use this 

	git clone https://githubfast.com/lshqqytiger/stable-diffusion-webui-directml.git

or 

	git clone https://github.com/likelovewant/stable-diffusion-webui-forge-on-amd.git

Then cd into the folder run:
		
		webui.bat --use-zluda

Added ROCmLibs_Testing.7z for the following archs

(You'll need to install 7-zip or WinRAR to extract this archive.)

`gfx1101`
`gfx1103 （amd 780m）`
`gfx 1135 (amd 680m)`

For roblab ,use the phoenix one .rocm gfx1103 phoenix.7z
