# UI-TARS-Google-Colab-Integration
Use this to run UI TARS on low power hardware for free!

Instructions:
1. Copy the below command to your clipboard, and open up Google Colab and sign in. Then, press 'New Notebook' and aste the command you copied into the code area.
  `!pip install vllm
  !pip install pyngrok
  from pyngrok import ngrok
  !ngrok authtoken [REPLACE THESE WORDS AND BRACKETS FOR YOUR AUTHTOKEN]
  
  public_url = ngrok.connect(8000)
  print("Public URL:", public_url)
  
  !vllm serve "bytedance-research/UI-TARS-2B-SFT" --limit-mm-per-prompt "image=5" --dtype=half &`

3. Create an Ngrok account and press 'Your Authtoken'. Then, copy this to your clipboard.
