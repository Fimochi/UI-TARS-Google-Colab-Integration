# UI-TARS-Google-Colab-Integration
Use this to run the bytedance-research/UI-TARS-2B-SFT model on any hardware that you need to use UI-TARS on for free (Yes, even without a GPU!)

**Instructions:**
1. Copy the below command to your clipboard, and open up Google Colab and sign in. Then, press 'New Notebook' and paste the command you copied into the code area.
   ```
   !pip install vllm
   !pip install pyngrok
   from pyngrok import ngrok
   !ngrok authtoken [REPLACE THESE BRACKETS AND WORDS WITH YOUR authtoken]
   
   !vllm serve "bytedance-research/UI-TARS-2B-SFT" --limit-mm-per-prompt "image=5" --dtype=half &
   
   public_url = ngrok.connect(8000)
   print("Public URL:", public_url)
   ```

2. Create an Ngrok account and press 'Your Authtoken'. Then, copy this to your clipboard, and paste this in the [REPLACE THESE BRACKETS AND WORDS WITH YOUR authtoken] area. Then, you may run the model.
3. Wait for the model to download. This should take a few minutes.
4. 
