# Speech-Denoising---Probabilistic-Latent-Semantic-Indexing

### 1. Convert the two training signals trs.wav and trn.wav using the earlier STFT setup you used in the previous homework. Let’s call these complex-valued matrices S and N.
### 2. Build a speech denoising system by using the PLSI algorithm. 
### 3. First, run your PLSI algorithm to learn B(1) from |S| (the magnitudes).
### 4. Second, run your PLSI algorithm to learn B(2) from |N|.
### 5. Third, load your test mixture tex.wav and turn it into a spectrogram X. Run your third PLSI routine here to learn Θ(3) by taking the magnitudes |X|. Remember, you don’t want to update B(1) and B(2) during testing. You just initialize them from the ones you trained.
### 6. You know, the speech source can be first recovered by doing B(1)Θ(3) , where Ks is the 1:Ks ,: number of basis vectors in B(1). It means that you need to pick your own choice of Ks and Kn during training.
### 7. However, B(1)Θ(3) will only give you the “probability matrix” of the speech source, not 1:Ks ,: the actual spectrogram. Hence, you need to turn it into some kind of TF-bin-wise posterior probability (of belonging to the speech source) and use it as a mask.
### 8. Transform Sˆtest back to the time domain.
### 9. Report the SNR value of the separation result by comparing sˆtest to tes.wav.
### 10. Plug in the recovered speech to the notebook with a player.
