# Ollama Spring Boot AI Implementation

## 📌 Project Overview
This project integrates **Spring Boot** with **Ollama AI models** to provide AI-powered responses using **Spring AI** and **Flux**. It enables synchronous and streaming AI responses with models like **DeepSeek R1**.

## 🚀 Features
- **Ask AI**: Send a query and receive an AI-generated response.
- **Streaming AI Response**: Get responses in chunks using Flux for improved speed and interactivity.
- **Integration with Ollama AI**: Supports various AI models from Ollama, including **DeepSeek R1**.
- **Reactive Programming**: Utilizes Spring WebFlux for handling real-time data streams efficiently.


## 🛠️ Prerequisites
Ensure you have the following installed on your machine:
- **Java 17+**
- **Maven 3+**
- **Docker (Optional, for running Ollama AI in containers)**
- **Ollama AI** (Installation steps below)

## 🔥 Installation Guide
### 1️⃣ Install Ollama AI
Ollama AI provides local AI models to power this application. Install it using:
```bash
curl -fsSL https://ollama.com/install.sh | sh
```

### 2️⃣ Pull DeepSeek R1 Model
You can download the DeepSeek R1 model using the following command:
```bash
ollama pull deepseek-r1
```

For more details, visit: [DeepSeek R1 on Ollama](https://ollama.com/library/deepseek-r1)

### 3️⃣ Clone This Repository
```bash
https://github.com/Hugs-4-Bugs/Ollama-Spring-Boot-AI-Implementation.git
cd ollama-spring-ai
```

### 4️⃣ Run the Application
#### Using Maven
```bash
./mvnw spring-boot:run
```
#### Using Docker (Optional)
Build and run the app inside a container:
```bash
docker build -t ollama-ai .
docker run -p 8180:8180 ollama-ai
```

### 5️⃣ Test the Endpoints
#### Sync AI Response
```bash
curl -G --data-urlencode "query=What is AI?" "http://localhost:8180/api/v1/ai"
```
#### Streaming AI Response
```bash
curl -G --data-urlencode "query=Tell me a story." "http://localhost:8180/api/v1/ai/stream"
```

## 📜 API Endpoints
| Method | Endpoint | Description |
|--------|------------|--------------------------|
| GET | `/api/v1/ai?query=your_query` | Get AI-generated response |
| GET | `/api/v1/ai/stream?query=your_query` | Get streamed AI response |

## 🛠 Technologies Used
- **Spring Boot** – Backend framework
- **Spring AI** – AI integration
- **Spring WebFlux** – Reactive programming
- **Ollama AI** – Local AI model execution

## 📌 Future Enhancements
- Support for multiple AI models
- Caching responses for performance optimization
- Frontend integration

## Snapshots
<img width="1440" alt="Screenshot 2025-02-01 at 6 15 59 PM" src="https://github.com/user-attachments/assets/1b65f2f5-c7df-49d8-919a-909ffffc4fa2" />

<img width="1440" alt="Screenshot 2025-02-01 at 6 22 30 PM" src="https://github.com/user-attachments/assets/5dfdb67d-d013-443e-8241-537f197b9063" />


## 🤝 Contribution
Feel free to submit issues or create pull requests. Contributions are welcome!

## 📄 License
This project is licensed under the **MIT License**.

Happy Coding! 🚀

