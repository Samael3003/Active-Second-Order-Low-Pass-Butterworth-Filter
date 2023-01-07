# Active-Second-Order-Low-Pass-Butterworth-Filter

## Introduction - 

Butterworth filters are characterized by the property that the magnitude characteristic is maximally flat at the origin, and there are no ‘ripples’, either in the pass band or in the stop band. The sequence of topics covered is as follows:

## What Does the ORDER of a Filter mean ?

Simply put, Order of the filter means the maximum number of delay elements used in the filter circuit. This can be easily observed by observing the difference equation and finding out at which sample we are having our maximum delay. 

Also if we are Z - Domain, then by observing the highest powers of ‘z’ you can tell the order of the filter. So, what happens if order increases, simply the number of delay blocks increases making the filter more complex in design, but making it more and more efficient filter.

This happens because, the more the past values of signal you accumulate, more experience you have about the signal and it’s characteristics, and it becomes easier for filter to predict or estimate or make some relevant output by taking large number of sampled input value delay versions. So the performance of a second order filter will always be better than the first order. Remember , more delay of input means, more information we have about the input and it becomes easier to produce output from such samples.

## Methodology - 

Butterworth filters are characterized by the property that the magnitude characteristic is
maximally flat at the origin of the s plane. The transfer function of anth
n order Low-pass-

Butterworth filter is given by:

    H(s)=K0/((s-s1)(s-s2)…(s-sn))

Where, K0 is normalising constant

    S_k=e^((jπ/2)[1+(2k-1)/n])

**Some features of the Butterworth filters represented by equation (1) are:**
    
    They are all-pole filters
    The poles lie on the left half of the s-plane
    They have the 3 dB cut-off ω_c=1 rad/sec
    The complete filter is specified by the order n
    Through frequency transformation, it is possible to transform the above transfer
    function to another filter of specified cut-off or type

**The design steps for obtaining the transfer function of the Butterworth filter are as follows:**

·	Given the frequency specifications, obtain the equivalent specifications of the low-pass filter (need two frequencies with desired attenuation)

·	Assume we need to have attenuation of As, Ap at frequencies fs and fp respectively. Then this corresponds to the specifications of low-pass filter

·	The order n, of the desired filter is a smallest integer that satisfies the equation given below:
