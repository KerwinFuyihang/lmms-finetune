1. Download this finetune_llava repo to the server
2. Assume you already have the Data folder (inside you have two subfolders called compound and subfigures).
Then, recommend putting the compound figures and subfigures into one folder, let's say call it allfigrues. using the command:
```
mkdir -p /Users/yihang/Desktop/pmc_llava/Data/images/allfigures
rsync -r /Users/yihang/Desktop/pmc_llava/Data/images/compound/ /Users/yihang/Desktop/pmc_llava/Data/images/allfigures/
rsync -r /Users/yihang/Desktop/pmc_llava/Data/images/subfigures/ /Users/yihang/Desktop/pmc_llava/Data/images/allfigures/
```

3. example_image.sh (in the example_scripts folder) is the file we submit to the server. In this file, you can modify the model we use (we can run the supported_models.py to see what models are supported under this codebase) and other settings including peft strategies (if needed).
I use the llava_onevision here and set the model_max_length 32768 (based on the train.sh script provided by official llava_onevision.)

4.  use ```pip install -r requirements.txt``` to install the environment. Do not forget to change the environment path in the example_image.sh file.
5.  The data (multi_image.json) in the example_data folder can be successfully implemented (tested on a rented A100 40G).


 
