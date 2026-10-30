# VINS AI VIDEO STUDIO — Cloud Edition (Starter)

A free-software starter for creating promotional videos on a low-spec PC. The browser app prepares a project ZIP; a Google Colab notebook renders the video in a temporary cloud runtime.

## What works in this starter
- Script-to-storyboard scene splitting
- Kannada/English/Hindi/Telugu/Tamil script input
- Kannada male (`kn-IN-GaganNeural`) and female (`kn-IN-SapnaNeural`) narration through the Edge TTS online voice service
- Upload shop/product photos, logo and optional background music
- MP4 export in vertical 9:16, landscape 16:9 or square 1:1
- SRT subtitle file output
- Cloud rendering through Google Colab; no GPU required on your PC

## Important: honest free-tier limits
This is a free-software workflow, not guaranteed unlimited free cloud hosting. Google Colab free availability, session length and compute are controlled by Google and can change. The Colab runtime is temporary; download the MP4 before closing it. Edge TTS uses Microsoft's online speech service through a community client, not a guaranteed free commercial API. It may change or be rate-limited. Check voice/service terms before commercial use. Do not upload confidential customer information.

Hugging Face Spaces is not used as the primary backend because its free hosting rules have changed; static sites are free, while ordinary Gradio/Docker compute is restricted. See official documentation links below.

## Quick start
1. Extract this ZIP on your PC.
2. Open `web/index.html` in Chrome or Edge. Internet is needed for the JSZip CDN.
3. Edit the script and business details; upload optional photos, logo and music.
4. Click **Build storyboard**, review scenes, then **Download cloud-render project ZIP**.
5. Open Google Colab: https://colab.research.google.com/
6. In Colab choose **File → Upload notebook** and upload `cloud/VINS_Cloud_Renderer.ipynb`.
7. Run the notebook cells from top to bottom. When prompted, upload `VINS_AI_Video_Project.zip`.
8. Wait for rendering. Download `VINS_Promo.mp4` and `VINS_Subtitles.srt` from the Colab file panel.

## Notes
- Kannada text must be typed in Kannada script for best pronunciation. English transliteration may be read incorrectly.
- The renderer makes a slideshow-style promotional video with gentle motion, text cards, narration, optional music and subtitles. It does not create photorealistic AI-generated moving scenes. True text-to-video diffusion requires GPU compute and is not reliably unlimited/free.
- Keep image uploads to a sensible size (e.g. 5–10 MB each) and use 3–10 photos for a short promo.
- If a font is missing, the notebook installs Noto fonts.
- For a private website, use a private hosting/account arrangement; GitHub Pages public repositories expose source code. The starter itself runs locally in your browser.

## VINS business defaults
VINS ENTERPRISES  
Opp. Sangeetha Mobiles, Bangalore Bypass Road, Lingasugur  
8147422496 / 9731443007  
Services: Computer sales and service; CCTV installation; Internet service provider; Hardware and networking solutions.

## Official references
- Hugging Face Spaces overview: https://huggingface.co/docs/hub/en/spaces-overview
- AI4Bharat Indic-TTS: https://github.com/AI4Bharat/Indic-TTS
- Microsoft Kannada voice names: https://learn.microsoft.com/azure/ai-services/speech-service/language-support?tabs=tts
- Google Colab: https://colab.research.google.com/
