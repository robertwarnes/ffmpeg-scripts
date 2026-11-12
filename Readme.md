A collection of FFmpeg Bat Scripts I regularly use:

**BINK (BIK) Files to Quicktime (MOV) with HEVC video codec (bitrate - 50,000kb/s) and loseless PCM audio**

for /f "tokens=1 delims=." %a in ('dir /B *.bik') do ffmpeg -i "%a.bik" -vf scale=3840:2160:flags=lanczos -c:v libx265 -b:v 50000k -c:a pcm_s16le "%a.mov"

**M2V Files to Quicktime (MOV) with HEVC video codec (bitrate - 50,000kb/s) and loseless PCM audio**

for /f "tokens=1 delims=." %a in ('dir /B *.m2v') do ffmpeg -i "%a.m2v" -vf scale=3840:2160:flags=lanczos -c:v libx265 -b:v 50000k -c:a pcm_s16le "%a.mov"

**AC3 Files to WAV (PCM loseless 16 bit)**

for /f "tokens=1 delims=." %a in ('dir /B *.ac3') do ffmpeg -i "%a.ac3" -c:a pcm_s16le "%a.wav"

**BKS Files to WAV (PCM loseless 16 bit)**

for /f "tokens=1 delims=." %a in ('dir /B *.bks') do ffmpeg -i "%a.bks" -c:a pcm_s16le "%a.wav"

**LPCM Files to WAV (PCM loseless 16 bit)**

for /f "tokens=1 delims=." %a in ('dir /B *.lpcm') do ffmpeg -i "%a.lpcm" -c:a pcm_s16le "%a.wav"

**XVAG Files to WAV (PCM loseless 16 bit)**

for /f "tokens=1 delims=." %a in ('dir /B *.xvag') do ffmpeg -i "%a.xvag" -c:a pcm_s16le "%a.wav"




