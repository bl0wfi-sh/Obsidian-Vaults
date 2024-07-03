The cmsis library likes to hold complex data in an interleaved form.
- { real[0], imag[0], real[1], imag[1] ... }

The library also likes to put the output of a computation in the same buffer used as input.
- For example a 1024 point complex FFT needs to have the following format
- { [input complex points], [output complex points] }
	- sub array holding complex input and output complex points will each be 2 * num of samples because the imaginary and real values are interleaved.
- Thus the total buffer size of an fft on 1024 complex samples = 1024 * 2 * 2
- First half is input, second half is output.
- If it's done on float 16's then final byte size is 1024 * 2 * 2 * 2