Internship Project - noise reduction
====================================
Convert audio file
------------------------------------
<p>
  Pydub is a kit in Python that can easily convert an audio file to another type of audio file. 
  In Pydub, there is a tool called AudioSegment that can directly read audio file and export another audio file.
</p>
```python
  from pydub import AudioSegment
  
  audio=AudioSegment.from_file(input_file)
  audio.export(output_file, format=output_form)
```
