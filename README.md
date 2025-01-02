1. Download this finetune_llava repo to the server
2. Recommend put the compound figures and subfigures into one folder, let's say call it allfigrues. using the command:
```
mkdir -p /Users/yihang/Desktop/pmc_llava/Data/images/allfigures
rsync -r /Users/yihang/Desktop/pmc_llava/Data/images/compound/ /Users/yihang/Desktop/pmc_llava/Data/images/allfigures/
rsync -r /Users/yihang/Desktop/pmc_llava/Data/images/subfigures/ /Users/yihang/Desktop/pmc_llava/Data/images/allfigures/
```

3. example_image.sh is the file we submit to the server. In this file, you can modify the model we use (run the supported_models.py to see what models are supported under this codebase) and other settings including peft strategies (if needed).
 
