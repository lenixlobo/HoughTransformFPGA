

<!-- ABOUT THE PROJECT -->
## About The Project


This repository maintains the code implementing Hough transform on a FPGA


The code is divided into 2 folders:
* Python : This implements the hough transform algorithm on the input source using OpenCV. The python code will be deployed on a micro-controller (Rpi 3b)
* FPGA : This implements the FPGA code designed for the Basys3, simulated on Vivado 


<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Prerequisites

For rpi3b+, install the required python dependencies imported in the lanedetect.py file. The dependencies include scipy, matplotlib and openCV.
Run the lanedetect.py, to get the output.

For FPGA, use the basys3 development board. For simulation, use Vivado (2018.2 and above)
Make sure you set the correct read and write path location in the tb_modules.v to open and write images.
In our case, the image 'flower.bmp' is opened from the bmp folder, and the processed file is written in bmp/output as 'output.bmp'


In tb_modules.v, lies the code which does the read and write operations.
Modules.v implements the actual filtering logic.
Use the sel_module variable to select which filter you wish to apply

To run the code, Run simulation -> Run All

To rerun change code, need to relauch the simulation -> Run All 

Selection Bits and corresponding filters : 

0000 - Gray

0001 - Increase brightness

0010 - Decrease brightness

0011 - Color Inversion

0100 - Red Filter

0101 - Blue Filter

0110 - Green Filter

0111 - No operation. (Rewrites the original image)
