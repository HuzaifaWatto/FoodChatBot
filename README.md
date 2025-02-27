# FoodChatBot

FoodChatBot is an AI-powered chatbot that helps users find food recommendations and restaurant details. It is built using **FASTAPI** for the backend, **MySQL** for the database, and **Dialogflow (Google Cloud)** for the chatbot. The chatbot is connected to the backend via a **webhook** using **ngrok**.

## Features
- AI-powered chatbot for food recommendations
- Simple frontend with **HTML & CSS**
- Backend built using **FASTAPI**
- Uses **MySQL** for storing data
- Webhook integration between **FASTAPI** and **Dialogflow**
- **ngrok** used to expose the local server with HTTPS support

## Tech Stack
- **Frontend:** HTML, CSS
- **Backend:** FASTAPI (Python)
- **Database:** MySQL
- **AI Chatbot:** Dialogflow (Google Cloud)
- **ngrok:** For HTTPS tunneling

## Installation Guide

### 1. Clone the Repository
```sh
git clone https://github.com/HuzaifaWatto/FoodChatBot.git
cd FoodChatBot
```

### 2. Install Dependencies
Make sure you have Python installed, then install the required libraries:
```sh
pip install fastapi uvicorn mysql-connector-python
```

### 3. Set Up MySQL Database
- Create a new MySQL database.
- Import the provided SQL file to set up tables.
- Update the database credentials in the `main.py` file.

### 4. Start the FASTAPI Server
```sh
uvicorn main:app --reload
```

### 5. Set Up ngrok for HTTPS
Since FASTAPI runs on HTTP, use **ngrok** to create an HTTPS tunnel:
```sh
ngrok.exe http 8000
```
Copy the generated **HTTPS URL** and paste it into Dialogflow's **webhook settings**.

### 6. Connect Dialogflow Webhook
- Go to **Dialogflow Console**.
- Navigate to **Fulfillment > Webhook**.
- Paste the **ngrok HTTPS URL** and enable it.
- Save changes and test the chatbot.

## How to Use
- Start the server using **uvicorn**.
- Run **ngrok** to generate an HTTPS URL.
- Connect the chatbot with the webhook in **Dialogflow**.
- Interact with the chatbot via the frontend or directly in Dialogflow.

## Video & Blog
🎥 **YouTube Video**: [Watch Demo](https://youtu.be/kWXNNT_rNXY?si=7V0cT9LoYosMW5rW)  
📝 **Medium Blog**: [Read More](https://medium.com/@huzaifawatto/building-foodchatbot-an-ai-powered-food-recommendation-chatbot-%EF%B8%8F-b92ad578c134)

## Contributing
Feel free to fork the repository, raise issues, or submit pull requests to enhance this project.

## License
This project is licensed under the **GPL-3.0 License**. See the [LICENSE](LICENSE) file for details.

---

## 📬 Contact

For questions or suggestions, feel free to reach out:

- **Email:** huzaifawatto@gmail.com
- **LinkedIn:** [Huzaifa Watto](https://www.linkedin.com/in/huzaifawatto/)
