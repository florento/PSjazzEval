# PSjazzEval
Results of evaluation of a Pitch Spelling algorithm on jazz datasets

The algorithm estimates jointly Pitch-Spelling of note, global Key Signature and and local scales.

The code of the algorithms can be found at https://anonymous.4open.science/r/PSE-D30

## Evaluation Datasets

The PS algorithms has been evaluated on 3 datasets:
- 200 lead sheets from the Real Book
- 50 MusicXML transcriptions of complex tenor sax soli from the Charlie Parker Omnibook
  published in https://smcnetwork.org/smc2024/papers/SMC2024_paper_id154.pdf
- 48 MusicXML verified transcriptions of basslines
  published in https://aim-qmul.github.io/FiloBass/

## Evaluation directories

Every evaluation directory contains:

- the score files (`MusicXML`) annotated with 
  - color codes for notes with spelling differences with original (see below for a precise description of colors)
    the original spelling is printed under the staff
  - the estimated local key for each measure
  - the estimated global key at the beginning of the score
- one evaluation table in `cvs` format 
  `.csv` file with 1 row for each score file evaluated

the firectory names have the following form:
```date_PSE_tons_C1_M1o1D1_filter_GRID_C2_M2o2D2```
where
- `tons` number of tonalities for evalution (typically 30 or 165)
- `Ci` = is the cost domain used at step `i`
- `Mi` or Ti = if the computation of the initial state for spelling (modal/tonal) at step `i`
- `oi` (optional) if the best-path-search for spelling cares for octaves or is modulo 12.
- `Di` or `Ei` = wheter the computation of the spell table is deterministic (with chromatic scale) or exhaustive, for the step `i`
- `filter` : % latency wrt best global for the pre-selection of global tons after step 1 
   100 means no selection (use all global for grid and step 2), and is not kept in the dir name
- `GRID`: name of algo for the computation of the grid

## Color code anotations

The notes in the score files  (`MusicXML`) are coloured according to their comparison to the spelling in the ground truth score in the dataset considered.
Both Pitch-Spelling algorithms PSE and PS13b processed in 2 steps: 

1. spelling
2. rewriting of passing notes

The comparison of the spelling result with ground truth after each step determines the color code as follows:

|                              | step 1 | step 2 | color  |
| ---------------------------- | ------ | ------ | ------ |
| comparison with ground truth | $=$    | $=$    | black  |
| comparison with ground truth | $=$    | $\neq$ | violet |
| comparison with ground truth | $\neq$ | $=$    | green  |
| comparison with ground truth | $\neq$ | $\neq$ | red    |

For instance, a green note indicates a spelling that was incorrect after step 1 but has been fixed by step 2 (rewriting), and a red note  indicates a spelling incorrect after step 1 that was not fixed by step 2.

