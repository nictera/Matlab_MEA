Matlab_MEA
===============

Matlab analysis and plotting functions for data collected with multi-channel systems MC_Rack

MEA_batchConvert.m will convert raw files created by MC_DataTool into a format readable by matlab.

MC_DataTool can be downloaded here:

http://www.multichannelsystems.com/software/mc-datatool

Here are the details:

%This function converts MEA bin (binary, RAW) files into mat files in a batch. It will
%attempt to convert all "raw" files in the directory, so make sure they are
%all MEA files or enter an extension to select a few.
%
%To create the RAW file, 
%1. open MC_DataTool
%2. File-Open Multiple
%3. Select files of interest
%4. Click "bin"
%5. Click "All"
%6. Make sure "Write header" and "Signed 16bit" are checked in lower right
%7. Click Save
%8. when done, click Close

After creating the raw files, get into the directory with the raw files in matlab and run
>>MEA_batchConvert

This will create subfolders for each raw file. You can get into one of these folders and run, for example,
>>plot_MEA([15 41:45])

This will plot channels 15 and 41 through 45.
