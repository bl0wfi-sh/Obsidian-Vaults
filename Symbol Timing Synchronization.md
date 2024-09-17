## how does it work?
- the idea is to detect zero crossing.
- basically when the symbol goes from -1 to 1 we detect the zero point and that point in time is the END of a symbol boundary
- as you can imagine depending on the number of samples per symbol we may not get a point EXACTLY at zero so interpolation is necessary. But as we interpolate we get a bunch of samples. We only want a single sample at the most ideal point and as a result decimation is needed 
## Basic Structure 
- Timing Error Detector (TED)
	- The algorithm that identifies if we are "early" or "late" to the ideal sampling time.
	- Some TED's use zero crossing
	- Some identity LARGEST slope
	- Others try to identify zero slope aka a the top of a HUMP
- How does the loop work?
	- the TED outputs a timing offset that is applied to the guestimated samples per symbol of the received signal 