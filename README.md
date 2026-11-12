# Hello MCP

A small Python Model Context Protocol (MCP) server built with FastMCP. It exposes two tools:

- `get_greeting(name)` returns a personalized greeting.
- `add_numbers(a, b)` returns the sum of two integers.

## Requirements

- Python 3.10 or later
- Visual Studio Code with MCP support (to use the workspace server configuration)

## Setup

From the project directory, create and activate a virtual environment, then install the dependencies:

```powershell
python -m venv venv
.\venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

The VS Code MCP configuration at `.vscode/mcp.json` uses `venv\Scripts\python.exe`, so install the requirements into that virtual environment.

## Use in VS Code

Open this folder in VS Code. The server is configured as `helloMcp` and starts by running `server.py` over stdio. Approve or start the server when prompted by VS Code, then invoke its tools from MCP-enabled chat.

Examples:

- `get_greeting` with `name` set to `"Gayathri"` returns `Hello, Gayathri! Your first MCP tool works.`
- `add_numbers` with `a` set to `25` and `b` set to `35` returns `60`.

## Run manually

To start the server from PowerShell:

```powershell
.\venv\Scripts\python.exe .\server.py
```

The server uses the MCP stdio transport; it is intended to be launched by an MCP client.
