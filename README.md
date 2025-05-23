🔐 Smart Audio Content Firewall
This tool processes audio or video content to transcribe, classify sensitive topics, detect toxicity, and provide explainable alerts. Designed for journalists, tech leads, and parents, the tool supports live audio, media file analysis, and redacted content review.

🧠 Why These Models?
🎧 Whisper (by OpenAI) – For Transcription
Why Whisper?
Whisper is a powerful open-source speech-to-text model from OpenAI that performs extremely well across accents, background noise, and real-world audio. Unlike alternatives like Vosk or Google Speech API:

✅ No need for internet (runs locally)

✅ Better generalization on noisy input

✅ Supports multi-lingual speech

✍️ DeepMultilingualPunctuation – For Punctuation Restoration
Why this model?
Whisper returns raw text without punctuation. This model adds sentence boundaries and structure, crucial for sentence-level classification.

✅ Multilingual support

✅ Compatible with Whisper output

📚 FLAN-T5 (Google) – For Semantic Topic Classification
Why FLAN-T5?
FLAN-T5 is fine-tuned on instruction-following tasks, making it ideal for zero-shot classification of complex statements into user-defined labels.

✅ Understands nuanced prompts

✅ Zero-shot: no fine-tuning needed

✅ Better than BERT for open-ended generation

⚠️ Unitary/toxic-bert – For Toxicity Detection
Why toxic-BERT?
A simple and effective fine-tuned BERT model for detecting offensive and inappropriate language.

✅ Lightweight and fast

✅ Sufficient for sentence-level toxicity scoring

✅ Runs on CPU

💻 Why Tkinter for the Interface?
Why tkinter (vs. Streamlit, Flask)?

🖥️ Tkinter is ideal for building simple desktop tools without needing a web server.

💡 It’s fast to develop, and works well offline.

👨‍👧‍👦 Great for non-developers who prefer standalone applications.

🗂️ Features
 Upload audio/video file and extract audio

 Record live audio (10s, adjustable)

 Whisper-based transcription

 Restore punctuation and split sentences

 Classify into user-defined sensitive topics

 Detect and score toxicity

 Auto-redact harmful or sensitive content

 Explain why each alert was triggered

 Save results to JSON

🧪 Sample Use Cases
A journalist wants to check if interview recordings leak confidential sources.

A founder verifies if a company all-hands meeting discloses unreleased product plans.

A parent reviews a child’s gaming voice chat for inappropriate remarks.

🧰 How to Run
🔧 Installation
bash
Copy
Edit
pip install -r requirements.txt
▶️ Run App
bash
Copy
Edit
python app.py
📂 Folder Structure
markdown
Copy
Edit
.
├── app.py
├── requirements.txt
├── README.md
└── samples/
    ├── sample_audio.mp3
    ├── transcript.txt
    └── classified_output.json
📝 Sample Output (JSON)
json
Copy
Edit
[
  {
    "sentence": "He leaked the release date of the next iPhone.",
    "matched_topic": "NDA",
    "severity": "Critical",
    "toxicity": "Non-toxic",
    "toxicity_score": 0.012,
    "redacted_sentence": "[REDACTED]",
    "justification": "This sentence discusses confidential product details, triggering NDA classification."
  }
  ]
