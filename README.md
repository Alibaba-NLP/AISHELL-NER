# AISHELL-NER
[ICASSP 2022] AISHELL-NER: Named Entity Recognition from Chinese Speech

## Run Entity-Aware ASR with ESPnet

We conduct the end-to-end entity-aware ASR experiments with [ESPnet](https://github.com/espnet/espnet). First, install ESPnet following the [instruction](https://espnet.github.io/espnet/installation.html). Then move to the `aishell` directory under the `egs2` directory.

```bash
$ cd egs2/aishell/asr1
```

You could download AISHELL-1 through:

```bash
$ ./run.sh --stage 1 --stop-stage 1
```

Otherwise you could mannuly download the dataset at https://www.openslr.org/33/.

Once AISHELL-1 is downloaded and extracted, replace the origin transcription in `downloads/data_aishell/transcript/aishell_transcript_v0.8.txt` by our `aishell_ner_transcript.txt`. Please note the file name should be the same as `aishell_transcript_v0.8.txt`. Another way is to change `aishell_text=path/to/aishell_ner_transcript.txt` in `local/data.sh`.

Then you could run the Conformer entity-aware ASR experiments through:

```bash
$ ./run.sh
```

## Nested Version

You could build a nested version referring to [CNERTA](https://github.com/DianboWork/CNERTA), please note that some annotations may differ.


## Citation

If you find the dataset useful, please consider citing our paper:

```bibtex
@inproceedings{chen2022aishell,
title={AISHELL-NER: Named Entity Recognition from Chinese Speech},
author={Chen, Boli and Xu, Guangwei and Wang, Xiaobin and Xie, Pengjun and Zhang, Meishan and Huang, Fei},
booktitle={2022 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)},
year={2022}
}
```
