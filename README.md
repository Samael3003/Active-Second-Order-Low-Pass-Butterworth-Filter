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

![image](https://user-images.githubusercontent.com/103866475/211167874-9c16058d-1e50-4250-91ea-97846d1d0791.png)

·	Once we have the transfer function of the desired Butterworth filter, we can obtain the following:

    1. The pole-zero plot
    2. The frequency response
    3. The cascade representation of first and second order filters
    4. The practical realization of the filter
    5. The impulse and step response of the filter
    6. Compare the frequency response of the designed filter with that of the desired filter.

·	The realization of Band-elimination filters Band elimination filters (or band reject filters) have a frequency response as shown in figure below

![image](https://user-images.githubusercontent.com/103866475/211168130-f833c1bd-b100-455b-b61a-543f98ac4bd2.png)


It is possible to realize a BEF using a parallel connection of LPF and HPF as shown in figure below. But this method requires more components, and hence is not used


## The Second Order Butterworth LPF :

Butterworth filters are characterized by the property that the magnitude characteristic is maximally flat at the origin of the s plane. The transfer function of anthn order Low-pass-Butterworth filter is given by:

![image](https://user-images.githubusercontent.com/103866475/211168147-4726b2c0-476b-4db6-9401-762374bd27b6.png)

Hence, We have the transfer function of Second order Butterworth FIlter as:

    H(s)=K0/((s-s1)(s-s2))

Where, K0 is normalising constant

    S1=e^((j3π/4)) = (-0.707+0.707j)
    
    S2=e^((j3π/4)) = (-0.707+0.707j)

![image](https://user-images.githubusercontent.com/103866475/211168182-deaefa50-6e64-4e01-838a-d8f0ce87dfaf.png)

We know that the following Laplace Transform relation:

![image](https://user-images.githubusercontent.com/103866475/211168200-d9652c5b-a752-4757-8125-ca9fa5220d11.png)

And hence the impulse response of the second order Butterworth filter is given by:

![image](https://user-images.githubusercontent.com/103866475/211168218-470bb67a-0fce-4b9c-af7e-dbc9377db42e.png)

Applying Continuous Frequency Transformation, 

We have Second Order Butterworth Filter with cut-off  w_c is given by:

![image](https://user-images.githubusercontent.com/103866475/211168234-cee367b8-b1d6-4968-93e6-d42b2d3375c8.png)

Obtaining the transfer function of filter, :

![image](https://user-images.githubusercontent.com/103866475/211168244-051b7204-ba3c-4eeb-8d76-ce65e1191900.png)

We shall attempt to obtain the transfer function of the above system using Laplace
Transform. 

Applying the voltage division across resistors R1 and R2, we have

![image](https://user-images.githubusercontent.com/103866475/211168263-5a80ecb0-a686-4a48-9bb5-bc73372b8cc6.png)

Applying the voltage division across resistor and capacitor, we have :

![image](https://user-images.githubusercontent.com/103866475/211168276-dfe77ce1-e786-446e-bc4e-530f670be914.png)

Hence, 

![image](https://user-images.githubusercontent.com/103866475/211168294-76d2e988-4ec8-4bcf-80d4-e38bea271ebe.png)

Then, we apply Current division Property,

And thus, the transfer Function is given by :

![image](https://user-images.githubusercontent.com/103866475/211168314-d92b9279-d00e-4bd2-81cd-d3153b097b52.png)


## Circuit Diagram - 

![image](https://user-images.githubusercontent.com/103866475/211168341-ebff6523-6663-4a8b-b18f-b32ba46db192.png)

## Output Image's - 

![image](https://user-images.githubusercontent.com/103866475/211168369-45b2eb28-4888-4df6-9f29-35d00a1d5706.png)

![image](https://user-images.githubusercontent.com/103866475/211168376-8228eff4-17c8-4ca0-8514-4a1ccf7aa668.png)

![image](https://user-images.githubusercontent.com/103866475/211168382-f56d0b94-d2a9-43b4-b5ab-2a50b94832a9.png)

## Applications - 
●	Generally, low pass filters are useful for eliminating noise, which is usually high frequency.

●	They are often used to stabilize opamps and other circuits, basically by cutting their high frequency gain and moving their gain crossover point to the left of the phase crossover, essentially preventing positive feedback from being introduced in certain kinds of simple circuits or plants (systems to be controlled). 

●	In image processing, a LPF can introduce a blur, and in acoustics, you can use it to separate out the low end of the sound to sent it to a subwoofer or something.

