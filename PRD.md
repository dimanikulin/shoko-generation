# 🎉 PRD: AI Audio Congratulator

## TL;DR
A web/mobile app that turns user-input text, stories, and optional photos into personalized, high-quality audio messages for any celebratory event (birthdays, weddings, retirements, etc.). The AI voice can be fully synthetic or based on a user’s own recording, with customizable tone and style. Outputs a downloadable audio file for sharing.

---

## Problem Statement
People often want to send something more special than a text message or a generic greeting card for important moments. Writing and recording heartfelt or funny messages is hard — many people feel awkward on the mic, or don’t know what to say. This product makes it effortless by generating warm, personal audio messages using AI voices and personal details, ready to share in minutes.

---

## Goals

### Business Goals
- Capture the growing demand for AI-generated, personalized content.
- Build a lightweight, viral consumer tool that spreads via shared audio messages.
- Monetize via premium voices, advanced personalization, and longer audio messages.

### User Goals
- Quickly create something unique, personal, and high-quality for a loved one.
- Avoid the stress of writing/recording from scratch.
- Have a sharable format they can send anywhere (WhatsApp, Messenger, social media).

### Non-Goals
- Competing with live “celebrity” shoutout services like Cameo.
- Producing video content (possible future add-on, but not core v1).

---

## User Stories
1. As a user, I want to enter a person’s name, relationship, and event type so the AI can tailor the message.
2. As a user, I want to add personal stories or inside jokes so the AI message feels authentic.
3. As a user, I want to upload a photo that the AI can reference in the message (and maybe appear in the audio file cover art).
4. As a user, I want to choose from different tones (funny, heartfelt, formal) and voice styles.
5. As a user, I want to receive a downloadable MP3 file that I can share instantly.

---

## User Experience (v1 Flow)
1. **Event Selection** → Choose from a list (birthday, wedding, retirement, custom).
2. **Personalization Form** → Name, relationship, event date, personal anecdotes, inside jokes, optional photo upload.
3. **Tone & Voice Selection** → Choose voice style (e.g., warm/friendly, comedic, dramatic), gender, and accent. Option to upload a short voice sample for cloning (premium).
4. **Preview & Edit** → See AI-generated text first. Option to tweak before converting to audio.
5. **Audio Generation** → AI synthesizes speech using chosen voice parameters.
6. **Download & Share** → Receive MP3 with cover art. Instant sharing to messaging apps.

---

## Narrative
Imagine it’s your best friend’s wedding day. You’ve been busy all week, but you still want to do something special. In minutes, you open the app, choose “Wedding,” type a few stories about when they first met, and select a warm, emotional voice style. The AI crafts a heartfelt message, sprinkles in a bit of humor, and delivers a rich, natural-sounding recording — as if you’d spent hours rehearsing it. You download the MP3 and play it during the reception toast. People laugh, cry, and ask where you got it. That’s the magic this product delivers: making you the person who always sends the most memorable congratulations.

---

## Success Metrics
- **Activation Rate**: % of users who complete an audio generation after signup.
- **Share Rate**: % of audio files shared to at least one external platform.
- **Repeat Usage**: Avg. number of events a user creates messages for in a year.
- **Premium Conversion**: % of free users upgrading for premium voices/customization.
- **Viral Coefficient**: How many new users join from a shared audio file.

---

## Technical Considerations
- **Voice Synthesis**: Use existing TTS APIs (e.g., ElevenLabs, OpenAI TTS) for initial version.
- **Photo Handling**: Only used for personalization text generation and cover art — no facial recognition needed in v1.
- **Data Privacy**: Ensure secure handling of personal names/stories/photos.
- **Cross-Platform**: Web app MVP with mobile-friendly UI; later add native apps for easier sharing.
- **AI Pipeline**:
  - Input text + optional metadata → GPT model for script generation → TTS engine for audio → MP3 packaging with optional cover art.

---

## Milestones & Sequencing
1. **MVP Build (6–8 weeks)**
   - Basic form for input (event, name, story)
   - Script generation via GPT
   - Voice selection + TTS output
   - MP3 download
2. **Personalization Expansion (3–4 weeks)**
   - Photo upload for contextual references
   - Tone/style presets
   - Better cover art generator
3. **Premium Features (4–6 weeks)**
   - Voice cloning from user sample
   - Longer messages
   - Additional voice packs
4. **Viral Features (2–3 weeks)**
   - Shareable web page for each message
   - In-audio “created with…” signature for free tier
