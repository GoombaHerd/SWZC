# SWZC
Star Wars Zero Company

Engine.ini file for changing engine settings for Star Wars Zero Company

,,,
  I have also uploaded an Engine.ini that was created by AI seperate from this one with comments strictly focused on the performance side of things.
  I have NOT tested these settings yet. If you want to use the "AI-Generated-Engine.ini" you will need to rename it to "Engine.ini"
,,,

Performance changes in Engine.ini (Suggested)

Please edit as neccessary.

Please do not take this as a guarentee to improve performance.

Modified for additional tweaks based on feedback and other testing from myself and the community (special thanks to Vercadi for the original tweak).

You will need to change the 'r.Streaming.PoolSize=12288' to match the VRAM amount for your graphics card. Here are some examples:

; 4 GB → 2048 (RTX 3050, RX 6600)
; 6 GB → 3072 (RTX 3060, RX 6700 XT)
; 8 GB → 5120 (RTX 4070, RTX 3080, RX 7800 XT)
; 12 GB → 9216 (RTX 4080, RTX 3090, RX 7900 XT, RTX 5070)
; 16 GB → 12288 (RTX 4080 Super, RX 7900 XTX, RTX 5080, RTX 5070 Ti)
; 24 GB → 18432 (RTX 4090, RTX 3090 Ti, RTX 5090* partial)
; 32 GB → 24576 (RTX 5090, RTX 6000 Ada)
; 48 GB → 36864 (RTX 6000 Ada, A6000 – pro/workstation)

The following settings decrease performance on lower tier graphics cards that struggle with Ray Tracing or those with less than 8GB of VRAM.

You can make the following changes to the code below:

Find	Replace with
r.Lumen.Reflections.Allow=1	r.Lumen.Reflections.Allow=0
r.Lumen.Reflections.ScreenSpaceReconstruction=1	r.Lumen.Reflections.ScreenSpaceReconstruction=0
r.lumen.Reflections.Temporal=1	r.lumen.Reflections.Temporal=0
r.NGX.DLSS.denoisermode=2	r.NGX.DLSS.denoisermode=0
r.CreateShadersOnLoad=1	r.CreateShadersOnLoad=0
fov=105	fov=90
r.FOV.DistanceScale=1.15	r.FOV.DistanceScale=1.0
