# Signals-and-Systems_WHO-Data-Manipulation

## Relevance of the signal operations:

1) Auto-correlation

Auto-correlation is a representation of the degree of similarity between a input time signal series and a delayed version of itself over running/sequential time intervals.
In this operation a single time series is considered. Its main purpose is to find non-randomness in data.

<p align="center" width="100%">
    <img width="250" height="250" src="https://user-images.githubusercontent.com/67193440/178097850-9c773547-39f8-4e7f-89fe-8e787fdc3e86.png">
</p>

 							Example Code for auto-correlation in MATLAB for lag=15,
								acf = autocorr(Y,'NumLags',15);

2) Cross-correlation:

Cross-correlation is used to find similarity of two series as a function of the displacement of one with respect to the other (shifted/lagged). In this operation, two different time series are evaluated at the same instance. If the cross-correlation coefficient is 1, then the two signals under consideration have a high similarity/direct relationship.


![download](https://user-images.githubusercontent.com/67193440/178098124-ae979fca-c219-471d-b0b7-e1924d29c0ea.png)

						Example code for Cross-correlation in MATLAB is:
								r=xcorr(x,y)
						           [c,lags] = xcorr(x,y);

3) Signal Addition

Addition of two time-series/signals is the addition of their corresponding amplitudes or Y-axis values.


![amplitude_addition](https://user-images.githubusercontent.com/67193440/178098155-07938d2a-8279-4a16-83a9-81284a54d453.png)


							Example MATLAB code for addition:
								     z=y1+y2;
						      Where, y1=signal 1 and y2=signal 2

4) Signal subtraction

Subtraction of two time-series/signals is the subtraction of their corresponding amplitudes or Y-axis values.


![amplitude_subtraction](https://user-images.githubusercontent.com/67193440/178098187-7eb7967e-c63a-4390-8b7e-29effc94a095.png)

						       Example MATLAB code for Subtraction:
								      z=y1-y2;
							Where, y1=signal 1 and y2=signal 2
							
5) Signal Multiplication

Multiplication of two signals is the multiplication of the amplitudes or the Y-axis values.


![amplitude_multiplication](https://user-images.githubusercontent.com/67193440/178098208-3f25b80c-d679-4c96-903b-9746a6d72845.png)

						    Example code for multiplication in MATLAB:
								     z=y1.*y2;
							Where, y1=signal 1 and y2=signal 2
							
6) Time-shifting 

Time shifting of the signal refers to the shifting of the signal either by adding or subtracting along the time axis.

The two kinds of shifts are:
1)	Negative shift, x(t+to) or advanced signal
2)	Positive shift, x(t-t0) or delayed signal


![time_shifting](https://user-images.githubusercontent.com/67193440/178098276-42ffd389-7185-45bf-ae54-9284c4650dfb.png)


7) Time-Scaling

Time scaling modifies the periodicity of the signal by keeping the amplitude constant.

There are two types of scaling:

1)	Compression of the signal
2)	Expansion of the signal

Where,  (A)- Expanded signal
	(B)- Compressed signal
	
![time_scaling](https://user-images.githubusercontent.com/67193440/178098294-51b36bf9-e000-47c2-89fd-ef4c1cea3724.png)
	
								Example code for Time-Scaling in MATLAB:
										t=x/b;
										(or)
										t=x*b;
									Where, x-Input signal
            								   b-Scaling factor

8) Time-Reversal

Time-reversal is applicable on both continuous and discrete signal. The Y-axis acts as a reflecting medium. The signal appears reflected/reversed with respect to the Y-axis.


![time_reversal](https://user-images.githubusercontent.com/67193440/178098349-24dc22cd-f647-4c58-b082-ed02a8b521fc.png)

						Where, x(t) is the original signal and x(-t) is the reversed signal.
							   Example code of Time-Reversal in MATLAB:
									       m=-x;
									       (or)
									    c=fliplr(x);

								   Where, x-original input signal.

9) Convolution:

Convolution is the amount of overlap of one function (here signal) x1 as it is shifted over the other function x2 (here signal). Mathematically, it is defined as the integral of the product of the two functions after one is reversed and shifted. It is a way of combining two signals to form the third signal based on the knowledge about the system’s unit impulse response.

 
![Comparison_convolution_correlation svg](https://user-images.githubusercontent.com/67193440/178098419-aaecdf76-738b-4363-8f85-37b959b0e309.png)



								Example code for Convolution in MATLAB:
									    z=conv(y1, y2);
									  Where, y1-Signal-1
									      y2-Signal-2
