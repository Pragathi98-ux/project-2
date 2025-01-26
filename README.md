Paris Olympics step by step Process

1.__Set Kaggle API Credentials Directory__:
  This sets the environment variable KAGGLE_CONFIG_DIR to specify the directory where the Kaggle API credentials are stored. You should update 'kaggle_path' with the actual path to the 
  Kaggle configuration directory containing your kaggle.json file. This file is required to authenticate with Kaggle's API.
2. __Dataset Identifier and Download Path__: 
   The dataset variable specifies the Kaggle dataset identifier, in this case, the dataset for the "Paris 2024 Olympic Summer Games". You can replace it with the identifier of any other 
   dataset you'd like to download.The download_path specifies where the dataset files will be saved on your local machine. Update 'file_path' to the path of the folder where you want to 
   store the dataset.
3.__Clean the Download Folder__ : 
  This loop checks the download folder and deletes any existing files. This helps avoid issues where old or duplicate files might interfere with the new dataset download.If there’s an 
  error during file deletion (e.g., file is in use), it will print an error message but continue with the process.
4.__Download and Unzip Dataset__:
  This command uses the Kaggle API to download the dataset and unzip it into the specified download path. The dataset files will be extracted automatically after download.
5. __List of CSV Files to Import__:
  This list contains the names of CSV files expected to be present in the dataset. These files contain the actual data that will be loaded into Pandas DataFrames.
6. __Load CSV Files into DataFrames__:
  This loop iterates over each CSV file in the csv_files list, constructs the full file path, and uses Pandas' read_csv function to load the CSV file into a DataFrame.
  Each DataFrame is stored in a dictionary named dataframes, with the key being the base name of the CSV file (without the .csv extension). This allows easy access to the datasets by their    
	respective table names.
