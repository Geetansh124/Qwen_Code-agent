================================================================================
                    KAGGLE TRAINING FILES (ONLY 2 FILES)
================================================================================

This folder contains ONLY the 2 files you need for running on Kaggle with 
ZERO ERRORS:

--------------------------------------------------------------------------------
FILE 1: codeagent_kaggle_bundle.zip  (23.5 MB)
--------------------------------------------------------------------------------
WHAT TO DO:
  1. Go to https://www.kaggle.com
  2. In the top-left sidebar, click: '+ Create' -> 'New Dataset'
  3. Drag & drop 'codeagent_kaggle_bundle.zip' into the upload box
  4. Title your dataset: codeagent-bundle
  5. Click 'Create' (Kaggle processes it in ~10 seconds)

--------------------------------------------------------------------------------
FILE 2: codeagent_kaggle_training.ipynb
--------------------------------------------------------------------------------
WHAT TO DO:
  1. Click '+ Create' -> 'New Notebook'
  2. Click 'File' (top menu) -> 'Import Notebook' -> upload this file
  3. On the right-side panel:
     - Under 'Data' / 'Input': Click '+ Add Input' -> select 'codeagent-bundle'
     - Under 'Session options':
         * Accelerator: select 'GPU T4 x 2'
         * Internet: toggle to 'Internet on'
  4. Click 'Run All' (Ctrl + F9)

--------------------------------------------------------------------------------
WHY THIS RUNS WITH ZERO ERRORS:
  - Has 'bitsandbytes>=0.46.1' pre-configured (4-bit QLoRA uses only 4.5 GB VRAM)
  - Has 'expandable_segments:True' enabled (stops CUDA memory fragmentation)
  - Has 'gradient_checkpointing=True' enabled (prevents CUDA Out-Of-Memory)
  - Targets GPU 0 with 'CUDA_VISIBLE_DEVICES=0'
================================================================================
