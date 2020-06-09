To create own data file with 10 folds and run mainProgram, you can use the following steps:
1. Create a csv file (e.g. mydata.csv) with your data (one row for one record/pattern, data should start from 1st row & 1st col, no header rows/cols)
2. Open your csv file in Matlab using Import data from Home tab
3. In the Output Type tab select "Numeric Matrix" and click Import Selection
4. The data will be imported as a variable inside the workspace
5. Create a variable for input data by by typing X = []; in Matlab's command window
6. Create a variable for output by typing y = []; in Matlab's command window
7. Copy all inputs from mydata file to X (e.g. X = mydata(:, 1:end-1), this assumes that the name of the data file is "mydata" and all columns besides the last column are input features)
8. Copy all class labels to y (e.g. y = mydata(:, end), last column contains the class labels)
9. Save the file by typing save mydata.mat X y in Matlab's command window
10. Create directory Datasets and copy mydata.mat file to Datasets
11. Run program CVpartition_data program by typing CVpartition_data(10) in Matlab's command window
12. Your mydata directory with 10 folds data will be created under Data directory
13. Open mainProgram.m and add following line Problem = {'mydata'}; and comment out any existing lines with Problem=; 
14. Run the mainProgram.m file by typing mainprogram in Matlab's command window
15. The results will be saved in results.csv file 

Note: The code automatically normalizes the data using min max normalization