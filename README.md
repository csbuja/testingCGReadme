OpenCG
==================================
**OpenCG** is an unsupervised learning system for understanding and exploring natural language documents using counting grids. The system ships with an oﬀ-the-shelf implementation of training a counting grid model. It also includes visualization software to explore text data using the model.

The counting grid learning and visualization code is available for research purposes only. All of the code was originally developed at Microsoft. The learning code and algorithms were developed by Nebojsa Jojic and Alessandro Perina. Andrzej Turski, Spencer Buja, Nebojsa Jojic, and Alessandro Perina developed the counting grids browser.

Installation
--------

Clone this repository.

To run the browser with the existing example, go to the Browser directory and run CountingGridsDesktop.exe or runCG.cmd. The browser may crash if the files in the directory for the dataset are incomplete.

To turn your data into files for the browser, edit and run main.m from Matlab. The input file should be in the directory Input and contain up to three tab-delimited columns as in our example dictionarySample.txt. The three columns are the title, abstract, and a link to the document (to enable following the link to document metadata). The output files will be stored in a subdirectory of Browser/Data (e.g. dictionarySample). The input/output names can be specified in main.m. Just add the appropriately formatted and named files into Input directory and run main.m.


Limitations
--------
The code is limited in several ways. The browser reads large text files into memory instead of using a database. This limits it to dataset sizes of 30-40k documents. The learning is done in a batch mode in Matlab. Di Wang has a torch version. Spencer Buja has a Python version. Yingzhen Yang has written a CUDA version as well as an online learning version (which adds the data to the model in smaller batches for much larger datasets). These may be available upon request from Nebojsa or these authors. We decided to make this simple Matlab implementation at the core of this repository because none of the other solutions were developed to work well with the browser.

While dataset size limitations may be of issue in many cases, we hope that simply training on a fraction of the data will still provide interesting insights. The development of tools that scale better is ongoing.

Platform Support
--------
Though the learning code is platform agnostic, the visualization code is a Windows Presentation Foundation (WPF) application. WPF will only run on Windows. We are developing a new visualization tool for the web.
