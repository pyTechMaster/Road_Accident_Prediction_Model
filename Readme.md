🚗💥 Road Accident Prediction System

AI-powered accident risk prediction for safer roads 🛡️✨

🌟 What This Does

This system predicts road accident risks using advanced AI models trained on real UK government data 🇬🇧.
Simply provide GPS coordinates 📍 and get instant risk assessments ⚡!

🚀 Quick Start
1️⃣ Clone the Project
git clone https://github.com/SangramKhandagale/Road_Accident_Prediction_Model
cd Road_Accident_Prediction_Model

2️⃣ Setup Virtual Environment (VS Code Only 💻)

Windows

python -m venv venv
venv\Scripts\activate


Mac/Linux

python3 -m venv venv
source venv/bin/activate


💡 Note: If using GitHub Codespaces, skip this step 🚫

3️⃣ Install Dependencies 📦
pip install -r requirements.txt

4️⃣ Run the Application ▶️
python app.py


🎉 Your app is now running at:
👉 http://localhost:5000
 🌐

📁 Project Structure
ACCIDENT-PREDICTION/
├── app/                 # 🐍 Core Flask app
├── models/              # 🤖 Trained AI models
├── static/              # 🎨 CSS, JS, images
├── templates/           # 📄 HTML templates
├── app.py               # 🚀 Main application
├── config.py            # ⚙️ Configurations
└── requirements.txt     # 📦 Dependencies

🔧 Configuration

Create a .env file (optional 📝):

FLASK_ENV=development
DEBUG=True
PORT=5000


✅ Make sure /models/ contains:

📊 best_accident_model.pkl – Main AI model

⚖️ feature_scaler.pkl – Data preprocessor

📝 feature_names.pkl – Feature definitions

🌐 API Endpoints
🎯 Single Prediction
POST /api/predict
Content-Type: application/json

{
  "latitude": 51.5074,
  "longitude": -0.1278
}

📦 Batch Predictions
POST /api/batch_predict
Content-Type: application/json

{
  "locations": [
    {"lat": 51.5074, "lon": -0.1278},
    {"lat": 52.5200, "lon": 13.4050}
  ]
}

❤️ Health Check
GET /api/health

🎨 Using the Web Interface

🌍 Homepage → http://localhost:5000

📍 Enter Location → Use map or type coordinates

🔮 Predict Risk → Click "Predict Risk"

📊 View Results → See risk level & confidence

🛠️ Development
Run in Development Mode 🐣
export FLASK_ENV=development
python app.py

Test API with curl 💻
# Single prediction
curl -X POST http://localhost:5000/api/predict \
  -H "Content-Type: application/json" \
  -d '{"latitude": 51.5074, "longitude": -0.1278}'

# Health check
curl http://localhost:5000/api/health

📊 Model Information

🎯 Accuracy: ~75–85%

🤖 Algorithm: XGBoost + LightGBM + CatBoost ensemble

📈 Data: 130,000+ UK accident records

🏷️ Output: 3 risk levels (Low, Medium, High)

🚨 Risk Levels
Level	🎨 Color	Description
🟢 Low	Green	Relatively safe area
🟡 Med	Yellow	Moderate risk, stay alert
🔴 High	Red	High risk, extra caution
🔧 Troubleshooting

❌ Model files not found → check models/ folder

❌ Import errors → run pip install -r requirements.txt

❌ Port in use → change port in .env or config.py

❌ Accuracy issues → normal for real-world predictions ✅

📦 Dependencies

🌐 Flask – Web framework

🤖 scikit-learn, XGBoost, LightGBM, CatBoost – AI models

📊 pandas, numpy – Data handling

🎨 matplotlib, seaborn – Visualization

📞 Support

📖 Read this README carefully

🔍 Review docs for examples

🧪 Test APIs

🛠️ Check logs for errors

📄 License

This project is proprietary software developed for accident prediction purposes.

🎉 Ready to predict accidents with AI! 🚗💨💡

Last Updated: September 2025