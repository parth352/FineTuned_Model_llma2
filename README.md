# FineTuned_Model_llma2
finetuned tinyllama2 model for realEstate based on Indian ministry of housing data

# 🤖 Serving AI Model via Google Colab + Ngrok + Postman

This guide explains how to serve a locally trained AI model using **Google Colab**, expose it using **Ngrok**, and hit it via **Postman**. It also explains how to push changes to GitHub directly from Colab.

---

## 📌 Prerequisites

- A trained model (e.g., TinyLLaMA or LLaMA-2)
- [Google Colab](https://colab.research.google.com/)
- [Ngrok account](https://ngrok.com/)
- [GitHub account](https://github.com/)
- Postman installed

---

## ✅ Step 1: Set Up Ngrok Account

1. Go to [https://dashboard.ngrok.com/signup](https://dashboard.ngrok.com/signup) and create a free account.
2. After login, you’ll get an **Auth Token** from your dashboard.
3. Copy the token for later use.

---

## ✅ Step 2: Serve Model in Google Colab

1. Load your fine-tuned model in Colab using `transformers` or `text-generation` libraries.
2. Start an API server in Colab using **FastAPI** or **Flask**:

```python
!pip install fastapi uvicorn nest-asyncio pyngrok

from fastapi import FastAPI, Request
from pydantic import BaseModel
import nest_asyncio
import uvicorn

app = FastAPI()

class Input(BaseModel):
    question: str

@app.post("/chat")
async def chat(input: Input):
    # Replace this with your model inference
    return {"response": f"Answer to: {input.question}"}

nest_asyncio.apply()
uvicorn.run(app, host="0.0.0.0", port=8000)
