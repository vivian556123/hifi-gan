# ENV
conda create -n hifigan python=3.6

pip install -r requirement.txt

pip uninstall --yes librosa

pip install librosa --force-reinstall