# Signals-and-Systems_WHO-Data-Manipulation

## Relevance of the signal operations:

1)	Auto-correlation
Auto-correlation is a representation of the degree of similarity between a input time signal series and a delayed version of itself over running/sequential time intervals.
In this operation a single time series is considered. Its main purpose is to find non-randomness in data.

![Comparison_convolution_correlation svg](https://user-images.githubusercontent.com/67193440/178097850-9c773547-39f8-4e7f-89fe-8e787fdc3e86.png){:height="36px" width="36px"}.
 Example Code for auto-correlation in MATLAB for lag=15,
		acf = autocorr(Y,'NumLags',15);

2)	Cross-correlation:
Cross-correlation is used to find similarity of two series as a function of the displacement of one with respect to the other (shifted/lagged). In this operation, two different time series are evaluated at the same instance. If the cross-correlation coefficient is 1, then the two signals under consideration have a high similarity/direct relationship.











        Source: https://upload.wikimedia.org/wikipedia/commons/2/21/Comparison_convolution_correlation.svg

Example code for Cross-correlation in MATLAB is:

r=xcorr(x,y)
[c,lags] = xcorr(x,y);

3)	Signal Addition
Addition of two time-series/signals is the addition of their corresponding amplitudes or Y-axis values.










              Source: https://www.tutorialspoint.com/signals_and_systems/signals_basic_operations.htm
Example MATLAB code for addition:
z=y1+y2;
Where, y1=signal 1 and y2=signal 2

4)	Signal subtraction
Subtraction of two time-series/signals is the subtraction of their corresponding amplitudes or Y-axis values.









                  Source: https://www.tutorialspoint.com/1signals_and_systems/signals_basic_operations.htm
Example MATLAB code for Subtraction:
z=y1-y2;
Where, y1=signal 1 and y2=signal 2
5)	Signal Multiplication
Multiplication of two signals is the multiplication of the amplitudes or the Y-axis values.












         Source: https://www.tutorialspoint.com/signals_and_systems/signals_basic_operations.htm
Example code for multiplication in MATLAB:
z=y1.*y2;
Where, y1=signal 1 and y2=signal 2
6)	Time-shifting 
Time shifting of the signal refers to the shifting of the signal either by adding or subtracting along the time axis.
The two kinds of shifts are:
1)	Negative shift, x(t+to) or advanced signal
2)	Positive shift, x(t-t0) or delayed signal











                Source: https://www.tutorialspoint.com/signals_and_systems/signals_basic_operations.htm
7)	Time-Scaling
Time scaling modifies the periodicity of the signal by keeping the amplitude constant.
There are two types of scaling:
1)	Compression of the signal
2)	Expansion of the signal







Where, (A)- Expanded signal
	(B)- Compressed signal
Example code for Time-Scaling in MATLAB:
t=x/b;
(or)
t=x*b;
Where, x-Input signal
            b-Scaling factor

8)	Time-Reversal
Time-reversal is applicable on both continuous and discrete signal. The Y-axis acts as a reflecting medium. The signal appears reflected/reversed with respect to the Y-axis.






Source:https://www.tutorialspoint.com/signals_and_systems/signals_basic_operations.htm
Where, x(t) is the original signal and x(-t) is the reversed signal.
Example code of Time-Reversal in MATLAB:
m=-x;
(or)
c=fliplr(x);

Where, x-original input signal.
9)	Convolution:
Convolution is the amount of overlap of one function (here signal) x1 as it is shifted over the other function x2 (here signal). Mathematically, it is defined as the integral of the product of the two functions after one is reversed and shifted. It is a way of combining two signals to form the third signal based on the knowledge about the system’s unit impulse response.

 








                   Source:https://en.wikipedia.org/wiki/Cross-correlation#/media/File:Comparison_convolution_correlation.svg
Example code for Convolution in MATLAB:
z=conv(y1, y2);
Where, y1-Signal-1
	y2-Signal-2
