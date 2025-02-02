# 🧙♂️ Kitchen Alchemist - AI Recipe Generator

![Kitchen Alchemist Banner](assets/banner.png) 

---

Transform your pantry ingredients into delicious recipes with AI magic! This Streamlit application powered by Groq's LLM API generates creative cooking ideas based on available ingredients and dietary preferences.

## 🚀 Features
- **AI-Powered Recipe Generation** (Using Llama-3-70B model)
- Dietary Preference Filters (Vegetarian, Vegan, Gluten-Free, etc.)
- Real-time Recipe Generation
- Docker Container Support
- Responsive Web Interface
- Pantry Staples Detection

## 📦 Prerequisites
- Docker installed
- Python 3.9+
- Groq API Key (Free tier available)
- Modern web browser

## 🛠️ Installation

### 1. Clone Repository
```bash
git clone https://github.com/We4TechAI/Kitchen-Alchemist.git
cd Kitchen-Alchemist
```

### 2. Configure API Key
Create `.streamlit/secrets.toml` file:
```toml
GROQ = "your-api-key-here"
```

### 3. Build & Run with Docker
```bash
docker build --tag kitchen_alchemist:latest .
docker run -d --name kitchen_alchemist -p 8501:8501 kitchen_alchemist:latest
```

## 🌐 Access the Application
Visit in your browser:  
http://localhost:8501

## ⚙️ Configuration
| Environment Variable | Description                     | Default               |
|-----------------------|---------------------------------|-----------------------|
| `GROQ_API_KEY`        | Groq API Key                    | Required              |
| `MODEL_NAME`          | LLM Model to use                | llama3-70b-8192       |
| `TEMPERATURE`         | AI Creativity level (0-1)       | 0.7                   |

## 🍳 Usage Example
1. Enter ingredients: "chicken, broccoli, rice, garlic"
2. Select dietary preference: "Low-Carb"
3. Click "Generate Recipe"

**Sample Output:**
```
🍗 Garlic Chicken & Broccoli Bowl

Ingredients:
- 2 chicken breasts (diced)
- 1 cup broccoli florets
- 3 garlic cloves (minced)
- 1 tbsp olive oil
- 1/2 cup cauliflower rice
- 1 tsp paprika

Instructions:
1. Heat oil in pan, sauté garlic until fragrant
2. Add chicken and cook until browned
3. Stir in broccoli and paprika
4. Serve over cauliflower rice
```

## 📚 API Reference
The application uses Groq's API with the following parameters:
```python
{
    "model": "llama3-70b-8192",
    "temperature": 0.7,
    "max_tokens": 1024,
    "top_p": 1,
    "stop": None
}
```


## 🤝 Contributing
1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License
Distributed under the MIT License. See `LICENSE` for more information.

## 🙏 Acknowledgments
- Groq for their blazing-fast LLM API
- Streamlit for the web framework
- Meta for the Llama-3 model
- All open-source contributors

---

**Note:** This application may incur costs through Groq API usage. Monitor your usage through the Groq console.
```

