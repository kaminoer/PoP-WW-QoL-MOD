# Prince of Persia: Warrior Within Quality-of-Life mod
This mod lets you disable post-processing effects in WW.

# Features
- Blur/bloom disabled by default.
    - Press F12 to toggle blur/bloom.
 - Unlike SoT, there is no overwhelming fog effect in WW. While present, the fog effect is dead code and never runs.
<img width="1720" height="2151" alt="v1.1" src="https://github.com/user-attachments/assets/ab7d5bc0-f643-422a-9c20-dea5e826d46a" />


# Installation
Download [PoP_WW_qol.zip](https://github.com/kaminoer/PoP-WW-QoL-MOD-/releases/download/v1.0/PoP_WW_qol.zip) and unpack its content to your game folder, next to POP2.exe. 
If you notice any other effects disappear when you disable blur/bloom, modify your `maxDim` value in `d3d9.ini`.
Set your blur/bloom remover in the `d3d9.ini` file:
- `mode=skip`: let the mips render normally but drop the final composite quad that blends them back, so brightness is preserved. You can finetune this mode with `compositeMaxTris`
- `mode=black`: clear the bloom render-target mips to black and skip drawing them. WW blends the scene toward the blurred image, which gives it a darker mood.
