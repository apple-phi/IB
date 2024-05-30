Abstracting out the modulation and demodulation we can represent the communication system assuming a constant modulation scheme as

![[binary-channel.png]]

## Binary symmetric channel
Define the crossover probability $p$ for a channel $\operatorname{BSC}(p)$ as the equal probability of a 0 or 1 bit flipping incorrectly during transmission. 

## Repetition code
It is sensible to add redundancy to the source bits during transmission to help with error detection.

The simplest channel code for $\mathrm{BSC}$ is a ($n$,1) repetition code, where $n$ is odd.
- Encoding—repeat each source bit $n$ times
- Decoding—majority vote of each $n$-tuple of bits
![[rep-code-3-1.png]]

A decoded bit is now only in error if 

tbc decoding errors, data rate, $P_{e}$ vs. rate