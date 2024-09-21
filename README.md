### Enhance Your AMD GPU Performance with ROCmLibs for gfx1103 and Beyond!

This repository provides optimized ROCm Library files tailored specifically for AMD GPUs, including the powerful
gfx1103 found in the AMD 780M APU. These libraries are designed to significantly boost performance in popular
applications like AI models (e.g., Llama, Stable Diffusion) within the ZLUDA CUDA Wrapper and other ROCm-based
environments.

**Here's a simplified guide on how to get started:**

1. **Prerequisites:** Ensure you have the HIP SDK installed for Windows or ROCm for Linux.
2. **Download Files:** Grab the `ROCmLibs.zip` file and the `rocm gfx1103 AMD780M phoenix V3 for hip sdk 5.7.7z`  (originally
`ROCmLibsgfx1103.zip`) from this repository.
3. **Installation:**
    * Unzip `ROCmLibs.zip`. Place the extracted library folder into your %HIP_PATH%\bin\rocblas directory,
renaming the existing "rocblas" folder (e.g., to "oldlibrary").
    * Copy the `rocblas.dll` file from the downloaded `ROCmLibs.zip`  into the rocblas\library folder within your
%HIP_PATH%\bin directory (example: C:\Program Files\AMD\ROCm\5.7\bin). Replace the original file.
    * Rename your existing "rocblas\library" folder (e.g., to "origlibrary").
    * Extract the contents of `rocm gfx1103 AMD780M phoenix V3 for hip sdk 5.7.7z` into the same directory where you placed  the ROCmLibs
folder.
4. **Reboot:** Restart your computer for the changes to take effect (not a must do).

**That's it! Your AMD GPU is now ready to harness the power of optimized ROCm libraries.**

**Performance Advantages:**

You can expect significant performance gains, often 2-3 times faster than DirectML, in applications like:

* [ollama](https://github.com/likelovewant/ollama-for-amd)
* [llama.cpp](https://github.com/ggerganov/llama.cpp)
* [SD.Next](https://github.com/vladmandic/automatic/wiki/ZLUDA)
* [Stable Diffusion DirectML](https://github.com/lshqqytiger/stable-diffusion-webui-amdgpu)
* [stable-diffusion-webui-forge-on-amd](https://github.com/likelovewant/stable-diffusion-webui-forge-on-amd)
* [stable-diffusion-webui-amdgpu-forge](https://github.com/lshqqytiger/stable-diffusion-webui-amdgpu-forge)
* [Training Flux LoRA Models with FluxGym, Zluda, and ROCm on Windows](https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/wiki/Training-Flux-LoRA-Models-with-FluxGym,-Zluda,-and-ROCm-on-Windows)
* [ LM Studio](https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/wiki/Unlock-LM-Studio-on-Any-AMD-GPU-with-ROCm-Guide)

 **Support and Resources:**

This repository is actively maintained and supports various AMD GPU architectures for Windows (`gfx803;gfx900;gfx902;gfx90c;gfx90c:xnack-;gfx906;gfx940;gfx941;gfx942;gfx1010;gfx1010:xnack-;gfx1011; gfx1012;gfx1012:xnack-
gfx1030; gfx1031; gfx1032; gfx1034; gfx1035; gfx1036; gfx1100; gfx1101; gfx1102; gfx1103`). 

The builded ROCmlibs for the other arches listed above moved to released page .

[Hip SDK 5.7](https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/releases/tag/v0.5.7)

[Hip SDK 6.1.2](https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/releases/tag/v0.6.1.2)

For detailed
instructions on adding support for additional GPUs, please refer to the wiki page.

For more information on using ROCmLibs in LM Studio on unsupported AMD GPUs, visit our dedicated wiki:
[ LM Studio](https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/wiki/Unlock-LM-Studio-on-Any-AMD-GPU-with-ROCm-Guide)




## Additional Information & Installation Tips:

**Extracting Archives:**

You'll need a program like 7-Zip or WinRAR to open the compressed `.zip` and `.7z` files in this repository.


**ROCm for Linux:**

While ROCm is available for Linux on the releases page, we **recommend against using it directly**.  There are simpler and more
effective methods for achieving compatibility. The easiest approach is using the `HSA_OVERRIDE_GFX_VERSION`
environment variable. For example, setting `export HSA_OVERRIDE_GFX_VERSION=11.0.0` can override your system's
default and provide support for gfx1103 and similar GPUs.

**ROCm for Windows:**
For the AMD 780M APU on Windows, we recommend using one of these files:

* **rocm gfx1103 AMD 780M phoenix V2.0 for hip sdk 5.7.7z:** Compatible with HIP SDK 5.7.1
* **rocm gfx1103 AMD780M phoenix V3 for hip sdk 5.7.7z:**  Compatible with HIP SDK 5.7.1
* **rocm gfx1103 AMD 780M phoenix V4.0 for hip sdk 6.1.2.7z:** Compatible with HIP SDK 6.1.2


**Important:**

* Always choose the file version that matches your installed HIP SDK.

 **Selecting the Right ROCm Files:**


Choose the appropriate `.7z` file based on your AMD GPU architecture. Refer to the release page for a complete list of
supported architectures.



**Creating Issues:**


Please refrain from creating issues in this repository for unrelated topics like ollama-for-amd. If you encounter
problems with those projects, please submit issues directly to the respective repositories. This helps us
maintain a clear and organized workflow.

We appreciate your understanding and cooperation!

Let me know if you have any further questions or need assistance with your ROCm setup!
