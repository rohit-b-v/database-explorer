MCP Database Explorer
A specialized Model Context Protocol (MCP) server designed to enable Large Language Models (LLMs)—specifically optimized for Gemini Flash—to interact with, explore, and analyze structured databases.

 Overview
This project serves as a bridge between LLMs and your data. It allows AI models to programmatically discover database schemas and execute analytical queries, transforming raw data into actionable insights through the MCP standard.

Key Capabilities:
Schema Introspection: Allows LLMs to understand table structures and relationships.

Data Analysis: Enables complex analytical queries driven by natural language.

LLM Integration: Seamlessly connects with models like Gemini Flash for real-time data exploration.

Tech Stack
Language: TypeScript 100%

Protocol: Model Context Protocol (MCP)

Environment: Node.js

Installation
Clone the repository:

Bash

git clone https://github.com/rohit-b-v/database-explorer.git
cd database-explorer
Install dependencies:

Bash

npm install
Build the project:

Bash

npm run build
Configuration
To connect this server to your LLM host (such as Claude Desktop or a custom Gemini implementation), add the server to your configuration file:

JSON

{
  "mcpServers": {
    "database-explorer": {
      "command": "node",
      "args": ["/path/to/database-explorer/dist/index.js"],
      "env": {
        "DATABASE_URL": "your_database_connection_string"
      }
    }
  }
}

Project Structure
src/: Core logic for the MCP server and database connectors.

tsconfig.json: TypeScript configuration for the project.

package.json: Project metadata and dependency management.

Screeenshots:

<img width="436" height="699" alt="image" src="https://github.com/user-attachments/assets/e56c78f8-e919-4010-b167-e15f0524b564" />
