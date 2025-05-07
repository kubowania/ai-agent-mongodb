# E-commerce AI Agent built with LangGraph.js and MongoDB

In this tutorial we will build an AI Agent in Express.js using LangGraph with MongoDB to build conversational apps using an agentic approach.


## What we will cover

- Introduction
- Understanding MongoDB Atlas
- Understanding LangGraph
- Managing Angetic Conversational flows
- Storing and Retreiving conversational data
- Generating human like responses with OpenAI and Anthropic's API
- Conversing with our AI Agent using a RESTful API approach.

## Prerequisites

- Install [Node.js and npm](https://nodejs.org/)

## To start this project

1. Clone this repository:

```bash
git clone https://github.com/mongodb-developer/LangGraph-MongoDB-Example.git 
cd LangGraph-MongoDB-Example
```

2. Install the required dependencies:

```bash
npm install
```

3. Set up your environment variables:
- Create a `.env` file in the root directory
- Add your API keys and MongoDB URI:

- [OpenAI API key](https://platform.openai.com/account/api-keys)
- [Anthropic API key](https://www.anthropic.com/claude)
- [MongoDB URI](https://www.mongodb.com/cloud/atlas)
  
  ```
  OPENAI_API_KEY=your_openai_api_key_here
  ANTHROPIC_API_KEY=your_anthropic_api_key_here
  MONGODB_ATLAS_URI=your_mongodb_atlas_uri_here
  ```

4. Seed the Database

Seed the database by running the following script:

```bash
npm run seed
```

5. Start the server:

```bash
npm run dev
```

6. Use the following API endpoints:

- To start a new conversation:
  ```
  curl -X POST -H "Content-Type: application/json" -d '{"message": "Your message here"}' http://localhost:3000/chat
  ```
- To continue an existing conversation:
  ```
  curl -X POST -H "Content-Type: application/json" -d '{"message": "Your follow-up message"}' http://localhost:3000/chat/{threadId}
  ```
