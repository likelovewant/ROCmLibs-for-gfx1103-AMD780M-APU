### Boost Your AMD GPU Performance with ROCmLibs for gfx1103 and Beyond!

> **This repository initially created to share optimized ROCm Libraries specifically for the AMD 780M APU's gfx1103 architecture (due to limited
official support), It has since grown to include more AMD GPU architectures using the same proven build methods to benefit the community, these libraries are designed to significantly
boost performance in popular applications like AI models (e.g., Llama, Stable Diffusion) within the ZLUDA CUDA Wrapper
and other ROCm-based environments.

> **All code is based on [the ROCm Official Linux version as explained in the
wiki](https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/wiki), with additional tweaks and optimizations
to address this gap in official support.The license may also comply with this if there is any other needs.**

**Here's a simplified guide on how to get started:**

1. **Prerequisites:** Ensure you have the HIP SDK installed for Windows .
2. **Download Files:** Grab the `ROCmLibs-arch titles .zip or 7z` file .For example the ROCmlibs for gfx1103 woud be `rocm gfx1103 AMD780M phoenix V3 for hip sdk 5.7.7z`  (originally
`ROCmLibsgfx1103.zip`) from this repository.
3. **Installation:**
    * Backup. Backup the originally `rocblas.dll` file in `%HIP_PATH%\bin\` and `library` folder in `%HIP_PATH%\bin\rocblas`,
by renaming them (e.g., `rocbals.dll` to `oldrocblas.dll` and `library` to `oldlibrary`). (Backup is only for development purpose otherwise simply delete them).
    * Unzip `ROCmLibs-arch titles.zip or 7z`. Place the extracted `library` folder into `%HIP_PATH%\bin\rocblas`,
and `rocblas.dll` into `%HIP_PATH%\bin\` (example: `C:\Program Files\AMD\ROCm\5.7\bin`). Replace the original files when Windows asks.
   
4. **Reboot(optional):** Restart your computer for the changes to take effect (not a must do).

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

This repository also shares some custom-built ROCm Libraries for various AMD GPU architectures on Windows, including (gfx803; gfx902; gfx90c; gfx90c:xnack-; gfx906; gfx1010; gfx1010:xnack-; gfx1011; gfx1012;
gfx1012:xnack-; gfx1031; gfx1032; gfx1034; gfx1035; gfx1036; gfx1103; gfx1150(experimental only)).

The builded ROCmlibs for the other arches listed above moved to released page .

[Hip SDK 5.7](https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/releases/tag/v0.5.7)

[Hip SDK 6.1.2](https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/releases/tag/v0.6.1.2)

[Hip SDK 6.2.4](https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/releases/tag/v0.6.2.4)

[Hip SDK 6.4.2](https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/releases/tag/v0.6.4.2)

For detailed
instructions on adding support for additional GPUs, please refer to the wiki page.

For more information on using ROCmLibs in LM Studio on unsupported AMD GPUs, visit our dedicated wiki:
[ LM Studio](https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/wiki/Unlock-LM-Studio-on-Any-AMD-GPU-with-ROCm-Guide)




## Additional Information & Installation Tips:

**Extracting Archives:**

You'll need a program like 7-Zip or WinRAR to open the compressed `.zip` and `.7z` files in this repository.


**ROCm for Linux:**

While ROCm is available for Linux on the releases page, **recommend against using it directly**.  There are simpler and more
effective methods for achieving compatibility. The easiest approach is using the `HSA_OVERRIDE_GFX_VERSION`
environment variable. For example, setting `export HSA_OVERRIDE_GFX_VERSION=11.0.0` can override your system's
default and provide support for gfx1103 and similar GPUs.

**ROCm for Windows:**
For the AMD 780M APU on Windows, recommend using one of these files:

* **rocm gfx1103 AMD 780M phoenix V2.0 for hip sdk 5.7.7z:** Compatible with HIP SDK 5.7.1
* **rocm gfx1103 AMD780M phoenix V3 for hip sdk 5.7.7z:**  Compatible with HIP SDK 5.7.1
* **rocm gfx1103 AMD 780M phoenix V4.0 for hip sdk 6.1.2.7z:** Compatible with HIP SDK 6.1.2
* **rocm gfx1103 AMD 780M phoenix V5.0 for hip sdk 6.2.4.7z:** Compatible with HIP SDK 6.2.4
* **rocm gfx1103 for hip sdk 6.4.2.7z:** Compatible with HIP SDK 6.4.2

**Important:**

* Always choose the file version that matches your installed HIP SDK.

 **Selecting the Right ROCm Files:**


Choose the appropriate `.7z` file based on your AMD GPU architecture. Refer to the release page for a complete list of
supported architectures.

> [!IMPORTANT]
> This 7z archive,
>`rocBLAS-Custom-Logic-Files.7z` -for-rx580-vega8-90c-navi10-navi12-navi14-navi22-navi23-navi24-rembrandt-navi26-phoenix-890m(equal to 880m also)-halo52-halo53,
>contains logic files optimized for various AMD GPUs (Rx 580, Vega series, Navi 10-26, Rembrandt, Phoenix).
> To build rocBLAS and utilize these custom logic files, please refer to the detailed guide provided in the
[wiki](https://github.com/likelovewant/ROCmLibs-for-gfx1103-AMD780M-APU/wiki)

**Creating Issues:**


Please refrain from creating issues in this repository for unrelated topics like ollama-for-amd. Maintaining a well-organized project benefits everyone. Therefore, please submit issues related to
ollama-for-amd to the correct repository. This helps keep things clear and streamlined.

Much appreciate your understanding and cooperation!

Let me know if you have any further questions or need assistance with your ROCm setup!
