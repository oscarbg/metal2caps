### metal2caps

Metal 2 optional features reports of different GPUs (note I also include tesselation support also not a Metal 2 feature)..

These are captured using some lame modifications to a Metal2 Apple sample app so I don't post code right now..

For GPU gens in Apple SOCs I report first Metal supported GPU Apple A7 and also A10X GPU..
interesting would be to check on A11 GPUs which should report improved Metal features at least areRasterOrderGroupsSupported should be 1 here..

I include for desktop reports of GPUs off all the three different existing GPU vendors today..
note perhaps they aren't their last GPU arch incarnations like I have NV Maxwell GPU (not latest Pascal) and Intel HD530 Skylake (not latest KBL/CFL gen9.5 GPUs)..
anyway they are minor revision (graphics features wise) so I don't expect to report improved Metal 2 caps..

Some comments of the report are:

Changing from Apple A7 to A10X don't expose any changes to Metal2 optional caps..

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
 currentAllocatedSize 262144
 maxThreadgroupMemoryLength 16384
````
