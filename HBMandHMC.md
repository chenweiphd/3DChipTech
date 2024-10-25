
# HBM and HMC

(Modified from Utmel)

## HBM

HBM (High-Bandwidth Memory) is a high-bandwidth memory targeted at the high-end graphics market. HBM uses 3D TSV and 2.5D TSV technologies to stack multiple memory chips together in 3D TSV, and 2.5D TSV technology to interconnect the stacked memory chips with the GPU on the carrier board. The diagram below shows a schematic of HBM technology.

![a515d4d9a8b44181f0c6d04493d7dba1_a1331fe8-974b-467a-b978-2036da5314a3](https://github.com/RIOSMPW/3DChipTech/assets/100336131/ee678f04-0981-485e-83fb-27df7bb13a19)

HBM（High-Bandwidth Memory ）


HBM is vertically stacked DRAM dies connected via Through Silicon Vias (TSVs) and bonded using TCB (hybrid bonding will be required for higher stack counts in the future). Beneath the DRAM dies sits on a base logic die that acts as a controller. Typically, modern HBM has 8 layers of memory and 1 base logic die but we will see products with 12+1 layer HBM soon, for example AMD’s MI300X and Nvidia’s upcoming H100 refresh.

![37dc16bb5d37da00c831a697d1b1198e_https%3A%2F%2Fsubstack-post-media s3 amazonaws com%2Fpublic%2Fimages%2Fb555e9d1-0d98-43a0-bc74-3e41edd02343_895x427](https://github.com/RIOSMPW/3DChipTech/assets/100336131/f71a5d91-a469-4f84-a579-ac7b53c58b41)


HBM is currently available in 4 versions, HBM, HBM2, HBM2E and HBM3, with bandwidths of 128 GBps/Stack, 256 GBps/Stack, and 307 Gbps/Stack respectively.

AMD, NVIDIA, and Hynix are pushing the HBM standard, with AMD first using it for its flagship graphics cards, with memory bandwidths of up to 512 Gbps, and NVIDIA following suit, using HBM to achieve 1TBps of memory bandwidth. Compared to DDR5, HBM improves performance by more than 3 times but reduces power consumption by 50%.

![fccd616a18574b21c82600e5fe341d4e_https%3A%2F%2Fsubstack-post-media s3 amazonaws com%2Fpublic%2Fimages%2Ffbe12301-f937-4b2f-95f0-a9c7f8c2e1d9_3999x2250](https://github.com/RIOSMPW/3DChipTech/assets/100336131/ba95bf48-288f-474d-a7d0-19c71158cc27)


## HMC
HMC (Hybrid Memory Cube) is a hybrid storage cube whose standard is being pushed by Micron. Its target market is the high-end server market, especially for multi-processor architectures. HMC uses stacked DRAM chips to achieve greater memory bandwidth. In addition, HMC integrates the Memory Controller into the DRAM stacked package through 3D TSV integration technology. The diagram below shows the HMC technology.

![00f27f6728d6494b41e4e5038780da3f_5f13c9a0-6466-4151-bdd8-7ca8645bd468](https://github.com/RIOSMPW/3DChipTech/assets/100336131/7a2a2b32-dd61-4634-a0ff-fb7d8e65a326)


HMC

The difference between HBM and HMC is that HBM is interconnected with the GPU through the Interposer, while HMC is mounted directly on the Substrate, missing the Interposer and 2.5D TSV.

In the HMC stack, the 3D TSVs are about 5~6um in diameter and number more than 2000+. DRAM chips are usually thinned to 50um and the chips are connected to each other through a 20um MicroBump.

In the past, memory controllers were made in the processor, so in high-end servers, when a large number of memory modules are needed, the design of memory controllers is very complicated. Now that the memory controller is integrated into the memory module, the design of the memory controller is greatly simplified. In addition, HMC uses a high-speed serial interface (SerDes) to implement a high-speed interface, which is suitable for situations where the processor and memory are far apart.
