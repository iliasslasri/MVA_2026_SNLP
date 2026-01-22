# Evaluation - Group Projects

## Deadlines
A reminder of the deadlines (also available on the main [README](https://github.com/rbawden/MVA_2026_SNLP/blob/main/README.md)):

- [x] 23/01/2026: List of projects released (on this page)
- 30/01/2026: Choice of project topic (first come first served)
- 02/01/2026: Decision on the composition of groups (randomly assigned based on choices)
- 20/02/2026: Deadline for 1-page project report
- 26/03/2026: Deadline for 4-page project report (late submissions will be penalised by 1 point/20 every day)
- Oral presentation (remote): 10-minute presentation + 5 minutes of questions: date TBD

## Evaluation criteria

You will be evaluated on a range of criteria based on your report, presentation and ability to work as a group, including:

- the quality of the written report (in terms of clearly setting out the motivation, describing the method, the results, analyis, critical thinking, etc.)
- the creativity and originality of the work
- the amount of work and depth/soundness of the analyses
- the quality of the oral presentation and the responses to questions

The ability of your group to work together to provide a coherent and cohesive idea for the project will be taken into account. 
I.e. if each member of the project does individual work on the same project such that it does not form a coherent or logical whole, this will
have an impact on the final marks. It is possible to decompose the tasks into individual ones, but there should be logic between them, for example
using the output of one analysis as a basis for a second experiment.

Marks will be assigned individually depending on contributions (i.e. not necessarily the same mark for all members of a group). You will be asked to
list the individual contributions of each member in each of the reports and at the presentation.

## Project topics

1. [**LLM Reasoning for Machine Translation: Synthetic Data Generation over Thinking Tokens (Zebaze et al., 2025)**](https://arxiv.org/abs/2510.11919)

  - Project supervisor: Armel Zebaze - armel.zebaze-dongmo@inria.fr
  - Abstract: Generative Large Language Models (LLMs) can solve a wide range of tasks through in-context (few-shot) learning. In this setting, the model is provided with a small number of input–output examples in its context, followed by a new query, which it solves by inferring and applying the underlying pattern. Machine Translation (MT) is no exception: LLMs can perform few-shot translation accurately and achieve performance close to that of supervised MT systems such as M2M100 or NLLB. Recently, a new class of models has emerged: thinking models. These models are trained to produce explicit reasoning steps before generating an answer. They can be viewed as extending chain-of-thought prompting from an inference-time technique to a training-time objective.
  - Project description: The objective of this project is to familiarize with the Machine Translation task. It involves using language models to perform the Machine Translation task on standard benchmarks (e.g. FLORES-200) and evaluate the outputs using the relevant metrics (e.g. BLEU, chrF++, COMET, MetricX). Multiple setups are expected:
    - How well do base/pretrained LLMs perform few-shot learning depending on the number of in-context examples considered? Focus on small LMs such as gemma-270m-pt, gemma-1b-pt  etc. and explore multiple translation directions and level of resourcedness.
    - What is the behaviour of CoT prompting in MT with base LLMs? Again, use small LMs. You can start your analysis by investigating zero-shot CoT ('Let's think step by step').
    - Do thinking models have better MT performance in general? How differently do they translate with and without thinking?
    - A comprehensive evaluation of multiple scenarios is much appreciated, with a good choice of metrics as well as human evaluation (i.e. manual inspection of the generations by humans to observe high-level differences that metrics fail to catch). Moreover, fine-tuning language models and evaluating them is also expected (this should be possible for small enough LLMs with quantization and PEFT methods, using colab). You can refer to the paper to have an idea of which experiments can be useful, but try to think beyond the paper. Additional and alternative experiences are more than welcome.
  - Relevant resources:
    - [Sacrebleu](https://github.com/mjpost/sacrebleu): standardized evaluation with BLEU and chrF++
    - [MetricX24](https://github.com/google-research/metricx): State-of-the-art metric for evaluating MT, reference-free and reference-based: e.g. [google/metricx-24-hybrid-large-v2p6-bfloat16](https://huggingface.co/google/metricx-24-hybrid-large-v2p6-bfloat16)
    - [COMET](https://github.com/Unbabel/COMET) e.g. [Unbabel/wmt22-comet-da](https://huggingface.co/Unbabel/wmt22-comet-da)
    - [Initial release](https://github.com/ArmelRandy/llm-reasoning-mt)

---

2. [**A Benchmark for Evaluating Machine Translation Metrics on Dialects without Standard Orthography (Aepli et al, 2023)**](https://aclanthology.org/2023.wmt-1.99/)
  - Project supervisor: Oriane Nédey - oriane.nedey@inria.fr
  - Abstract: Among the 7000+ languages spoken worldwide, many are characterized by variation that depends on the geographical location (dialectal variation) and/or social factors (diastratical variation) related to the speakers. Also, these varieties often do not have well-established standards (if at all), including orthographical norms, leading to many possible variants of the same utterance. This paper explores the evaluation of Machine Translation outputs into two Swiss German dialectal varieties by comparing statistical and neural metrics, and by adapting COMET to make it more robust to dialectal variation.
  - Expected:
    - Run evaluations and analyses with existing metrics, including at least one metric not analysed in the paper
    - Propose, motivate, and test a new experiment aimed at increasing robustness to dialectal variation in Machine Translation evaluation
  - Available resources:
    - [Codebase](https://github.com/textshuttle/dialect_eval), including MT evaluation test data: references, human ratings, challenge set
    - MT evaluation training data
      - [RicardoRei/wmt-da-human-evaluation](https://huggingface.co/datasets/RicardoRei/wmt-da-human-evaluation)
      - [RicardoRei/wmt-sqm-human-evaluation](https://huggingface.co/datasets/RicardoRei/wmt-sqm-human-evaluation)
      - [A pretrained model adapted to Swiss German](https://huggingface.co/ZurichNLP/swiss-german-xlm-roberta-base)

---


3. [**TBD**]()
  - Project supervisor: Gabrielle - gabrielle.le-bellier@inria.fr
  - TODO


---

4. [**BERT Has Uncommon Sense: Similarity Ranking for Word Sense BERTology (Gessler and Schneider, 2021)**](https://aclanthology.org/2021.blackboxnlp-1.43/)
   - Project supervisor: Aina - aina.gari-soler@inria.fr
   - Abstract: Words often have multiple meanings, and some are used more frequently than others (e.g., the noun duck typically refers to an animal but it is also a cricket term). This paper introduces a simple method to investigate how well the BERT model captures less common word meanings.
   - Code: [https://github.com/lgessler/bert-has-uncommon-sense/tree/master](https://github.com/lgessler/bert-has-uncommon-sense/tree/master)

---

5. [**ML-SUPERB: Multilingual Speech Universal PERformance Benchmark (Shi et al., 2023)**](https://arxiv.org/abs/2305.10615)
  - Project supervisor: Maxime Poli - maxime.poli@ens.psl.eu
  - Code: [https://github.com/espnet/espnet/tree/master/egs2/ml_superb](https://github.com/espnet/espnet/tree/master/egs2/ml_superb)
  - Abstract: Self-supervised speech representation learning (SSL) is the core component of modern speech processing systems. These models are trained on large quantities of unlabeled speech using a pretext task that enables them to learn contextualized representations. The use of such representations has led to significant improvements in downstream tasks, such as speech recognition, speaker diarization, or emotion recognition. Initially, these models were developed in English only. However, there has been a growing interest in the speech community in applying SSL to multilingual and low-resource settings. The project will consist of using a pretrained SSL model (HuBERT, wav2vec 2.0, etc.), freezing its parameters, and implementing speech recognition with a CTC loss using only 10 minutes / 1h of speech in a low-resource language, following the procedure outlined in ML-SUPERB.
Some ideas for extensions: comparison with other monolingual or multilingual models, comparison of performance between finetuning languages, other tasks (phone recognition, language identification...), other training procedure (LoRA or other PEFT methods as in ML-SUPERB 2.0, etc.), multilingual finetuning vs monolingual finetuning.

---

6. [**Augmentation Invariant Discrete Representation for Generative Spoken Language Modeling (Gat et al., 2023)**](https://aclanthology.org/2023.iwslt-1.46/)

  - Project supervisor: Maxime Poli - maxime.poli@ens.psl.eu
  - Abstract: Generative Spoken Language Modeling research focuses on optimizing speech language models (LMs) using raw speech recordings without any textual supervision. Such speech LMs operate over discrete units obtained from quantizing internal representations of self-supervised models. This paper focuses on improving the robustness of discrete input representations for generative spoken language modeling. The project will consist in reproducing the evaluations of robustness from the paper on selected models and augmentations, implementing the pseudo-labeling algorithm, and training the robust quantizer. It will be evaluated using the ABX metric on the discrete units (not with the zero-shot language modeling tasks: too costly to train the LM).
  - Some ideas for extensions:
    - Introduce new augmentations
    - Evaluation of robustness across languages
    - Comparison with newer speech encoders (SpidR, DinoSR, HuBERT + Spin, mHuBERT-147, XEUS, etc.)

---

7. [**Anti-efficient encoding in emergent communication (Chaabouni et al., 2019)**](https://arxiv.org/abs/1905.12561) and [**LazImpa: Lazy and impatient agents learn to communicate efficiently (Rita et al., 2020)**](https://aclanthology.org/2020.conll-1.26/)
   - Project supervisor: Jean-Baptiste Sevestre - jean-baptiste.sevestre@ens.psl.eu
   - Abstract paper 1: Despite renewed interest in emergent language simulations with neural networks, little is known about the basic properties of the induced code, and how they compare to human language. One fundamental characteristic of the latter, known as Zipf's Law of Abbreviation (ZLA), is that more frequent words are efficiently associated to shorter strings. We study whether the same pattern emerges when two neural networks, a "speaker" and a "listener", are trained to play a signaling game. Surprisingly, we find that networks develop an anti-efficient encoding scheme, in which the most frequent inputs are associated to the longest messages, and messages in general are skewed towards the maximum length threshold. This anti-efficient code appears easier to discriminate for the listener, and, unlike in human communication, the speaker does not impose a contrasting least-effort pressure towards brevity. Indeed, when the cost function includes a penalty for longer messages, the resulting message distribution starts respecting ZLA. Our analysis stresses the importance of studying the basic features of emergent communication in a highly controlled setup, to ensure the latter will not strand too far from human language. Moreover, we present a concrete illustration of how different functional pressures can lead to successful communication codes that lack basic properties of human language, thus highlighting the role such pressures play in the latter.
   - Code for paper 1: [https://github.com/facebookresearch/EGG](https://github.com/facebookresearch/EGG)
   - Abstract paper 2: Previous work has shown that artificial neural agents naturally develop surprisingly non-efficient codes. This is illustrated by the fact that in a referential game involving a speaker and a listener neural networks optimizing accurate transmission over a discrete channel, the emergent messages fail to achieve an optimal length. Furthermore, frequent messages tend to be longer than infrequent ones, a pattern contrary to the Zipf Law of Abbreviation (ZLA) observed in all natural languages. Here, we show that near-optimal and ZLA-compatible messages can emerge, but only if both the speaker and the listener are modified. We hence introduce a new communication system, “LazImpa”, where the speaker is made increasingly lazy, i.e., avoids long messages, and the listener impatient, i.e., seeks to guess the intended content as soon as possible.
   - Code for paper 2: [https://github.com/MathieuRita/Lazimpa](https://github.com/MathieuRita/Lazimpa)     
   - Project description: These papers aim to study how universal properties of human languages (here efficient coding of the transmitted information) can emerge (or not) in simple communicative agents depending on the architecture and inductive biases of these agents. The project aims to reproduce one experiment of one of these two papers and propose, motivate and test a new experiment.
  



