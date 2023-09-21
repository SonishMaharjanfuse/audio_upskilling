# Speech Enhancement
Speech Enhancement refers to the process of improving the quality of speech signals that have been corrupted by noise. The goal is to make the speech more intelligible and perceptually pleasing to the listener. There are several techniques and algorithms used for speech enhancement, and three of them are discussed below.
## Spectral Subtraction
Spectral Subtraction is a widely used method for speech enhancement. It operates in the frequency domain and is based on the assumption that noise and speech occupy different frequency bands. The key steps involved in Spectral Subtraction are:

- <b>Short-Time Fourier Transform (STFT):</b> The noisy speech signal is divided into short overlapping frames, and a Fourier transform is applied to each frame. This converts the signal from the time domain to the frequency domain.

- <b>Estimation of Noise Spectrum:</b> In Spectral Subtraction, an estimate of the noise spectrum is obtained from the observed noisy speech signal. This is typically done by assuming that the first few frames of the signal primarily contain noise.

- <b>Spectral Subtraction:</b> The noise spectrum estimate is subtracted from the magnitude spectrum of each frame. This process attenuates the noise components, leaving behind enhanced speech components.

- <b>Inverse Short-Time Fourier Transform (ISTFT):</b> Finally, the processed frames are transformed back to the time domain using the Inverse Short-Time Fourier Transform to obtain the enhanced speech signal.

## NMF Algorithm (Non-Negative Matrix Factorization)
Non-Negative Matrix Factorization is a dimensionality reduction technique that is particularly useful for source separation tasks, including speech enhancement. It operates on a non-negative matrix and factorizes it into two lower-rank non-negative matrices. The basic idea behind NMF is that it assumes that the underlying sources are additive and non-negative.

In the context of speech enhancement, NMF can be applied as follows:

**Data Representation:** The observed noisy audio signal can be represented as a non-negative matrix, where columns represent time frames and rows represent frequency bins.

**NMF Decomposition:** The NMF algorithm factorizes this matrix into two lower-rank matrices. One matrix represents the spectral patterns or basis functions, and the other matrix represents the temporal activation coefficients.

**Source Separation:** By multiplying the basis functions and activation coefficients, the original matrix can be approximated. This allows for the separation of sources, which in the context of speech enhancement, means isolating the speech from the noise.

## ICA (Independent Component Analysis)
Independent Component Analysis is a statistical signal processing technique used for separating independent sources from a mixed signal. It assumes that the observed signal is a linear combination of independent source signals, each with a distinct probability distribution.

In the context of speech enhancement, ICA can be applied to separate the speech signal from background noise. The key steps are:

**Data Representation:** The mixed audio signal is represented as a matrix, where each row corresponds to a sensor (microphone) and each column corresponds to a time sample.

**Whitening:** The data is preprocessed to make the sources as statistically independent as possible. This often involves whitening the data.

**ICA Decomposition:** The ICA algorithm estimates a linear transformation matrix that maximizes the statistical independence of the resulting signals.

**Source Separation:** By applying the estimated transformation matrix to the mixed signal, the original independent sources can be recovered.



# Audio Annotation
 For the audio annotation we use the <a href='https://www.audacityteam.org/'>Audacity</a> as an annotation tool.
