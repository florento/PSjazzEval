

## corpus

 50 MusicXML transcriptions of complex tenor sax soli from the Charlie Parker Omnibook

reference: 

> Xavier Riley and Simon Dixon
> Reconstructing the Charlie Parker Omnibook using an audio-to-score automatic transcription pipeline
> SMC 2024

- https://arxiv.org/abs/2405.16687
- https://zenodo.org/records/14362769 (SMC paper)
- https://zenodo.org/records/14628467 (data)



## commands 

see subdirectories



evaluation corpus

```python
eval_Omnibook(tons=165, costtype1=ps.pse.CTYPE_ACCIDtb, tonal1=False, octave1=False, det1=False, global1=100, grid=ps.pse.Grid_Exhaustive, costtype2=ps.pse.CTYPE_ADplus, tonal2=True, octave2=True, det2=False, dflag=True, mflag=True, csflag=2)
```



evaluation 1 opus

```python
eval_Omnibookitem(name='FRfYc', tons=165, costtype1=ps.pse.CTYPE_ACCIDtb, tonal1=False, octave1=False, det1=False, global1=100, grid=ps.pse.Grid_Exhaustive, costtype2=ps.pse.CTYPE_ADplus, tonal2=True, octave2=True, det2=False, dflag=True, mflag=True, csflag=2)
```







