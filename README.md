

<!-- ABOUT THE PROJECT -->
## About The Project


This repository maintains the code implementing Hough transform on a FPGA


The code is divided into 2 folders:
* Python : This implements the hough transform algorithm on the input source using OpenCV. The python code will be deployed on a micro-controller (Rpi 3b)
* FPGA : This implements the FPGA code designed for the Basys3, simulated on Vivado 


<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Prerequisites

For rpi3b+, install the required python dependencies imported in the lanedetect.py file. The dependencies include scipy, matplotlib and openCV.

For FPGA, use the basys3 development board. For simulation, use Vivado (2018.2 and above)
