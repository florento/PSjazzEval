

## corpus

- 48 MusicXML verified transcriptions of basslines 



reference

> X. Riley and S. Dixon. 
> FiloBass: A Dataset and Corpus Based Study of Jazz Basslines
> in *Proc. of the 24th Int. Society for Music Information Retrieval Conf.,* Milan, Italy, 2023.

- https://aim-qmul.github.io/FiloBass/



## commands 

see subdirectories



evaluation corpus

```python
eval_FiloBass(tons=165, costtype1=ps.pse.CTYPE_ACCIDtb, tonal1=False, octave1=False, det1=False, global1=100, grid=ps.pse.Grid_Exhaustive, costtype2=ps.pse.CTYPE_ADplus, tonal2=True, octave2=True, det2=False, dflag=True, mflag=True, csflag=2)
```



evaluation 1 opus

```python
eval_FiloBassitem(name='01-All-the-Things-You-Are', tons=165, costtype1=ps.pse.CTYPE_ACCIDtb, tonal1=False, octave1=False, det1=False, global1=100, grid=ps.pse.Grid_Exhaustive, costtype2=ps.pse.CTYPE_ADplus, tonal2=True, octave2=True, det2=False, dflag=True, mflag=True, csflag=2)
```







