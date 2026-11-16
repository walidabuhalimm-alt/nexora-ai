from flask import Flask
import os

app = Flask(__name__)

@app.route("/")
def home():
    return "NEXORA AI is Online ✅"

@app.route("/health")
def health():
    return {"status": "ok", "bot": "NEXORA AI"}

if __name__ == "__main__":
    port = int(os.environ.get("PORT", 10000))
    app.run(host="0.0.0.0", port=port)
