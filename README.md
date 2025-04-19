# Symptom-Based Medicine Recommendation Chatbot

## Overview
This chatbot is an AI-driven tool that allows users to input their symptoms and receive **personalized medicine suggestions with proper dosages**. Integrated with WhatsApp, it ensures convenient access and enhances user engagement with intuitive interactions.

## Features
- **Symptom Analysis:** Users provide symptoms, and the chatbot suggests relevant medicines.
- **Dosage Information:** Provides detailed dosage instructions for each suggested medicine.
- **WhatsApp Integration:** Seamlessly communicates with users through WhatsApp for real-time interaction.
- **Multi-Step Conversations:** Supports follow-up questions for precise symptom evaluation.
- **User Data Privacy:** Prioritizes confidentiality and complies with data protection standards.

## Technologies Used
- **Frontend:** User interactions via WhatsApp (Twilio API)
- **Backend:** Python (Flask/FastAPI)
- **AI Integration:** Google Generative AI (Gemini API) for intelligent responses
- **Database:** Firebase or SQLite for storing user interactions and recommendations
- **Deployment:** AWS/GCP/Azure with Docker for scalability and reliability

## Installation & Setup

### Prerequisites:
- Python 3.8 or above
- Twilio WhatsApp Business Account
- Google API Key for Generative AI

### Steps:
1. **Clone the Repository:**
   ```bash
   git clone https://github.com/your-repo/medicine-chatbot.git
   cd medicine-chatbot
   ```

2. **Install Dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Set Environment Variables:**
   Create a `.env` file to store your API keys and credentials:
   ```plaintext
   GOOGLE_API_KEY=your_google_api_key
   TWILIO_ACCOUNT_SID=your_account_sid
   TWILIO_AUTH_TOKEN=your_auth_token
   TWILIO_WHATSAPP_NUMBER=whatsapp:+14155238886
   ```

4. **Run the Server:**
   ```bash
   python3 uvicorn main:app --reload
   ```

5. **Connect with WhatsApp:**
   - Configure the Twilio webhook in your Twilio Console to point to `/whatsapp` endpoint of your server.

## Usage
1. **Start a WhatsApp Conversation:**
   - Message your Twilio WhatsApp number with symptoms.
2. **Receive Medicine Suggestions:**
   - The chatbot will analyze your symptoms and provide:
     - Suggested medicines
     - Accurate dosage information
     - Additional recommendations (e.g., precautions, side effects)
3. **Follow Up:**
   - Chatbot supports follow-up queries for symptom refinement or additional questions.

## Limitations
- **Not a Replacement for Doctors:** The suggestions are informational and should not replace professional medical advice.
- **Data Accuracy:** Recommendations are based on input data; incorrect symptoms might lead to irrelevant suggestions.

## Future Enhancements
- **Multi-Language Support:** Incorporate diverse language options.
- **Risk Assessment:** Integrate advanced AI models for predicting health risks.
- **Appointment Scheduling:** Allow users to book appointments with medical professionals.

## License
This project is open-source and available under the MIT License.
