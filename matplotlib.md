# Matplotlib #

* Remove ticks
```
pl.xticks([], [])
pl.yticks([], [])
```
* Tighten layout
  * ``` pl.tight_layout() ```
* Flip y-axis (useful for plotting spectrograms)
  * ```pl.gca().invert_yaxis()```
* Plot spectrogram
  * ```pl.imshow(spec, interpolation=”nearest”, aspect=”auto”) ```  
