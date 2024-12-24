## **THP AI API Core** ▵

[![GitHub license](https://img.shields.io/badge/license-MIT-blue)](#license)
[![TypeScript](https://img.shields.io/badge/TypeScript-4.x-blue)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-16.x-green)](https://nodejs.org/)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen)](#contributors)

> 🚦 This project is experimental and still under development. Please be patient while we get it ready for production.

An internal deployable service for The Hackers Playbook's clients, partners and internal use to interface with the [Vercel AI SDK Core](https://vercel.com/docs/ai). This service is designed for **The Hackers Playbook (THP)** to simplify the use of the SDK across various languages and platforms via a network-accessible API.

This project is built for internal use at The Hackers Playbook but we're open to discussing a partnership with **Vercel** to improve adoption and extend its utility.

---

![Lady Cyborg](https://img.freepik.com/premium-photo/futuristic-cyborg-silhouette-with-headphones-minimalist-digital_38013-84634.jpg)

> 🚨 **Disclaimer**: This service was built independently and is **not affiliated with or endorsed by Vercel**. Its use should comply with all applicable terms and conditions of the Vercel AI SDK.

---

### **Purpose** ⭐️

Vercel AI SDK Core is an excellent tool for interacting with large language models (LLMs). While it natively supports **TypeScript**, integrating it into projects in other languages can be complex.

The **AI SDK Core Service** provides:

- A **language-agnostic** interface for the Vercel AI SDK.
- **Network accessibility** via REST API for easy integration across projects and apps.
- **Self-hosted** with simplified deployment using **Docker**.

#### **On the Idea** 💡

> We felt that building this service to abstract the SDK and make it language-agnostic is a **great idea** for internal use, especially for teams relying heavily on the SDK.

---

### **Features** ☀️

- 🧠 **Unified API** for Vercel AI SDK Core functions like `generateText`, `streamText`, `generateObject`, and `streamObject`.
- 🔩 **Robust Tool Calling Framework**: Includes a robust tool-calling framework for orchestrating agentic actions over the network.
- 🛠️ **Deployable with Docker**, ensuring consistency across environments.
- ⚡ Built with **NestJS (Fastify)** for efficient and scalable performance.
- 🔒 **Internal Use Only**: Not an official Vercel service. However, it adheres to Vercel's technical standards to ensure compatibility.
- 🛡️ **Test Driven Development (TDD)**: Developed with TDD to ensure high quality standards.
- 📜 **Open Design & Architecture Documentation**: We Open Sourced our Architecture & Design documents to encourage people to build in open.
- 📭 **Postman Collection**: Executable Documentation is always great, download the collection here.

---

### **Tech Stack** 🧳

- **NestJS (Fastify)**: Provides a scalable, modular framework for the API layer.
- **Docker**: Facilitates quick deployment and reproducibility across environments.
- **Vercel AI SDK Core**: Backend integration with powerful AI tools.

---

### **Installation** ▶️

1. Clone the repository:

   ```bash
   git clone https://github.com/TheHackersPlaybook/ai-sdk-core-service.git
   cd ai-sdk-core-service
   ```

2. Build and run the service with Docker:

   ```bash
   docker build -t ai-sdk-core-service .
   docker run -p 3000:3000 ai-sdk-core-service
   ```

3. Access the API:
   - Default endpoint: `http://localhost:3000`

---

### **Usage** 🚀

#### **Example API Call**

To generate text using the OpenAI GPT-4 model:

```bash
curl -X POST http://localhost:3000/generate-text \
  -H "Content-Type: application/json" \
  -d '{
    "model": "openai:gpt-4-turbo",
    "prompt": "What is love?"
  }'
```

#### **Expected Response**

```json
{
  "text": "Love is a complex and multifaceted emotion that involves affection, care, and connection..."
}
```

#### **Endpoints** 🔌

| Endpoint           | Description                                        |
| ------------------ | -------------------------------------------------- |
| `/generate-text`   | Generate text and tool calls.                      |
| `/stream-text`     | Stream text and tool calls.                        |
| `/generate-object` | Generate structured objects matching a Zod schema. |
| `/stream-object`   | Stream structured objects matching a Zod schema.   |

Refer to the API documentation in the repository for detailed usage instructions.

---

### **Limitations** 🙅🏼

- ❗ **Unofficial Service**: This is not endorsed or maintained by Vercel.
- 🚧 **Internal Use Only**: Designed for THP use but can be customized.
- ⚠️ Ensure compliance with Vercel's [Terms of Service](https://vercel.com/legal/terms).

---

### **License** 🧑🏼‍⚖️

This service is licensed under the **MIT License**. See `LICENSE` for details.

---

### **Contact** 📲

For inquiries, contributions, or partnership discussions with Vercel:  
📧 Email: [contact@hackersplaybook.io](mailto:contact@hackersplaybook.io)  
🌐 Website: [The Hackers Playbook](https://hackersplaybook.io)

---

> _"Don't wait for the right time; the right time is now."_  
> — Anonymous
