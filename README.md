![](./mcp-icon-light.png)

# Model Context Protocol (sse) servers

This repository is a collection of *reference implementations* for the [Model Context Protocol](https://modelcontextprotocol.io/) (MCP) with SSE, as well as references to community built servers and additional resources.

For many enterpises, it's no way to have each employees to connect to AI Tools without control and governance, it's critical to have these MCP tools with remote connect capabilities (sse) and allow enterprise to create a reliable and responsible environemnt to run AI realted usecases.

All the MCP servers listed in this repository showcase the versatility and extensibility of MCP, demonstrating how it can be used to give Large Language Models (LLMs) secure, controlled access to tools and data sources.

Each MCP server is implemented with either the [Typescript MCP SDK](https://github.com/modelcontextprotocol/typescript-sdk) or [Python MCP SDK](https://github.com/modelcontextprotocol/python-sdk).

> Note: Lists in this README are maintained in alphabetical order to minimize merge conflicts when adding new items.

## MCP Spec

There are two mcp spec released at 2025 Mar/30, let's quick compare the differnece of these two specs:

- [2025-03-26 (Latest)](https://spec.modelcontextprotocol.io/specification/2025-03-26/)
- [2024-11-05 (Final)](https://spec.modelcontextprotocol.io/specification/2024-11-05/)


To organize the differences clearly, the following table encapsulates the comparison:

| Feature/Aspect          | Description                                                                 | 2024-11-05 (Final)  | 2025-03-26 (Latest) |
|------------------------|-----------------------------------------------------------------------------|------------------|------------------|
| Authorization Framework | A system to manage and control access to MCP servers, ensuring that only authorized users or applications can interact with them. | No specific framework mentioned; general guidelines for user consent. | Added a comprehensive framework based on Oatuh 2.1 for standardized authorization processes. |
| Transport Layer         | The method used for data transmission between clients and servers.          | HTTP with Server-Sent Events (HTTP+SSE) | Replaced with Streamable HTTP, which likely offers more flexibility or improved performance. |
| JSON-RPC Batching       | The ability to send multiple JSON-RPC requests in a single message, which can improve efficiency by reducing network overhead. | Not supported | Supported, allowing for batch processing of requests. |
| Tool Annotations        | Descriptive labels or metadata for tools that indicate their behavior, such as whether they are read-only or can perform destructive operations. | Not mentioned | Added to provide better understanding and control over tool usage. |
| ProgressNotification   | Notifications that inform about the progress of ongoing operations.        | Did not have a `message` field | Added a `message` field to provide descriptive status updates, enhancing user experience and debugging. |
| Data Support            | The types of data that the protocol can handle and transmit.               | Text and Image   | Added support for Audio data, expanding the range of content types that can be managed. |
| Completions Capability  | A feature that allows for providing suggestions or completions for arguments in requests, which can be useful for user interfaces or to assist in constructing requests. | Not explicitly mentioned | Added to support argument autocompletion, likely improving usability and efficiency. |

### Implications and Observations

The updates from 2024-11-05 to 2025-03-26 indicate a focus on enhancing security, flexibility, and usability. 

The addition of an **OAuth 2.1-based authorization framework** and **Streamable HTTP transport** suggests a move toward more robust and scalable implementations. 

The inclusion of audio data support and tool annotations could significantly expand MCP’s applicability, particularly in multimedia and complex AI workflows. 

The unexpected detail of audio support, not previously highlighted, may indicate a shift toward more versatile AI interactions, potentially impacting industries like voice assistants or multimedia content analysis.

## 🌟 Reference Servers

These servers aim to demonstrate MCP features and the TypeScript and Python SDKs.



