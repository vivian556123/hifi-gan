# ENV
conda create -n hifigan python=3.6

pip install -r requirement.txt

pip uninstall --yes librosa

pip install librosa --force-reinstall

python train.py --input_wavs_dir=/home/aiscuser/Fisher_English_Processed_only_laughter/train_only_laughter --input_val_wavs_dir=/home/aiscuser/Fisher_English_Processed_only_laughter/val_only_laughter --config=config_ly_v1_fisher.json --checkpoint_path /modelblob/users/v-leyzhang/exp/hifigan/fisher_v1_test --stdout_interval 2

python train.py --input_wavs_dir=/home/aiscuser/overlap_pair_data/train_separate --input_val_wavs_dir=/home/aiscuser/overlap_pair_data/val_separate --config=config_ly_v1_fisher.json --checkpoint_path /modelblob/users/v-leyzhang/exp/hifigan/fisher_v1_stereo --stdout_interval 2