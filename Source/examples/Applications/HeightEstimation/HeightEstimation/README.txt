========================================================================
    CONSOLE APPLICATION : HeightEstimation Project Overview
========================================================================
Height Estimation:

	The Height of the person standing under the camera is estimated with the reference to the "BaseHeight" file generated by the HeightCalibration project.
	The Height of the person is actually selected by scanning the depth in the 1/3 of the diaparity map. the lowest depth is selected as the depth of the head.
	The Head depth is subtracted from the base depth and the height of the person is displayed.

Note: 
	Make the sure the person head is in 1/3 of the frame and Height calibration is executed first.


Command to create HeightEstimation binary:
==========================================
To Build:
		$ make
		
To clean:
		$ make clean	
==========================================
