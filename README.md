# ALERTCalibrationSuite
A calibration suite for the ALERT detector
at current status the suite has two parts:

DC Calibration and ATOF calibration

ATOF :

-Front Back Calibration
-Timing calibration between front and back scintillator bars
-Pedestal Calibration
-Time Walk Calibration :
time walk is an instrumental shift in the measured TDC hit time that arises when using leading edge discriminators (LEDs). This shift in timing arises due to the finite rise time of the PMT analog pulse. For a given event time, pulses of different amplitude cross the discriminator threshold at slightly different times

-Veff Calibration :
The effective velocity is the average speed that scintillation light propagates along the scintillation bars.

DC Calibration: 

1)T0 Calibration:
 
 The drift time is the elapsed time between the time that the particle traversed the wire cell and the time that the released gas ions (electrons) reached the sense wire.
 The drift time needs to be corrected for various fixed and event-dependent time delays.
 T0 is the fixed time (cable) delay for the wire and contributes the most to the time delay.

2)T2D Calibration:

An initial parametrization is used to translate drift times into drift distances in order to use in tracking :
CalcDoca : DOCA calculated from time
TrackDoca : Distance of hit wires from fit tracks
Find a new functional form that minimizes the distance between DOCA and TrackDoca (residuals).
