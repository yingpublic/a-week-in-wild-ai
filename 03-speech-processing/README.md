### Speech processing: recognition, synthesis + Survey on chatbot platforms and API's

------

- [Timeline of speech and voice recognition](https://en.wikipedia.org/wiki/Timeline_of_speech_and_voice_recognition)
- [List of speech recognition software](https://en.wikipedia.org/wiki/List_of_speech_recognition_software)
- [Survey on Chatbot Design Techniques in Speech
Conversation Systems](https://thesai.org/Downloads/Volume6No7/Paper_12-Survey_on_Chatbot_Design_Techniques_in_Speech_Conversation_Systems.pdf)
- [The 2018 State of Chatbots Report: How Chatbots Are Reshaping Online Experiences](https://blog.drift.com/chatbots-report/)
- [Comparison of speech synthesizers](https://en.wikipedia.org/wiki/Comparison_of_speech_synthesizers)


---------------

[Fundamental equation of speech recognition](https://www.inf.ed.ac.uk/teaching/courses/asr/2013-14/asr01-intro.pdf)

![eq](https://github.com/gopala-kr/a-week-in-wild-ai/blob/master/03-speech-processing/eq.JPG)

-------------

Speech signal processing(preprocessing/feature extraction)

- [Audio/Speech Signal Processing](http://home.iitk.ac.in/~nnaik/pdf/PPT_AudioSpeech.pdf)
- [speech-signal-processing](https://www.slideshare.net/lucky43/speech-signal-processing)
- [Research issues in speech processing](https://www.slideshare.net/SabarimalaiManikandan/speech-processing)
- [Digital Signal Processing Overview]()
- [Digital_signal_processing](https://en.wikipedia.org/wiki/Digital_signal_processing)
- [Digital_signal_processor](https://en.wikipedia.org/wiki/Digital_signal_processor)
- [Neurocomputational speech processing](https://en.wikipedia.org/wiki/Neurocomputational_speech_processing)
- [Speech_coding](https://en.wikipedia.org/wiki/Speech_coding)
- [Speech_synthesis](https://en.wikipedia.org/wiki/Speech_synthesis)
- [speechlinks](http://www.speech.cs.cmu.edu/comp.speech/Section3/speechlinks.html)
- [Lecture Notes in Speech Production, Speech Coding, and Speech Recognition](http://www.isle.illinois.edu/~hasegawa/notes/)

------------

Acoustic Modeling


- [Acoustic model](https://en.wikipedia.org/wiki/Acoustic_model)
- [open source acoustic models at VoxForge](http://www.repository.voxforge1.org/downloads/Nightly_Builds/)
- [Computational_linguistics](https://en.wikipedia.org/wiki/Category:Computational_linguistics)
- [Phonetic_algorithms](https://en.wikipedia.org/wiki/Category:Phonetic_algorithms)
- []()
- []()
- []()
- []()







----------

Langauge Modeling

---------

Speech Decoding



--------------

Deep speech(recent state of the arts using DL)


- Deep neural networks for acoustic modeling in speech recognition: The shared views of four research groups [[pdf]](http://cs224d.stanford.edu/papers/maas_paper.pdf)
- Speech recognition with deep recurrent neural networks [[pdf]](http://arxiv.org/pdf/1303.5778.pdf)
- Towards End-To-End Speech Recognition with Recurrent Neural Networks[[pdf]](http://www.jmlr.org/proceedings/papers/v32/graves14.pdf)
- Fast and accurate recurrent neural network acoustic models for speech recognition [[pdf]](http://arxiv.org/pdf/1507.06947)
- Deep speech 2: End-to-end speech recognition in english and mandarin [[pdf]](https://arxiv.org/pdf/1512.02595.pdf) (Baidu Speech Recognition System)
- Achieving Human Parity in Conversational Speech Recognition [[pdf]](https://arxiv.org/pdf/1610.05256v1) 
- [End-to-end Speech Recognition with Recurrent Neural Networks (D3L6 Deep Learning for Speech and Language UPC 2017)](https://www.slideshare.net/xavigiro/endtoend-speech-recognition-with-recurrent-neural-networks-d3l6-deep-learning-for-speech-and-language-upc-2017)
- [Deep Speech and Vision - Xavier Giro-i-Nieto - UPC Barcelona 2018](https://www.slideshare.net/xavigiro/deep-speech-and-vision-xavier-giroinieto-upc-barcelona-2018)
- [[PPT](https://github.com/gopala-kr/summary/blob/master/summaries/Week-1/lec26_audio.pptx)] [[PPT](https://github.com/gopala-kr/summary/blob/master/summaries/Week-1/LiDeng-BerlinOct2015-ASR-GenDisc-4by3.pptx)] [[PPT](https://www.microsoft.com/en-us/research/wp-content/uploads/2017/07/HumansVsMachine-Afeka2017-invited.pdf)]
----------------

> State of the art results on speech recognitions


#### WER

#### LibriSpeech

(Possibly trained on more data than LibriSpeech.)

| WER test-clean | WER test-other | Paper          | Published | Notes   |
| :------------- | :------------- | :------------- | :-------- | :-----: |
| 5.83% | 12.69% | [Deep Speech 2: End-to-End Speech Recognition in English and Mandarin](http://arxiv.org/abs/1512.02595v1) | December 2015 | *Humans* |
| 3.19% | 7.64% | [The CAPIO 2017 Conversational Speech Recognition System](https://arxiv.org/abs/1801.00059) | April 2018 | TDNN + TDNN-LSTM + CNN-bLSTM + Dense TDNN-LSTM across two kinds of trees
| 3.82% | 12.76% | [Improved training of end-to-end attention models for speech recognition](https://www-i6.informatik.rwth-aachen.de/publications/download/1068/Zeyer--2018.pdf) | Interspeech, Sept 2018 | encoder-attention-decoder end-to-end model |
| 4.28% | | [Purely sequence-trained neural networks for ASR based on lattice-free MMI](http://www.danielpovey.com/files/2016_interspeech_mmi.pdf) | September 2016 | HMM-TDNN trained with MMI + data augmentation (speed) + iVectors + 3 regularizations |
| 4.83% | | [A time delay neural network architecture for efficient modeling of long temporal contexts](http://speak.clsp.jhu.edu/uploads/publications/papers/1048_pdf.pdf) | 2015 | HMM-TDNN + iVectors |
| 5.33% | 13.25% | [Deep Speech 2: End-to-End Speech Recognition in English and Mandarin](http://arxiv.org/abs/1512.02595v1) | December 2015 | 9-layer model w/ 2 layers of 2D-invariant convolution & 7 recurrent layers, w/ 100M parameters trained on 11940h |
| 5.51% | 13.97% | [LibriSpeech: an ASR Corpus Based on Public Domain Audio Books](http://www.danielpovey.com/files/2015_icassp_librispeech.pdf) | 2015 | HMM-DNN + pNorm[*](http://www.danielpovey.com/files/2014_icassp_dnn.pdf) |
| 4.8%  | 14.5% | [Letter-Based Speech Recognition with Gated ConvNets](https://arxiv.org/abs/1712.09444) | December 2017 | (Gated) ConvNet for AM going to letters + 4-gram LM |
| 8.01% | 22.49% | same, [Kaldi](http://kaldi-asr.org/) | 2015 | HMM-(SAT)GMM |
| | 12.51% | [Audio Augmentation for Speech Recognition](http://www.danielpovey.com/files/2015_interspeech_augmentation.pdf) | 2015 | TDNN + pNorm + speed up/down speech |

#### WSJ

(Possibly trained on more data than WSJ.)

| WER eval'92    | WER eval'93    | Paper          | Published | Notes   |
| :------------- | :------------- | :------------- | :-------- | :-----: |
| 3.47% | | [Deep Recurrent Neural Networks for Acoustic Modelling](http://arxiv.org/pdf/1504.01482v1.pdf) | April 2015 | TC-DNN-BLSTM-DNN |
| 5.03% | 8.08% | [Deep Speech 2: End-to-End Speech Recognition in English and Mandarin](http://arxiv.org/abs/1512.02595v1) | December 2015 | *Humans* |
| 3.63% | 5.66% | [LibriSpeech: an ASR Corpus Based on Public Domain Audio Books](http://www.danielpovey.com/files/2015_icassp_librispeech.pdf) | 2015 | test-set on open vocabulary (i.e. harder), model = HMM-DNN + pNorm[*](http://www.danielpovey.com/files/2014_icassp_dnn.pdf) |
| 3.60% | 4.98% | [Deep Speech 2: End-to-End Speech Recognition in English and Mandarin](http://arxiv.org/abs/1512.02595v1) | December 2015 | 9-layer model w/ 2 layers of 2D-invariant convolution & 7 recurrent layers, w/ 100M parameters |
| 5.6% | | [Convolutional Neural Networks-based Continuous Speech Recognition using Raw Speech Signal](http://infoscience.epfl.ch/record/203464/files/Palaz_Idiap-RR-18-2014.pdf) | 2014 | CNN over RAW speech (wav) |

#### Hub5'00 Evaluation (Switchboard / CallHome) 

(Possibly trained on more data than SWB, but test set = full Hub5'00.)

| WER (SWB) | WER (CH) | Paper          | Published | Notes   |
| :-------  | :------- | :------------- | :-------- | :-----: |
| 5.0% | 9.1%  | [The CAPIO 2017 Conversational Speech Recognition System](https://arxiv.org/abs/1801.00059) | December 2017 | 2 Dense LSTMs + 3 CNN-bLSTMs across 3 phonesets from [previous Capio paper](https://pdfs.semanticscholar.org/d0ec/cd60d800308cd6e59810769b92b40961c09a.pdf) & AM adaptation using parameter averaging (5.6% SWB / 10.5% CH single systems) |
| 5.1% | 9.9%  | [Language Modeling with Highway LSTM](https://arxiv.org/abs/1709.06436) | September 2017 | HW-LSTM LM trained with Switchboard+Fisher+Gigaword+Broadcast News+Conversations, AM from [previous IBM paper](https://arxiv.org/abs/1703.02136)|
| 5.1% |       | [The Microsoft 2017 Conversational Speech Recognition System](https://arxiv.org/abs/1708.06073) | August 2017 | ~2016 system + character-based dialog session aware (turns of speech) LSTM LM | 
| 5.3% | 10.1% | [Deep Learning-based Telephony Speech Recognition in the Wild](https://pdfs.semanticscholar.org/d0ec/cd60d800308cd6e59810769b92b40961c09a.pdf) | August 2017 | Ensemble of 3 CNN-bLSTM (5.7% SWB / 11.3% CH single systems)
| 5.5% | 10.3% | [English Conversational Telephone Speech Recognition by Humans and Machines](https://arxiv.org/abs/1703.02136) | March 2017 | ResNet + BiLSTMs acoustic model, with 40d FMLLR + i-Vector inputs, trained on SWB+Fisher+CH, n-gram + model-M + LSTM + Strided (à trous) convs-based LM trained on Switchboard+Fisher+Gigaword+Broadcast |
| 6.3% | 11.9% | [The Microsoft 2016 Conversational Speech Recognition System](http://arxiv.org/pdf/1609.03528v1.pdf) | September 2016 | VGG/Resnet/LACE/BiLSTM acoustic model trained on SWB+Fisher+CH, N-gram + RNNLM language model trained on Switchboard+Fisher+Gigaword+Broadcast |
| 6.6% | 12.2% | [The IBM 2016 English Conversational Telephone Speech Recognition System](http://arxiv.org/pdf/1604.08242v2.pdf) | June 2016 | RNN + VGG + LSTM acoustic model trained on SWB+Fisher+CH, N-gram + "model M" + NNLM language model |
| 8.5% | 13% | [Purely sequence-trained neural networks for ASR based on lattice-free MMI](http://www.danielpovey.com/files/2016_interspeech_mmi.pdf) | September 2016 | HMM-BLSTM trained with MMI + data augmentation (speed) + iVectors + 3 regularizations + Fisher |
| 9.2% | 13.3% | [Purely sequence-trained neural networks for ASR based on lattice-free MMI](http://www.danielpovey.com/files/2016_interspeech_mmi.pdf) | September 2016 | HMM-TDNN trained with MMI + data augmentation (speed) + iVectors + 3 regularizations + Fisher (10% / 15.1% respectively trained on SWBD only) |
| 12.6% | 16% | [Deep Speech: Scaling up end-to-end speech recognition](http://arxiv.org/abs/1412.5567) | December 2014 | CNN + Bi-RNN + CTC (speech to letters), 25.9% WER if trained _only_ on SWB |
| 11% | 17.1% | [A time delay neural network architecture for efficient modeling of long temporal contexts](http://speak.clsp.jhu.edu/uploads/publications/papers/1048_pdf.pdf) | 2015 | HMM-TDNN + iVectors |
| 12.6% | 18.4% | [Sequence-discriminative training of deep neural networks](http://www.danielpovey.com/files/2013_interspeech_dnn.pdf) | 2013 | HMM-DNN +sMBR |
| 12.9% | 19.3% | [Audio Augmentation for Speech Recognition](http://www.danielpovey.com/files/2015_interspeech_augmentation.pdf) | 2015 | HMM-TDNN + pNorm + speed up/down speech |
| 15% | 19.1% | [Building DNN Acoustic Models for Large Vocabulary Speech Recognition](http://arxiv.org/abs/1406.7806v2) | June 2014  | DNN + Dropout |
| 10.4% | | [Joint Training of Convolutional and Non-Convolutional Neural Networks](http://www.mirlab.org/conference_papers/International_Conference/ICASSP%202014/papers/p5609-soltau.pdf) | 2014 | CNN on MFSC/fbanks + 1 non-conv layer for FMLLR/I-Vectors concatenated in a DNN |
| 11.5% | | [Deep Convolutional Neural Networks for LVCSR](http://www.cs.toronto.edu/~asamir/papers/icassp13_cnn.pdf) | 2013 | CNN |
| 12.2% | | [Very Deep Multilingual Convolutional Neural Networks for LVCSR](http://arxiv.org/pdf/1509.08967v1.pdf) | September 2015 | Deep CNN (10 conv, 4 FC layers), multi-scale feature maps |
| 11.8% | 25.7% | [Improved training of end-to-end attention models for speech recognition](https://www-i6.informatik.rwth-aachen.de/publications/download/1068/Zeyer--2018.pdf) | Interspeech, Sept 2018 | encoder-attention-decoder end-to-end model, trained on 300h SWB |

#### Rich Transcriptions
| WER RT-02 | WER RT-03 | WER RT-04 | Paper          | Published | Notes   |
| :-------  | :-------- | :-------- | :------------- | :-------- | :-----: |
| 8.1% | 8.0%  |       | [The CAPIO 2017 Conversational Speech Recognition System](https://arxiv.org/abs/1801.00059) | April 2018 | 2 Dense LSTMs + 3 CNN-bLSTMs across 3 phonesets from [previous Capio paper](https://pdfs.semanticscholar.org/d0ec/cd60d800308cd6e59810769b92b40961c09a.pdf) & AM adaptation using parameter averaging  |
| 8.2% | 8.1%  | 7.7%  | [Language Modeling with Highway LSTM](https://arxiv.org/abs/1709.06436) | September 2017 | HW-LSTM LM trained with Switchboard+Fisher+Gigaword+Broadcast News+Conversations, AM from [previous IBM paper](https://arxiv.org/abs/1703.02136)|
| 8.3% | 8.0%  | 7.7%  | [English Conversational Telephone Speech Recognition by Humans and Machines](https://arxiv.org/abs/1703.02136) | March 2017 | ResNet + BiLSTMs acoustic model, with 40d FMLLR + i-Vector inputs, trained on SWB+Fisher+CH, n-gram + model-M + LSTM + Strided (à trous) convs-based LM trained on Switchboard+Fisher+Gigaword+Broadcast |

#### Fisher (RT03S FSH)
| WER     | Paper  | Published | Notes   |
| :------ | :----- | :-------- | :-----: |
| 9.6% | [Purely sequence-trained neural networks for ASR based on lattice-free MMI](http://www.danielpovey.com/files/2016_interspeech_mmi.pdf) | September 2016 | HMM-*BLSTM* trained with MMI + data augmentation (speed) + iVectors + 3 regularizations + SWBD |
| 9.8% | [Purely sequence-trained neural networks for ASR based on lattice-free MMI](http://www.danielpovey.com/files/2016_interspeech_mmi.pdf) | September 2016 | HMM-*TDNN* trained with MMI + data augmentation (speed) + iVectors + 3 regularizations + SWBD |

#### TED-LIUM
| WER Test | Paper          | Published | Notes   |
| :------- | :------------- | :-------- | :-----: |
| 6.5% | [The CAPIO 2017 Conversational Speech Recognition System](https://arxiv.org/abs/1801.00059) | April 2018 | TDNN + TDNN-LSTM + CNN-bLSTM + Dense TDNN-LSTM across two kinds of trees |
| 11.2% | [Purely sequence-trained neural networks for ASR based on lattice-free MMI](http://www.danielpovey.com/files/2016_interspeech_mmi.pdf) | September 2016 | HMM-TDNN trained with LF-MMI + data augmentation (speed perturbation) + iVectors + 3 regularizations |
| 15.3% | [TED-LIUM: an Automatic Speech Recognition dedicated corpus](https://pdfs.semanticscholar.org/1e0b/8416b9d2afb9b1ef87557958ef964cb4472b.pdf) | May 2014 | Multi-layer perceptron (MLP) with bottle-neck feature extraction |

#### CHiME (noisy speech)

| clean | real | sim | Paper | Published | Notes |
| :------ | :----- | :----- | :----- | :----- | :-----: |
| 3.34% | 21.79% | 45.05% | [Deep Speech 2: End-to-End Speech Recognition in English and Mandarin](http://arxiv.org/abs/1512.02595v1) | December 2015 | 9-layer model w/ 2 layers of 2D-invariant convolution & 7 recurrent layers, w/ 68M parameters |
| 6.30% | 67.94% | 80.27% | [Deep Speech: Scaling up end-to-end speech recognition](http://arxiv.org/abs/1412.5567) | December, 2014 |  CNN + Bi-RNN + CTC (speech to letters) |

TODO

#### PER

##### TIMIT

(So far, all results trained on TIMIT and tested on the standard test set.)

| PER     | Paper  | Published | Notes   | 
| :------ | :----- | :-------- | :-----: |
| 16.5%   | [Phone recognition with hierarchical convolutional deep maxout networks](https://link.springer.com/content/pdf/10.1186%2Fs13636-015-0068-3.pdf) | September 2015 | Hierarchical maxout CNN + Dropout |
| 16.5%   | [A Regularization Post Layer: An Additional Way how to Make Deep Neural Networks Robust](https://www.researchgate.net/profile/Jan_Vanek/publication/320038040_A_Regularization_Post_Layer_An_Additional_Way_How_to_Make_Deep_Neural_Networks_Robust/links/59f97fffaca272607e2f804a/A-Regularization-Post-Layer-An-Additional-Way-How-to-Make-Deep-Neural-Networks-Robust.pdf) | 2017 | DBN with last layer regularization |
| 16.7%   | [Combining Time- and Frequency-Domain Convolution in Convolutional Neural Network-Based Phone Recognition](http://www.inf.u-szeged.hu/~tothl/pubs/ICASSP2014.pdf) | 2014 | CNN in time and frequency + dropout, 17.6% w/o dropout |
| 17.3%   | [Segmental Recurrent Neural Networks for End-to-end Speech Recognition](https://arxiv.org/abs/1603.00223) | March 2016 | RNN-CRF on 24(x3) MFSC |
| 17.6%   | [Attention-Based Models for Speech Recognition](http://arxiv.org/abs/1506.07503) | June 2015 | Bi-RNN + Attention |
| 17.7%   | [Speech Recognition with Deep Recurrent Neural Networks](http://arxiv.org/abs/1303.5778v1) | March 2013 | Bi-LSTM + skip connections w/ RNN transducer (18.4% with CTC only) |
| 18.0%   | [Learning Filterbanks from Raw Speech for Phone Recognition](https://arxiv.org/abs/1711.01161) | October 2017 | Complex ConvNets on raw speech w/ mel-fbanks init |
| 18.8%   | [Wavenet: A Generative Model For Raw Audio](https://arxiv.org/pdf/1609.03499.pdf) | September 2016 | Wavenet architecture with mean pooling layer after residual block + few non-causal conv layers |
| 23%     | [Deep Belief Networks for Phone Recognition](http://www.cs.toronto.edu/~asamir/papers/NIPS09.pdf) | 2009 | (first, modern) HMM-DBN |

#### LM
TODO

#### Noise-robust ASR
TODO

#### BigCorp™®-specific dataset
TODO?

#### Lexicon
 * WER: word error rate
 * PER: phone error rate
 * LM: language model
 * HMM: hidden markov model
 * GMM: Gaussian mixture model
 * DNN: deep neural network
 * CNN: convolutional neural network
 * DBN: deep belief network (RBM-based DNN)
 * RNN: recurrent neural network
 * LSTM: long short-term memory
 * CTC: connectionist temporal classification
 * MMI: maximum mutual information (MMI),
 * MPE: minimum phone error 
 * sMBR: state-level minimum Bayes risk
 * SAT: speaker adaptive training
 * MLLR: maximum likelihood linear regression
 * LDA: (in this context) linear discriminant analysis
 * MFCC: [Mel frequency cepstral coefficients](http://snippyhollow.github.io/blog/2014/09/25/classical-speech-recognition-features-in-one-picture/)
 * FB/FBANKS/MFSC: [Mel frequency spectral coefficients](http://snippyhollow.github.io/blog/2014/09/25/classical-speech-recognition-features-in-one-picture/) 
 * VGG: very deep convolutional neural networks from Visual Graphics Group, VGG is an architecture of 2 {3x3 convolutions} followed by 1 pooling, repeated



Source:  [wer_are_we](https://github.com/syhw/wer_are_we/blob/master/README.md), [Are we there yet ?](http://rodrigob.github.io/are_we_there_yet/build/)

-----------------

> Literature reviews:



Automatic Speech Recognition




-------

- **An Introduction to the Application of the Theory of Probabilistic Functions of a Markov Process to Automatic Speech Recognition**(1982), S. E. LEVINSON et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6768244)
- **A Maximum Likelihood Approach to Continuous Speech Recognition**(1983), LALIT R. BAHL et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=4767370&tag=1)
- **Heterogeneous Acoustic Measurements and Multiple Classifiers for Speech Recognition**(1986), Andrew K. Halberstadt. [[pdf]](https://groups.csail.mit.edu/sls/publications/1998/phdthesis-drew.pdf)
- **Maximum Mutual Information Estimation of Hidden Markov Model Parameters for Speech Recognition**(1986), Lalit R. Bahi et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=1169179)
- **A Tutorial on Hidden Markov Models and Selected Applications in Speech Recognition**(1989), Lawrence R Rabiner. [[pdf]](https://pdfs.semanticscholar.org/fb04/6159dfb4a2beb95756fe1116056a6d922565.pdf?\_ga=2.37020706.362861000.1494045851-921183529.1494045851)
- **Phoneme recognition using time-delay neural networks**(1989), Alexander H. Waibel et al. [[pdf]](https://pdfs.semanticscholar.org/b554/da42487697cb0d01a4146858e966c1d2404f.pdf?\_ga=2.97032540.235965811.1494658719-1308334183.1494658711)
- **Speaker-independent phone recognition using hidden Markov models**(1989), Kai-Fu Lee et al. [[pdf]](http://repository.cmu.edu/cgi/viewcontent.cgi?article=2768&context=compsci)
- **Hidden Markov Models for Speech Recognition**(1991), B. H. Juang et al. [[pdf]](http://www.jstor.org/stable/1268779)
- **Connectionist Speech Recognition: A Hybrid Approach**(1994), Herve Bourlard et al. [[pdf]](https://www.researchgate.net/profile/Herve\_Bourlard/publication/230875873\_Connectionist\_Speech\_Recognition\_A\_Hybrid\_Approach/links/0deec5149eb889b8c7000000/Connectionist-Speech-Recognition-A-Hybrid-Approach.pdf)
- **A post-processing system to yield reduced word error rates: Recognizer Output Voting Error Reduction (ROVER)**(1997), J.G. Fiscus. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=659110)
- **Speech recognition with weighted finite-state transducers**(2001), M Mohri et al. [[pdf]](https://cs.nyu.edu/~mohri/pub/hbka.pdf)
- **Review of Tdnn (time Delay Neural Network) Architectures for Speech Recognition**(2014), Masahide Sugiyamat et al. [[pdf]](https://pdfs.semanticscholar.org/073b/6128f04fe4b88b88ae297615af289c308753.pdf?\_ga=2.103860032.1725061846.1494658711-1308334183.1494658711)
- **Framewise phoneme classification with bidirectional LSTM and other neural network architectures**(2005), Alex Graves et al. [[pdf]](https://pdfs.semanticscholar.org/83d6/1d9b71a838aa150d7ef232dc6d4c73e24250.pdf?\_ga=1.187838062.730356906.1493526584)
- **Connectionist temporal classification: labelling unsegmented sequence data with recurrent neural networks**(2006), Alex Graves et al. [[pdf]](https://pdfs.semanticscholar.org/daed/0db4538e1a83b4680545b44e3083843168e7.pdf?\_ga=1.45211874.730356906.1493526584)
- **The kaldi speech recognition toolkit**(2011), Daniel Povey et al. [[pdf]](http://publications.idiap.ch/downloads/reports/2011/Povey\_Idiap-RR-04-2012.pdf)
- **Applying Convolutional Neural Networks concepts to hybrid NN-HMM model for speech recognition**(2012), Ossama Abdel-Hamid et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6288864)
- **Context-Dependent Pre-Trained Deep Neural Networks for Large-Vocabulary Speech Recognition**(2012), George E. Dahl et al. [[pdf]](http://ieeexplore.ieee.org/document/5740583/?part=1)
- **Deep Neural Networks for Acoustic Modeling in Speech Recognition**(2012), Geoffrey Hinton et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6296526)
- **Sequence Transduction with Recurrent Neural Networks**(2012), Alex Graves et al. [[pdf]](https://arxiv.org/pdf/1211.3711.pdf)
- **Deep convolutional neural networks for LVCSR**(2013), Tara N. Sainath et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6639347)
- **Improving deep neural networks for LVCSR using rectified linear units and dropout**(2013), George E. Dahl et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6639346)
- **Improving low-resource CD-DNN-HMM using dropout and multilingual DNN training**(2013), Yajie Miao et al. [[pdf]](https://pdfs.semanticscholar.org/a818/a229c70161d6e46f9861bb5b7d59065d3982.pdf?\_ga=1.187845614.730356906.1493526584)
- **Improvements to deep convolutional neural networks for LVCSR**(2013), Tara N. Sainath et al. [[pdf]](https://pdfs.semanticscholar.org/b299/c8878276d837f9417eb4760ad7b69edb0b58.pdf?\_ga=1.150662000.730356906.1493526584)
- **Machine Learning Paradigms for Speech Recognition: An Overview**(2013), Li Deng et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6423821)
- **Recent advances in deep learning for speech research at Microsoft**(2013), Li Deng et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6639345)
- **Speech recognition with deep recurrent neural networks**(2013), Alex Graves et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6638947)
- **Convolutional deep maxout networks for phone recognition**(2014), László Tóth et al. [[pdf]](https://pdfs.semanticscholar.org/0a24/5098455a6663f922a83d318f7b61d357ab1f.pdf?\_ga=1.218359519.730356906.1493526584)
- **Convolutional Neural Networks for Speech Recognition**(2014), Ossama Abdel-Hamid et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6857341)
- **Combining time- and frequency-domain convolution in convolutional neural network-based phone recognition**(2014), László Tóth. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6853584)
- **Deep Speech: Scaling up end-to-end speech recognition**(2014), Awni Y. Hannun et al. [[pdf]](https://arxiv.org/pdf/1412.5567.pdf)
- **End-to-end Continuous Speech Recognition using Attention-based Recurrent NN: First Results**(2014), Jan Chorowski et al. [[pdf]](https://arxiv.org/pdf/1412.1602.pdf)
- **First-Pass Large Vocabulary Continuous Speech Recognition using Bi-Directional Recurrent DNNs**(2014), Andrew L. Maas et al. [[pdf]](https://arxiv.org/pdf/1408.2873.pdf)
- **Long short-term memory recurrent neural network architectures for large scale acoustic modeling**(2014), Hasim Sak et al. [[pdf]](https://pdfs.semanticscholar.org/c85d/46a94768bdcf7ffcb844b47c5b8e8e8234a3.pdf?\_ga=1.8585459.730356906.1493526584)
- **Robust CNN-based speech recognition with Gabor filter kernels**(2014), Shuo-Yiin Chang et al. [[pdf]](https://pdfs.semanticscholar.org/1d34/0fe19026b0359bde23fcd7299a99a240bd15.pdf?\_ga=1.184683503.730356906.1493526584)
- **Stochastic pooling maxout networks for low-resource speech recognition**(2014), Meng Cai et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6854204)
- **Towards End-to-End Speech Recognition with Recurrent Neural Networks**(2014), Alex Graves et al. [[pdf]](https://pdfs.semanticscholar.org/0fa5/53cfa0cf3cbdf7a913aa2ae789a757dfb32f.pdf?\_ga=1.214035281.730356906.1493526584)
- **A neural transducer**(2015), N Jaitly et al. [[pdf]](https://arxiv.org/abs/1511.04868)
- **Attention-Based Models for Speech Recognition**(2015), Jan Chorowski et al. [[pdf]](https://pdfs.semanticscholar.org/b624/504240fa52ab76167acfe3156150ca01cf3b.pdf?\_ga=1.50080608.730356906.1493526584)
- **Analysis of CNN-based speech recognition system using raw speech as input**(2015), Dimitri Palaz et al. [[pdf]](https://pdfs.semanticscholar.org/31f5/36e48482fc273d521525604606f417638881.pdf?\_ga=1.213722706.730356906.1493526584)
- **Convolutional, Long Short-Term Memory, fully connected Deep Neural Networks**(2015), Tara N. Sainath et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7178838)
- **Deep convolutional neural networks for acoustic modeling in low resource languages**(2015), William Chan et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7178332)
- **Deep Neural Networks for Single-Channel Multi-Talker Speech Recognition**(2015), Chao Weng et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7122291)
- **EESEN: End-to-end speech recognition using deep RNN models and WFST-based decoding**(2015), Y Miao et al. [[pdf]](https://arxiv.org/pdf/1507.08240.pdf)
- **Fast and Accurate Recurrent Neural Network Acoustic Models for Speech Recognition**(2015), Hasim Sak et al. [[pdf]](https://pdfs.semanticscholar.org/9fca/2af9a0e3f2c5c3ed47abb3ebd21b7265ac2b.pdf?\_ga=1.222094174.730356906.1493526584)
- **Lexicon-Free Conversational Speech Recognition with Neural Networks**(2015), Andrew L. Maas et al. [[pdf]](https://pdfs.semanticscholar.org/55ee/875b9039febd378a3f8ac4e3d7603f83d57c.pdf?\_ga=2.128588684.1093285980.1494121465-1276580355.1494121465)
- **Online Sequence Training of Recurrent Neural Networks with Connectionist Temporal Classification**(2015), Kyuyeon Hwang et al. [[pdf]](https://arxiv.org/pdf/1511.06841.pdf)
- **Advances in All-Neural Speech Recognition**(2016), Geoffrey Zweig et al. [[pdf]](https://arxiv.org/pdf/1609.05935.pdf)
- **Advances in Very Deep Convolutional Neural Networks for LVCSR**(2016), Tom Sercu et al. [[pdf]](https://pdfs.semanticscholar.org/76b1/791f2d2776c4d3dd671b7e4f2a9fb3575703.pdf?\_ga=1.150210288.730356906.1493526584)
- **End-to-end attention-based large vocabulary speech recognition**(2016), Dzmitry Bahdanau et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7472618)
- **Deep Convolutional Neural Networks with Layer-Wise Context Expansion and Attention**(2016), Dong Yu et al. [[pdf]](https://pdfs.semanticscholar.org/8926/fa45d9fc76523766a9d65e2c3b4a9c3feb88.pdf?\_ga=1.37888869.730356906.1493526584)
- **Deep Speech 2: End-to-End Speech Recognition in English and Mandarin**(2016), Dario Amodei et al. [[pdf]](https://pdfs.semanticscholar.org/c2ba/9d550bbfb542e9fdd6e817e9be15585d0f47.pdf?\_ga=1.248137409.730356906.1493526584)
- **End-to-end attention-based distant speech recognition with Highway LSTM**(2016), Hassan Taherian. [[pdf]](https://arxiv.org/pdf/1610.05361.pdf)
- **Joint CTC-Attention based End-to-End Speech Recognition using Multi-task Learning**(2016), Suyoun Kim et al. [[pdf]](https://arxiv.org/pdf/1609.06773.pdf)
- **Listen, attend and spell: A neural network for large vocabulary conversational speech recognition**(2016), William Chan et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7472621)
- **Latent Sequence Decompositions**(2016), William Chan et al. [[pdf]](https://arxiv.org/pdf/1610.03035.pdf)
- **Modeling Time-Frequency Patterns with LSTM vs. Convolutional Architectures for LVCSR Tasks**(2016), Tara N. Sainath et al. [[pdf]](https://static.googleusercontent.com/media/research.google.com/zh-CN//pubs/archive/45401.pdf)
- **Recurrent Models for Auditory Attention in Multi-Microphone Distance Speech Recognition**(2016), Suyoun Kim et al. [[pdf]](https://pdfs.semanticscholar.org/b9fc/cd8bee6e6998b87b4efc671dbcee45917282.pdf?\_ga=2.168507874.235965811.1494658719-1308334183.1494658711)
- **Segmental Recurrent Neural Networks for End-to-End Speech Recognition**(2016), Liang Lu et al. [[pdf]](https://pdfs.semanticscholar.org/8477/ec32bc1dde071bed8174348da5cd6740dab0.pdf?\_ga=1.220546782.730356906.1493526584)
- **Towards better decoding and language model integration in sequence to sequence models**(2016), Jan Chorowski et al. [[pdf]](https://arxiv.org/pdf/1612.02695.pdf)
- **Very Deep Convolutional Neural Networks for Noise Robust Speech Recognition**(2016), Yanmin Qian et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7552554)
- **Very Deep Convolutional Networks for End-to-End Speech Recognition**(2016), Yu Zhang et al. [[pdf]](https://arxiv.org/pdf/1610.03022.pdf)
- **Very deep multilingual convolutional neural networks for LVCSR**(2016), Tom Sercu et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7472620)
- **Wav2Letter: an End-to-End ConvNet-based Speech Recognition System**(2016), Ronan Collobert et al. [[pdf]](https://arxiv.org/pdf/1609.03193.pdf)
- **WaveNet: A Generative Model for Raw Audio**(2016), Aäron van den Oord et al. [[pdf]](https://arxiv.org/pdf/1609.03499.pdf)
- **Attentive Convolutional Neural Network based Speech Emotion Recognition: A Study on the Impact of Input Features, Signal Length, and Acted Speech**(2017), Michael Neumann et al. [[pdf]](https://arxiv.org/pdf/1706.00612)
- **An enhanced automatic speech recognition system for Arabic**(2017), Mohamed Amine Menacer et al. [[pdf]](https://pdfs.semanticscholar.org/788e/b75befd9c2597f64e072cb2e86f9e7a877e4.pdf?\_ga=1.188540654.730356906.1493526584)
- **Advances in Joint CTC-Attention based End-to-End Speech Recognition with a Deep CNN Encoder and RNN-LM**(2017), Takaaki Hori et al. [[pdf]](https://arxiv.org/pdf/1706.02737)
- **A network of deep neural networks for distant speech recognition**(2017), Mirco Ravanelli et al. [[pdf]](https://arxiv.org/pdf/1703.08002.pdf)
- **An online sequence-to-sequence model for noisy speech recognition**(2017), Chung-Cheng Chiu et al. [[pdf]](https://arxiv.org/pdf/1706.06428.pdf)
- **An Unsupervised Speaker Clustering Technique based on SOM and I-vectors for Speech Recognition Systems**(2017), Hany Ahmed et al. [[pdf]](https://pdfs.semanticscholar.org/f5be/2cb9d37e5e54c5d20644ff7025cdee14995f.pdf?\_ga=1.185419759.730356906.1493526584)
- **Attention-Based End-to-End Speech Recognition in Mandarin**(2017), C Shan et al. [[pdf]](https://arxiv.org/abs/1707.07167)
- **Building DNN acoustic models for large vocabulary speech recognition**(2017), Andrew L. Maas et al. [[pdf]](https://pdfs.semanticscholar.org/ff7b/9fbbbdc78d874fa93134d643a5a0295f648f.pdf?\_ga=1.242426692.730356906.1493526584)
- **Direct Acoustics-to-Word Models for English Conversational Speech Recognition**(2017), Kartik Audhkhasi et al. [[pdf]](https://arxiv.org/pdf/1703.07754.pdf)
- **Deep Learning for Environmentally Robust Speech Recognition: An Overview of Recent Developments**(2017), Zixing Zhang et al. [[pdf]](https://arxiv.org/pdf/1705.10874)
- **English Conversational Telephone Speech Recognition by Humans and Machines**(2017), George Saon et al. [[pdf]](https://arxiv.org/pdf/1703.02136.pdf)
- **ESE: Efficient Speech Recognition Engine with Sparse LSTM on FPGA**(2017), Song Han et al. [[pdf]](http://dl.acm.org/citation.cfm?id=3021745)
- **Exploring Speech Enhancement with Generative Adversarial Networks for Robust Speech Recognition**(2017), Chris Donahue et al. [[pdf]](https://arxiv.org/pdf/1711.05747)
- **Deep LSTM for Large Vocabulary Continuous Speech Recognition**(2017), Xu Tian et al. [[pdf]](https://arxiv.org/pdf/1703.07090.pdf)
- **Dynamic Layer Normalization for Adaptive Neural Acoustic Modeling in Speech Recognition**(2017), Taesup Kim et al. [[pdf]](https://arxiv.org/pdf/1707.06065v1.pdf)
- **Gram-CTC: Automatic Unit Selection and Target Decomposition for Sequence Labelling**(2017), Hairong Liu et al. [[pdf]](https://arxiv.org/pdf/1703.00096.pdf)
- **Improving the Performance of Online Neural Transducer Models**(2017), Tara N. Sainath et al. [[pdf]](https://arxiv.org/pdf/1712.01807)
- **Learning Filterbanks from Raw Speech for Phone Recognition**(2017), Neil Zeghidour et al. [[pdf]](https://arxiv.org/pdf/1711.01161)
- **Multichannel End-to-end Speech Recognition**(2017), Tsubasa Ochiai et al. [[pdf]](https://arxiv.org/pdf/1703.04783.pdf)
- **Multi-task Learning with CTC and Segmental CRF for Speech Recognition**(2017), Liang Lu et al. [[pdf]](https://arxiv.org/pdf/1702.06378.pdf)
- **Multichannel Signal Processing With Deep Neural Networks for Automatic Speech Recognition**(2017), Tara N. Sainath et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7859320)
- **Multilingual Speech Recognition With A Single End-To-End Model**(2017), Shubham Toshniwal et al. [[pdf]](https://arxiv.org/pdf/1711.01694)
- **Optimizing expected word error rate via sampling for speech recognition**(2017), Matt Shannon. [[pdf]](https://arxiv.org/pdf/1706.02776)
- **Residual Convolutional CTC Networks for Automatic Speech Recognition**(2017), Yisen Wang et al. [[pdf]](https://arxiv.org/pdf/1702.07793.pdf)
- **Residual LSTM: Design of a Deep Recurrent Architecture for Distant Speech Recognition**(2017), Jaeyoung Kim et al. [[pdf]](https://arxiv.org/pdf/1701.03360.pdf)
- **Recurrent Models for Auditory Attention in Multi-Microphone Distance Speech Recognition**(2017), Suyoun Kim et al. [[pdf]](https://pdfs.semanticscholar.org/b9fc/cd8bee6e6998b87b4efc671dbcee45917282.pdf?\_ga=2.162545140.93942331.1493904208-1691509212.1493904208)
- **Reducing Bias in Production Speech Models**(2017), Eric Battenberg et al. [[pdf]](https://arxiv.org/pdf/1705.04400.pdf)
- **Robust Speech Recognition Using Generative Adversarial Networks**(2017), Anuroop Sriram et al. [[pdf]](https://arxiv.org/pdf/1711.01567)
- **State-of-the-art Speech Recognition With Sequence-to-Sequence Models**(2017), Chung-Cheng Chiu et al. [[pdf]](https://arxiv.org/pdf/1712.01769)
- **Towards Language-Universal End-to-End Speech Recognition**(2017), Suyoun Kim et al. [[pdf]](https://arxiv.org/pdf/1711.02207)
- **Accelerating recurrent neural network language model based online speech recognition system**(2018), K Lee et al. [[pdf]](https://arxiv.org/pdf/1801.09866)


Speaker Verification

- **Speaker Verification Using Adapted Gaussian Mixture Models**(2000), Douglas A.Reynolds et al. [[pdf]](http://www.sciencedirect.com/science/article/pii/S1051200499903615#)
- **A tutorial on text-independent speaker verification**(2004), Frédéric Bimbot et al. [[pdf]](https://dl.acm.org/ft\_gateway.cfm?id=1289376&ftid=464492&dwn=1&CFID=843437542&CFTOKEN=31448020)
- **Deep neural networks for small footprint text-dependent speaker verification**(2014), E Variani et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6854363)
- **Deep Speaker Vectors for Semi Text-independent Speaker Verification**(2015), Lantian Li et al. [[pdf]](https://arxiv.org/pdf/1505.06427)
- **Deep Speaker: an End-to-End Neural Speaker Embedding System**(2017), Chao Li et al. [[pdf]](https://arxiv.org/pdf/1705.02304.pdf)
- **Deep Speaker Feature Learning for Text-independent Speaker Verification**(2017), Lantian Li et al. [[pdf]](https://arxiv.org/pdf/1705.03670)
- **Deep Speaker Verification: Do We Need End to End?**(2017), Dong Wang et al. [[pdf]](https://arxiv.org/pdf/1706.07859)
- **Speaker Diarization with LSTM**(2017), Quan Wang et al. [[pdf]](https://arxiv.org/pdf/1710.10468)
- **Text-Independent Speaker Verification Using 3D Convolutional Neural Networks**(2017), Amirsina Torfi et al. [[pdf]](https://arxiv.org/pdf/1705.09422)


Speech Synthesis

- **Signal estimation from modified short-time Fourier transform**(1993), Daniel W. Griffin et al. [[pdf]](https://pdfs.semanticscholar.org/ade8/d1511a61d78948bb0d43e207593389935421.pdf?\_ga=2.229355228.1725061846.1494658711-1308334183.1494658711)
- **Text-to-speech synthesis**(2009), Paul Taylor et al. [[pdf]](https://books.google.com/books?hl=zh-CN&lr=&id=BFnkm-FpBAUC&oi=fnd&pg=PR9&dq=Text-to-Speech+Synthesis&ots=ucm6pVQ0bW&sig=1ZoIFILLQLbdHtJu0MlLHkmPnqE#v=onepage&q=Text-to-Speech%20Synthesis&f=false)
- **A fast Griffin-Lim algorithm**(2013), Nathanael Perraudin et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=6701851)
- **First Step Towards End-to-End Parametric TTS Synthesis: Generating Spectral Parameters with Neural Attention**(2016), Wenfu Wang et al. [[pdf]](http://doi.org/10.21437/Interspeech.2016-134)
- **Recent Advances in Google Real-Time HMM-Driven Unit Selection Synthesizer**(2016), Xavi Gonzalvo et al. [[pdf]](http://doi.org/10.21437/Interspeech.2016-264)
- **SampleRNN: An Unconditional End-to-End Neural Audio Generation Model**(2016), Soroush Mehri et al. [[pdf]](https://arxiv.org/pdf/1612.07837.pdf)
- **WaveNet: A Generative Model for Raw Audio**(2016), Aäron van den Oord et al. [[pdf]](https://arxiv.org/pdf/1609.03499.pdf)
- **Char2Wav: End-to-end speech synthesis**(2017), J Sotelo et al. [[pdf]](https://openreview.net/forum?id=B1VWyySKx)
- **Deep Voice: Real-time Neural Text-to-Speech**(2017), Sercan O. Arik et al. [[pdf]](https://arxiv.org/pdf/1702.07825.pdf)
- **Deep Voice 2: Multi-Speaker Neural Text-to-Speech**(2017), Sercan Arik et al. [[pdf]](https://arxiv.org/pdf/1705.08947)
- **Deep Voice 3: 2000-Speaker Neural Text-to-speech**(2017), Wei Ping et al. [[pdf]](https://arxiv.org/pdf/1710.07654)
- **Natural TTS Synthesis by Conditioning WaveNet on Mel Spectrogram Predictions**(2017), Jonathan Shen et al. [[pdf]](https://arxiv.org/pdf/1712.05884)

- **Parallel WaveNet: Fast High-Fidelity Speech Synthesis**(2017), Aaron van den Oord et al. [[pdf]](https://arxiv.org/pdf/1711.10433)
- **Statistical Parametric Speech Synthesis Using Generative Adversarial Networks Under A Multi-task Learning Framework**(2017), S Yang et al. [[pdf]](https://arxiv.org/pdf/1707.01670)
- **Tacotron: Towards End-to-End Speech Synthesis**(2017), Yuxuan Wang et al. [[pdf]](https://pdfs.semanticscholar.org/a072/c2a400f62f720b68dc54a662fb1ae115bf06.pdf?\_ga=2.133718478.1725061846.1494658711-1308334183.1494658711)
- **Uncovering Latent Style Factors for Expressive Speech Synthesis**(2017), Yuxuan Wang et al. [[pdf]](https://arxiv.org/pdf/1711.00520)
- **VoiceLoop: Voice Fitting and Synthesis via a Phonological Loop**(2017), Yaniv Taigman et al. [[pdf]](https://arxiv.org/pdf/1707.06588)
- **Natural TTS Synthesis by Conditioning WaveNet on Mel Spectrogram Predictions**(2017), Jonathan Shen et al. [[pdf]](https://arxiv.org/pdf/1712.05884)
- **Neural Voice Cloning with a Few Samples**(2018), Sercan O. Arık ,  Jitong Chen , 1 Kainan Peng , Wei Ping *  et al. [[pdf]](https://arxiv.org/pdf/1802.06006.pdf)


Language Modelling

- **Class-Based n-gram Models of Natural Language**(1992), Peter F. Brown et al. [[pdf]](https://pdfs.semanticscholar.org/ce84/cf6160ab221d5ee67afad046d2b89560749d.pdf?\_ga=2.197138663.999867306.1494660639-1308334183.1494658711)
- **An empirical study of smoothing techniques for language modeling**(1996), Stanley F. Chen et al. [[pdf]](https://dl.acm.org/ft\_gateway.cfm?id=981904&ftid=567802&dwn=1&CFID=843437542&CFTOKEN=31448020)
- **A Neural Probabilistic Language Model**(2000), Yoshua Bengio et al. [[pdf]](https://pdfs.semanticscholar.org/8d43/4a90b68fd0f2592d6fe7acf67d232123ad67.pdf?\_ga=2.262836293.895163446.1494660654-1308334183.1494658711)
- **A new statistical approach to Chinese Pinyin input**(2000), Zheng Chen et al. [[pdf]](https://dl.acm.org/ft\_gateway.cfm?id=1075249&ftid=261667&dwn=1&CFID=843437542&CFTOKEN=31448020)
- **Discriminative n-gram language modeling**(2007), Brian Roark et al. [[pdf]](https://pdfs.semanticscholar.org/b258/5b3cdcb81db887f756b8f90fd0e04f9ef952.pdf?\_ga=2.103398592.1137797782.1494660710-1308334183.1494658711)
- **Neural Network Language Model for Chinese Pinyin Input Method Engine**(2015), S Chen et al. [[pdf]](https://pdfs.semanticscholar.org/1294/f49cf1a7397f0423ec617a78c7995139bc5b.pdf)
- **Efficient Training and Evaluation of Recurrent Neural Network Language Models for Automatic Speech Recognition**(2016), Xie Chen et al. [[pdf]](http://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=7533441)
- **Exploring the limits of language modeling**(2016), R Jozefowicz et al. [[pdf]](https://arxiv.org/pdf/1602.02410)
- **On the State of the Art of Evaluation in Neural Language Models**(2016), G Melis et al. [[pdf]](https://arxiv.org/pdf/1707.05589)



------------------


- [Intelligence Quotient and Intelligence Grade of Artificial Intelligence](https://arxiv.org/abs/1709.10242)
- [What Is The Difference Between Siri And Viv?](https://www.forbes.com/sites/quora/2016/05/27/what-is-the-difference-between-siri-and-viv/#230a8fdf5b49)
- [How Siri Works – Interview with Tom Gruber, CTO of SIRI](http://www.novaspivack.com/technology/how-hisiri-works-interview-with-tom-gruber-cto-of-siri)
- [How Siri Works: Siri-A-Primer](http://www.venturewerks.com/Siri-A-Primer.pdf)
- [How Siri Works (jeffwofford.com)](https://news.ycombinator.com/item?id=3111133)
- [CHATBOT ASSISTING: SIRI](http://www.technicaljournalsonline.com/ijaers/VOL%20IV/IJAERS%20VOL%20IV%20ISSUE%20II%20JANUARY%20MARCH%202015/562.pdf)
- [Apple: Deep Learning for Siri’s Voice: On-device Deep Mixture Density Networks for Hybrid Unit Selection Synthesis](https://machinelearning.apple.com/2017/08/06/siri-voices.html)
- [Apple has designed a new Siri Architecture allowing Two Digital Assistants to Communicate with Each Other](http://www.patentlyapple.com/patently-apple/2017/05/apple-has-designed-a-new-siri-architecture-allowing-two-digital-assistants-to-communicate-with-each-other.html)

----------------
---------------

Appendix: Reference images

--------

Evolution of Search 


![cognitivesearch](https://marionoioso.com/wp-content/uploads/2018/06/cognitivesearch-768x414.jpg)

![1496154841914](https://static1.squarespace.com/static/56e9401ef8baf3149e959bb3/t/592d82cf86e6c0040d66a212/1496154841914/?format=750w)

------

Architecture of ASR:


![0*-fsj14f4eQo2EZEI](https://cdn-images-1.medium.com/max/1600/0*-fsj14f4eQo2EZEI.)

-----------

![1-s2.0-S0167639313000988-gr2](https://www.researchgate.net/profile/Alexey_Karpov2/publication/259118437/figure/fig1/AS:297010319118352@1447824186627/Architecture-of-a-state-of-the-art-automatic-speech-recognition-system-and-its-components.png)

-------------

The holy grail of ASR

![nJNxFmJaHxyJTtVFkhGTlg](https://cdn-images-1.medium.com/max/880/1*nJNxFmJaHxyJTtVFkhGTlg.png)

-----------

Example App flow:

![diagram-of-speech-recognition](https://www.researchgate.net/profile/Hae-Duck_Jeong/publication/287429405/figure/fig2/AS:310678364672001@1451082902257/Data-flow-diagram-of-speech-recognition.png)

-----------

QA flow:

![1280px-DeepQA.svg.png](https://upload.wikimedia.org/wikipedia/commons/thumb/4/41/DeepQA.svg/1280px-DeepQA.svg.png?1532246161874)

-----------

<a href="https://www.researchgate.net/Architecture-to-develop-user-adapted-spoken-conversational-agents_fig3_288480562"><img src="https://www.researchgate.net/publication/288480562/figure/fig3/AS:329780403687425@1455637183466/Architecture-to-develop-user-adapted-spoken-conversational-agents.png" alt="Architecture to develop user-adapted spoken conversational agents."/></a>

--------------

IBM Watson(DeepQA) :

![DeepQA-Arch](https://researcher.watson.ibm.com/researcher/files/us-mike.barborak/DeepQA-Arch.PNG)


--------------

Alexa/Echo:


![alexa_skills_kit_architecture_diagram](https://3lhowb48prep40031529g5yj-wpengine.netdna-ssl.com/wp-content/uploads/2016/08/alexa_skills_kit_architecture_diagram.png)

![Ms9HNob9HyWcWkbk](https://cdn-images-1.medium.com/max/880/0*Ms9HNob9HyWcWkbk.png)

- [Build an Alexa Skill with Python and AWS Lambda](https://moduscreate.com/blog/build-an-alexa-skill-with-python-and-aws-lambda/)

--------

Google speech services:

![HBp13IJewSkrPZhb](https://cdn-images-1.medium.com/max/880/0*HBp13IJewSkrPZhb.png)


--------------

Google assistant(Actions workflow)

![action_sdk_workflow](https://www.grokkingandroid.com/wordpress/wp-content/uploads/2017/10/action_sdk_workflow.png)

- [Using the Actions SDK for Google Assistant Development](https://dzone.com/articles/using-the-actions-sdk-for-google-assistant-develop)

------

![google-action-request](https://www.jovo.tech/blog/wp-content/uploads/2017/08/google-action-request.png)

[[Tutorial] Build a Google Action in Node.js with Jovo](https://www.jovo.tech/blog/google-action-tutorial-nodejs/)

---------

Siri:

![a7a976303e8fa3c272824daea4706188](https://qph.ec.quoracdn.net/main-qimg-a7a976303e8fa3c272824daea4706188.webp)

-----------

![cortana](https://image.slidesharecdn.com/nlandry-developing-windows10-apps-with-speech-and-cortana-150826134754-lva1-app6891/95/building-windows-10-universal-apps-with-speech-and-cortana-28-638.jpg?cb=1440597026)


- [AI in Mobile Apps: How to Make an App like Siri](https://codetiburon.com/ai-mobile-apps-make-app-like-siri/)

---------

Sirius:

![sirius-free-voice-systems-1](https://res.infoq.com/news/2015/04/sirius-free-voice-assistant/en/resources/sirius-free-voice-systems-1.jpg)

---------
Mobile voice assistants architecture

![Mobile voice assistants architecture](https://www.cleveroad.com/images/article-previews/Basic-technologies-in-mobile-voice-assistants.png)


[how-to-create-virtual-assistant-apps-like-siri-and-google-assistant](https://www.cleveroad.com/blog/how-to-create-virtual-assistant-apps-like-siri-and-google-assistant)

--------------------

The complete ASR Infograph:


![oice_search-clean-hook](https://www.technology.org/texorgwp/wp-content/uploads/2018/07/voice_search-clean-hook.png)



----------

Bot ecosystem and frameworks:


![c2f9ee689ce32bef47152b8ed2046c1a](https://d3ansictanv2wj.cloudfront.net/bots-landscape-2-c2f9ee689ce32bef47152b8ed2046c1a.png)

--------

![5588dd73-2c97-4efb-9a8e-e24ff0f31806](https://azurecomcdn.azureedge.net/mediahandler/acomblog/media/Default/blog/5588dd73-2c97-4efb-9a8e-e24ff0f31806.png)

Source: [Conversational Bots Deep Dive – What’s new with the General Availability of Azure Bot Service and Language Understanding](https://azure.microsoft.com/en-us/blog/conversational-bots-deep-dive-what-s-new-with-the-general-availability-of-azure-bot-service-and-language-understanding/)


---------
--------------