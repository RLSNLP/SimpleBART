We use the method from https://aclanthology.org/2021.semeval-1.72/ to identify the word complexity. Then, we create the data for continued pre-training. An example .csv file is in this folder. The 'text' column represents the masked text and the 'label' column represents the original text.

To continue pre-training, you could execute the following commands:

python MLM.py --train_file train.csv --validation_file valid.csv --model_name_or_path ./bart/ --per_device_train_batch_size 64 --num_train_epochs 1 --learning_rate 5e-5 --num_warmup_steps 0 --output_dir ./output/
