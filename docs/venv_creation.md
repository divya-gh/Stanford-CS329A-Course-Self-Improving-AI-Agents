1. Create the venv
bash
```
python3 -m venv agent-env
```
2. Activate it
bash
```
source agent-env/Scripts/activate

```
3. Install Dependancies
```
pip install langgraph langchain openai anthropic google-generativeai
pip install langchain-google-genai
pip install google-genai
pip install python-dotenv
pip install jupyter ipykernel
python -m ipykernel install --user --name agent-env
```

4. Add your Gemini API key inside .env
Put this inside the file:
```
GEMINI_API_KEY=your_actual_key_here
```
⚠️ No quotes  
⚠️ No spaces  
⚠️ No export keyword

Just the key.


5. Minimal Gemini client test
Create a file test_gemini.py:
```

import google.generativeai as genai
import os

genai.configure(api_key=os.environ["GEMINI_API_KEY"])

model = genai.GenerativeModel("gemini-2.0-flash-thinking")

response = model.generate_content("Hello Gemini, test message.")
print(response.text)
```