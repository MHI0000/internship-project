Internship Project - noise reduction
====================================
Convert audio file
------------------------------------
<p>
  Pydub is a kit in Python that can easily convert an audio file to another type of audio file. 
  In Pydub, there is a tool called AudioSegment that can directly read audio file and export another audio file.
  With the following simple code, the audio conversion can be done.
</p>

```python
  from pydub import AudioSegment
  
  audio=AudioSegment.from_file(input_file)
  audio.export(output_filename, format=output_form)
```

<p>
  If you need to convert an audio in numpy array from to a audio file, you will need another method.
</p>

```python
  from pydub import AudioSegment
  import numpy as np

  audio = AudioSegment(input_array.tobytes(),
                      frame_rate=44100, sample_width=input_array.dtype.itemsize,
                      channels=1 if input_array.ndim == 1 else input_array.shape[1])
  audio.export(output_filename, format=output_form)
```
