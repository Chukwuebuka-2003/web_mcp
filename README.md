# WebMCP Project


[![Ask DeepWiki](https://deepwiki.com/badge.svg)](https://deepwiki.com/Chukwuebuka-2003/web_mcp)

<img width="679" height="382" alt="image" src="https://github.com/user-attachments/assets/6a050161-e5eb-40b7-acf3-eeee4533d37a" />

## Description

WebMCP (Model Context Protocol for the Web) is a project that aims to empower web applications by allowing them to expose their functionality as "tools" that can be accessed by AI agents and other assistive technologies. It provides a JavaScript-based interface that enables developers to create collaborative, human-in-the-loop workflows where users and AI agents can work together within the same web interface.

This project allows websites to act as MCP servers, sharing tools, resources, and prompts with client-side Large Language Models (LLMs). This enables a seamless integration of AI capabilities into existing web applications, leveraging their current business logic and user interfaces.

## Core Concepts

  * **Tools:** Web pages can define JavaScript functions with natural language descriptions and structured schemas. These tools can be invoked by AI agents to perform specific actions on the page.
  * **Client-Side Execution:** Unlike backend integrations, WebMCP tools are available once a page is loaded and are executed on the client-side.
  * **Shared Context:** WebMCP facilitates a shared context between the user, the web page, and the AI agent, allowing for a more cooperative and interactive experience.
  * **Preservation of User Interface:** It augments rather than replaces the existing user interface, allowing developers to maintain their branding and user experience.

## Features

  * **One-Click Activation:** Easily enable native MCP support in your browser.
  * **No Complex Setups:** Eliminates the need for complex configurations.
  * **Preserves Login Sessions:** Works with existing user login sessions at no migration cost.
  * **Dual-Mode Connectivity:** Supports both remote and local proxy switching.
  * **Plug-and-Play MCP Service:** Instantly activate MCP for your browser.

## Technologies Used

This project is primarily built with the following technologies:

  * **JavaScript / TypeScript**
  * **HTML**
  * **CSS**

## Getting Started

To get started with adding WebMCP to your website, follow these steps:

### Prerequisites

Make sure you have a modern web browser and a basic understanding of JavaScript.

### Installation

1.  **Include the WebMCP script:** Add the `webmcp.js` script to your HTML file. You can either host it yourself or link to it if it's available from a CDN.

    ```html
    <script src="webmcp.js"></script>
    ```

2.  **Define your tools:** In your website's JavaScript, define the tools you want to expose to AI agents using the WebMCP API.

    ```javascript
    // Example of defining a tool
    webmcp.tool("search", "Searches the website for a given query", {
        "query": {
            "type": "string",
            "description": "The search term"
        }
    }, async (params) => {
        // Your existing search functionality
        const results = await performSearch(params.query);
        return {
            "content": [
                {
                    "type": "text",
                    "text": JSON.stringify(results),
                },
            ],
        };
    });
    ```

## Usage

Once you have installed and configured WebMCP on your website, users with a compatible MCP client or browser extension can interact with your defined tools. When a user visits your website, the WebMCP widget will appear, allowing them to connect their AI agent to your site.

The AI agent can then see the available tools and call them to perform actions, such as filling out forms, searching for information, or navigating the site.

## License

This project is licensed under the MIT License. See the `LICENSE` file for more details.

-----

For a deeper dive into MCP, check out this video: [Ultimate MCP Crash Course](https://www.youtube.com/watch?v=ZoZxQwp1PiM)