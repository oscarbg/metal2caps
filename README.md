### metal2caps

Metal 2 optional features reports of different GPUs (note I also include tesselation support also not a Metal 2 feature)..

These are captured using some lame modifications to a Metal2 Apple sample app so I don't post code right now..

For GPU gens in Apple SOCs I report first Metal supported GPU Apple A7 and also A10X GPU..</br>
interesting would be to check on A11 GPUs which should report improved Metal features at least areRasterOrderGroupsSupported should be 1 there..

I include for desktop, reports of GPUs off all the three different existing GPU vendors today..</br>
note perhaps they aren't their last GPU arch incarnations as I have NV Maxwell GPU (not latest Pascal) and Intel HD530 Skylake (not latest KBL/CFL gen9.5 GPUs)..</br>
anyway they are minor revision (graphics features wise) so I don't expect these new gens to report improved Metal 2 caps..

Some comments of the report are:

(please note all my comments regarding Apple SOCs are valid up to A10 SOCs)

Changing from Apple A7 to A10X don't expose any changes to Metal2 optional caps..

-**Argument Buffers**: all Apple GPUs support up to Tier1, while all desktop GPUs support up to Tier2..</br>

-**Programmable sample positions** are supported on all Apple GPUs and desktops expect Nvidia GPUs (perhaps Apple native Nvidia driver supports on Kepler?.. altough highly doubt Kepler HW was capable of it)..</br>

-**Read Write Textures** aren't supported on Apple SOCs, discrete desktop GPUs (NV&AMD) support up to Tier1 and Intel IGPUs up to Tier2..</br>

-**Raster Order Groups** are supported right now only on desktop Intel IGPUs (well and A11..) right now..</br>
at WWDC Metal2 sessions was shared Vega GPUs should expose support for it.. although not yet in 10.13.2 betas..</br>
also Nvidia Maxwell HW arch should support it so seems a driver limitation..</br>

-**ThreadgroupMemory** is limited to 16Kbytes on mobile and 32Kbytes on desktop (except Nvidia which exposes up to 48Kbytes)..

**Hoping Nvidia Web driver can get later in the 10.13.x release cycle support for programmable sample positions and raster order groups..**

## Apple GPUs

# Ipad Air 1 (2013) A7 GPU

```
 Tessellation is not supported on this device

 MTLArgumentBuffersTier1
 minimumLinearTextureAlignmentForPixelFormat MTLPixelFormatRGBA8Snorm 64
 
 areProgrammableSamplePositionsSupported 1
  1 samples: 1
 printing sample positions
  sample 0: (0.500000,0.500000)
  2 samples: 1
 printing sample positions
  sample 0: (0.750000,0.750000)
  sample 1: (0.250000,0.250000)
  4 samples: 1
 printing sample positions
  sample 0: (0.375000,0.125000)
  sample 1: (0.875000,0.375000)
  sample 2: (0.125000,0.625000)
  sample 3: (0.625000,0.875000)
  8 samples: 0
 
 removable 0
 MTLReadWriteTextureTierNone
 areRasterOrderGroupsSupported 0
 registryID 4294967735
 maxThreadgroupMemoryLength 16384
````

# Ipad Pro 10.5 (2017) A10X GPU

```
 Tessellation is supported on this device
 MTLArgumentBuffersTier1
 minimumLinearTextureAlignmentForPixelFormat MTLPixelFormatRGBA8Snorm 64
 
 areProgrammableSamplePositionsSupported 1
  1 samples: 1
 printing sample positions
  sample 0: (0.500000,0.500000)
  2 samples: 1
 printing sample positions
  sample 0: (0.750000,0.750000)
  sample 1: (0.250000,0.250000)
  4 samples: 1
 printing sample positions
  sample 0: (0.375000,0.125000)
  sample 1: (0.875000,0.375000)
  sample 2: (0.125000,0.625000)
  sample 3: (0.625000,0.875000)
  8 samples: 0
 
 removable 0
 MTLReadWriteTextureTierNone
 areRasterOrderGroupsSupported 0
 registryID 4294967844
 maxThreadgroupMemoryLength 16384
```  

## Desktop GPUs (on hackintosh 10.13.2 beta 2)


# AMD RX Vega 56

```
 Tessellation is supported on this device
 MTLArgumentBuffersTier2
 minimumLinearTextureAlignmentForPixelFormat MTLPixelFormatRGBA8Snorm 256
 
 areProgrammableSamplePositionsSupported 1
  1 samples: 1
 printing sample positions
  sample 0: (0.500000,0.500000)
  2 samples: 1
 printing sample positions
  sample 0: (0.750000,0.750000)
  sample 1: (0.250000,0.250000)
  4 samples: 1
 printing sample positions
  sample 0: (0.375000,0.125000)
  sample 1: (0.875000,0.375000)
  sample 2: (0.125000,0.625000)
  sample 3: (0.625000,0.875000)
  8 samples: 1
 printing sample positions
  sample 0: (0.562500,0.312500)
  sample 1: (0.437500,0.687500)
  sample 2: (0.812500,0.562500)
  sample 3: (0.312500,0.187500)
  sample 4: (0.187500,0.812500)
  sample 5: (0.062500,0.437500)
  sample 6: (0.687500,0.937500)
  sample 7: (0.937500,0.062500)
 
 removable 0
 MTLReadWriteTextureTier1
 areRasterOrderGroupsSupported 0
 registryID 4294968392
 maxThreadgroupMemoryLength 32768
```

# Nvidia Geforce GTX 970 (Maxwell arch) 

```
Using NV Web driver 378.10.10.10.20.107 patched for 10.13.2..

 Tessellation is supported on this device
 MTLArgumentBuffersTier2
 minimumLinearTextureAlignmentForPixelFormat MTLPixelFormatRGBA8Snorm 256
 
 areProgrammableSamplePositionsSupported 0
  1 samples: 1
 printing sample positions
  sample 0: (0.500000,0.500000)
  2 samples: 1
 printing sample positions
  sample 0: (0.750000,0.750000)
  sample 1: (0.250000,0.250000)
  4 samples: 1
 printing sample positions
  sample 0: (0.375000,0.125000)
  sample 1: (0.875000,0.375000)
  sample 2: (0.125000,0.625000)
  sample 3: (0.625000,0.875000)
  8 samples: 1
 printing sample positions
  sample 0: (0.562500,0.312500)
  sample 1: (0.437500,0.687500)
  sample 2: (0.812500,0.562500)
  sample 3: (0.312500,0.187500)
  sample 4: (0.187500,0.812500)
  sample 5: (0.062500,0.437500)
  sample 6: (0.687500,0.937500)
  sample 7: (0.937500,0.062500)
 
 removable 0
 MTLReadWriteTextureTier1
 areRasterOrderGroupsSupported 0
 registryID 4294968451
 maxThreadgroupMemoryLength 49152
```

# Intel HD Graphics 530 (Skylake GPU gen9)

```
 Tessellation is supported on this device
 MTLArgumentBuffersTier2
 minimumLinearTextureAlignmentForPixelFormat MTLPixelFormatRGBA8Snorm 256
 
 areProgrammableSamplePositionsSupported 1
  1 samples: 1
 printing sample positions
  sample 0: (0.500000,0.500000)
  2 samples: 1
 printing sample positions
  sample 0: (0.750000,0.750000)
  sample 1: (0.250000,0.250000)
  4 samples: 1
 printing sample positions
  sample 0: (0.375000,0.125000)
  sample 1: (0.875000,0.375000)
  sample 2: (0.125000,0.625000)
  sample 3: (0.625000,0.875000)
  8 samples: 1
 printing sample positions
  sample 0: (0.562500,0.312500)
  sample 1: (0.437500,0.687500)
  sample 2: (0.812500,0.562500)
  sample 3: (0.312500,0.187500)
  sample 4: (0.187500,0.812500)
  sample 5: (0.062500,0.437500)
  sample 6: (0.687500,0.937500)
  sample 7: (0.937500,0.062500)
  
 removable 0
 MTLReadWriteTextureTier2
 areRasterOrderGroupsSupported 1
 registryID 4294968485
 maxThreadgroupMemoryLength 32768
```
