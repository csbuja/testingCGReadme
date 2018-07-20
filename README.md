Counting grid learning and visualziation code here is available for research purposes.
Code was developed by Nebojsa Jojic, Alessandro Perina (the learning algorihtms) and Andrzej Turski, Spencer Buja, Nebojsa Jojic, and  Alessandro Perina (the counting grid browser) at Microsoft.
Extract the files into a directory on your PC.
To run the browser with the existing example, go to the Browser directory and run the CountingGridsDesktop.exe or runCG.cmd. (The browser may crash if the files in the directory for the dataset are incomplete).
To turn your data into files for the browser, edit and run main.m from Matlab. (In fact, try running it first as is). The input file should be in the directory Input and contain up to three tab-delimited columns as in our example dictionarySample.txt. The three columns are the title, abstract and a link to the document (so that you can click on the document in the browser and follow the link). The output files will be stored in a subdirectory of Browser/Data (in our example, dictionarySample) . The input/output names can be specified in main.m (just add the appropriately formated and name file into Input directory, and run main.m).
The code is limited in several ways. The browser reads large text files into memory instead of using a database. This limits it to dataset sizes of 30-40k documents. The leanring is done in a batch mode in Matlab. Di Wang has a torch version, Spencer Buja has a python version, and Yingzhen Yang has written CUDA version as well as an online learning version (which adds the data to the model in smaller batches for much larger datasets). These may be available upon request from Nebojsa or these authors. We decide to make this original simple Matlab implementation at the core of this repository because none of the other solutions were developed to work well with the browser.
While dataset limitation may be of issue in many cases, we hope that by simply training on a fraction of the data still provides interesting insights.
The development of tools that scale better is ongoing.