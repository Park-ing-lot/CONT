# CONT

## Set up
1. Clone our repository.
   ```
   git clone https://github.com/Park-ing-lot/CONT.git
   ```
   
2. Clone and set the environments by following the instructions from [MoLFormer](https://github.com/IBM/molformer/tree/main). \
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
