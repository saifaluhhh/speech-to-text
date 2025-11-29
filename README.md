<h1>Speech-to-Text-WaveNet

<h2>End-to-end sentence-level English speech recognition using DeepMind’s WaveNet ideas

A TensorFlow implementation of sentence-level ASR inspired by WaveNet: A Generative Model for Raw Audio.
Prior TensorFlow implementations (e.g., ibab, tomlepaine) focus on raw-audio generation, not ASR. This repo adapts WaveNet-style dilated causal convolutions to an acoustic model trained with CTC.

Key deviations from the paper

Dataset: We train on VCTK instead of TIMIT (free to use).

Features: We use MFCCs (not raw waveform) and remove mean-pooling for downsampling due to compute constraints.

Loss: CTC with sentence-level transcripts (VCTK lacks phoneme labels).

Scope: No external LM / post-processing; no BLEU or LM rescoring due to time limits.
