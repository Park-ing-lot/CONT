# CONT

## Set up
1. Clone our repository.
   ```
   git clone https://github.com/Park-ing-lot/CONT.git
   cd CONT
   ```
2. Download sets of similar molecules from [here](https://1drv.ms/f/s!Av7zLRuxiWW_kLs96rYdzCEkzr04jA?e=CpBmn1) and unzip it in the current directory.
   ```
   unzip feature_extraction.zip
   ```
   
3. Clone and set the environments by following the instructions from [MoLFormer](https://github.com/IBM/molformer/tree/main). \
   You also need to download the dataset and pre-trained checkpoints.
   ```
   git clone https://github.com/IBM/molformer.git
   conda activate MolTran_CUDA11
   cp CONT/* molformer/finetune/
   cd molformer/finetune/
   ```
   
## Train with CONT
1. Run CONT (Fingerprint-based Contrastive Learning). \
   First, run CONT before fine-tuning the model:
   ```
   bash run_continue_qm9.sh
   ```
   You can change tasks by modifying task-related arguments.
   
3. Fine-tune the model on downstream tasks:
   ```
   bash run_finetune_cont_r2.sh
   ```
   You can change tasks by modifying task-related arguments.
