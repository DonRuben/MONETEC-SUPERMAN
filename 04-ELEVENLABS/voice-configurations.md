# 🎤 ELEVENLABS VOICE CONFIGURATIONS

## MONETEC VOICE SETUP

### Primary Voice Configuration
```python
# MONETEC Professional German Narrator
voice_config = {
    "voice_id": "MONETEC-VOICE-V1",  # To be created
    "name": "Monetec Professional",
    "description": "Male German narrator, 35-45, confident and innovative",
    "language": "de",
    "accent": "German (Germany)",
    "age": "middle-aged",
    "gender": "male",
    "use_case": "narration"
}
```

### Model Selection

#### V2 Model (Automatic Integration)
```python
# For code integration
model_v2 = {
    "model_id": "eleven_multilingual_v2",
    "stability": 0.65,
    "similarity_boost": 0.75,
    "style": 0.35,
    "use_speaker_boost": True,
    "language": "de"
}
```

#### V3 Model (Manual with Emotions)
```python
# For ElevenLabs Playground
model_v3 = {
    "model_id": "eleven_multilingual_v3",
    "emotion_tags": [
        "confident",
        "professional",
        "enthusiastic",
        "trustworthy",
        "innovative"
    ],
    "emotion_examples": {
        "intro": "<emotion:confident>Willkommen bei Monetec</emotion:confident>",
        "benefits": "<emotion:enthusiastic>€10 Millionen bereits verarbeitet</emotion:enthusiastic>",
        "cta": "<emotion:trustworthy>Kontaktieren Sie uns heute</emotion:trustworthy>"
    }
}
```

### Voice Creation Script

```python
from elevenlabs import Voice, VoiceSettings, generate

# Create Monetec Voice
def create_monetec_voice():
    voice = Voice(
        name="MONETEC-VOICE-V1",
        description="Professional German narrator for Monetec presentations",
        samples=[
            "sample1_professional.mp3",
            "sample2_confident.mp3",
            "sample3_technical.mp3"
        ],
        settings=VoiceSettings(
            stability=0.65,
            similarity_boost=0.75,
            style=0.35,
            use_speaker_boost=True
        )
    )
    return voice
```

## LEONARDO VOICE SETUP

### Avatar Voice Configuration
```python
# Leonardo DiCaprio Style Voice
leonardo_config = {
    "voice_id": "LEONARDO-AVATAR-V1",  # To be created
    "reference": "Professional, charismatic, Hollywood quality",
    "characteristics": {
        "tone": "Confident, engaging",
        "pace": "Measured, dramatic pauses",
        "emotion": "Passionate about innovation",
        "style": "Executive presenter"
    }
}
```

### Voice Cloning Process
```python
# Step 1: Prepare samples
samples = [
    "leonardo_sample1.mp3",  # Professional tone
    "leonardo_sample2.mp3",  # Enthusiastic delivery
    "leonardo_sample3.mp3"   # Confident closing
]

# Step 2: Clone voice
cloned_voice = clone_voice(
    name="LEONARDO-AVATAR-V1",
    files=samples,
    description="Executive avatar voice for intro video"
)
```

## SLIDE NARRATION SCRIPTS

### Slide 1: Hero
```text
Willkommen bei Monetec - Die Zukunft der Immobilienfinanzierung beginnt hier.
```

### Slide 2: Comparison
```text
Während traditionelle Methoden Wochen dauern, 
erledigt Monetec alles in nur 48 Stunden.
```

### Slide 3: Triptych
```text
Schnell. Sicher. Smart. 
Drei Säulen, die Ihre Finanzierung revolutionieren.
```

### Slide 4: Dashboard
```text
Über €10 Millionen bereits erfolgreich verarbeitet. 
500 Partner vertrauen unserer Technologie.
```

### Slide 5: Map
```text
Von Deutschland aus erobern wir ganz Europa. 
Ihr Erfolg kennt keine Grenzen.
```

### Slide 6: Transformation
```text
Früher: 4 Wochen Wartezeit. 
Heute: 48 Stunden bis zur Entscheidung.
```

### Slide 7: CTA
```text
Bereit für die Zukunft? 
Kontaktieren Sie uns noch heute und erleben Sie den Unterschied.
```

## GENERATION WORKFLOW

### Batch Generation Script
```python
# Generate all slide narrations
for slide_num, text in enumerate(slide_texts, 1):
    audio = generate(
        text=text,
        voice="MONETEC-VOICE-V1",
        model="eleven_multilingual_v2",
        output_format="mp3_44100_128"
    )
    
    # Save with naming convention
    filename = f"slide_{slide_num:02d}_narration_de.mp3"
    save_audio(audio, filename)
```

### Quality Control Checklist
- [ ] German pronunciation accurate
- [ ] € symbol timing correct
- [ ] Emotion appropriate per slide
- [ ] Pacing matches animations
- [ ] Audio levels consistent