<p align='center'>
<img src='./build/icon.png' width="150" height="150" alt="AgentConnector AI Assistant Icon" />
</p>

<h1 align="center">AgentConnector - Powerful Open-Source Multi-Model Agent Network Client</h1>

<p align="center">AgentConnector is a feature-rich open-source Agent Network Client built upon DeepChat, supporting multiple cloud and local large language models with powerful search enhancement and tool calling capabilities.</p>

<div align="center">
  <a href="./README.zh.md">中文</a> / <a href="./README.md">English</a>
</div>

## 📑 Table of Contents

- [📑 Table of Contents](#-table-of-contents)
- [🚀 Project Introduction](#-project-introduction)
- [💡 Why Choose AgentConnector](#-why-choose-AgentConnector)
- [🔥 Main Features](#-main-features)
- [🤖 Supported Model Providers](#-supported-model-providers)
  - [Compatible with any model provider in OpenAI/Gemini/Anthropic API format](#compatible-with-any-model-provider-in-openaigeminianthropic-api-format)
- [🔍 Use Cases](#-use-cases)
- [📦 Quick Start](#-quick-start)
  - [Download and Install](#download-and-install)
  - [Configure Models](#configure-models)
  - [Start Conversations](#start-conversations)
- [💻 Development Guide](#-development-guide)
  - [Install Dependencies](#install-dependencies)
  - [Start Development](#start-development)
  - [Build](#build)
- [👥 Community \& Contribution](#-community--contribution)
- [🙏🏻 Thanks](#-Thanks)
- [📃 License](#-license)

## 🚀 Project Introduction

AgentConnector is a powerful, open-source Agent network client that delivers a unified interface for interacting with a wide range of large language models. Whether you're leveraging cloud APIs such as OpenAI, Gemini, and Anthropic, or running local models via Ollama, AgentConnector ensures a seamless and consistent user experience across all endpoints.

As a cross-platform application, it goes beyond basic conversational AI by integrating advanced capabilities—including search augmentation, tool calling, and multimodal interaction—to make sophisticated AI functionalities more accessible and practical for everyday use.

## 💡 Why Choose AgentConnector

Compared to other AI tools, AgentConnector offers the following unique advantages:

- **Comprehensive Feature Inheritance from DeepChat**: Built upon the robust DeepChat framework, AgentConnector inherits all its powerful chat capabilities and user experience advantages, providing a mature and stable interaction foundation out of the box.
- **Seamless Integration with AgentDNS Ecosystem**: Natively designed to connect with the AgentDNS system, it enables automatic discovery and dynamic routing to the most suitable intelligent services, achieving true "agent-level" interconnection and collaboration.
- **Advanced Tool Calling with Built-in MCP Support**: Integrated with the Model Context Protocol, it supports code execution, web access, and a variety of extensible tools without requiring complex configurations.
- **Flexible and Powerful Search Augmentation**: upports multiple search engines and offers customizable search paradigms, significantly enhancing the accuracy and timeliness of AI responses.
- **Privacy-First Design**: With local data storage and network proxy support, it effectively reduces the risk of data leakage and safeguards user privacy.
- **Business-Friendly Open Source Licensing**: Released under the Apache 2.0 License, it is free for both commercial and personal use, providing maximum flexibility.

## 🔥 Main Features

- **Deep Integration with AgentDNS**: Dynamically connects to the agent network, enabling automatic service discovery, intelligent routing, and unified scheduling.

By fully inheriting the core chat functionalities from DeepChat, AgentConnector stands on the shoulders of a giant. This strategic foundation allows us to avoid reinventing the wheel and instead focus our development energy on pioneering advanced features like AgentDNS integration and enhanced tool calling, delivering greater value to our users.
- 🌐 **Multiple Cloud LLM Provider Support**: DeepSeek, OpenAI, SiliconFlow, Grok, Gemini, Anthropic, and more
- 🏠 **Local Model Deployment Support**:
  - Integrated Ollama with comprehensive management capabilities
  - Control and manage Ollama model downloads, deployments, and runs without command-line operations
- 🚀 **Rich and Easy-to-Use Chat Capabilities**
  - Complete Markdown rendering with code block rendering based on industry-leading
  - Multi-window + multi-tab architecture supporting parallel multi-session operations across all dimensions, use large models like using a browser, non-blocking experience brings excellent efficiency
  - Supports Artifacts rendering for diverse result presentation, significantly saving token consumption after MCP integration
  - Messages support retry to generate multiple variations; conversations can be forked freely, ensuring there's always a suitable line of thought
  - Supports rendering images, Mermaid diagrams, and other multi-modal content; supports GPT-4o, Gemini, Grok text-to-image capabilities
  - Supports highlighting external information sources like search results within the content
- 🔍 **Robust Search Extension Capabilities**
  - Built-in integration with leading search APIs like BoSearch, Brave Search via MCP mode, allowing the model to intelligently decide when to search
  - Supports mainstream search engines like Google, Bing, Baidu, and Sogou Official Accounts search by simulating user web browsing, enabling the LLM to read search engines like a human
  - Supports reading any search engine; simply configure a search assistant model to connect various search sources, whether internal networks, API-less engines, or vertical domain search engines, as information sources for the model
- 🔧 **Excellent MCP (Model Context Protocol) Support**
  - Complete support for the three core capabilities of Resources/Prompts/Tools in the MCP protocol
  - Supports semantic workflows, enabling more complex and intelligent automation by understanding the meaning and context of tasks.
  - Extremely user-friendly configuration interface
  - Aesthetically pleasing and clear tool call display
  - Detailed tool call debugging window with automatic formatting of tool parameters and return data
  - Built-in Node.js runtime environment; npx/node-like services require no extra configuration and work out-of-the-box
  - Supports StreamableHTTP/SSE/Stdio protocol Transports
  - Supports inMemory services with built-in utilities like code execution, web information retrieval, and file operations; ready for most common use cases out-of-the-box without secondary installation
  - Converts visual model capabilities into universally usable functions for any model via the built-in MCP service
- 💻 **Multi-Platform Support**: Windows, macOS, Linux
- 🎨 **Beautiful and User-Friendly Interface**, user-oriented design, meticulously themed light and dark modes
- 🔗 **Rich DeepLink Support**: Initiate conversations via links for seamless integration with other applications. Also supports one-click installation of MCP services for simplicity and speed
- 🚑 **Security-First Design**: Chat data and configuration data have reserved encryption interfaces and code obfuscation capabilities
- 🛡️ **Privacy Protection**: Supports screen projection hiding, network proxies, and other privacy protection methods to reduce the risk of information leakage
- 💰 **Business-Friendly**:
  - Embraces open source, based on the Apache License 2.0 protocol, enterprise use without worry
  - Enterprise integration requires only minimal configuration code changes to use reserved encrypted obfuscation security capabilities
  - Clear code structure, both model providers and MCP services are highly decoupled, can be freely customized with minimal cost
  - Reasonable architecture, data interaction and UI behavior separation, fully utilizing Electron's capabilities, rejecting simple web wrappers, excellent performance


## 🤖 Supported Model Providers

<table>
  <tr align="center">
    <td>
      <img src="./src/renderer/src/assets/llm-icons/ollama.svg" width="50" height="50" alt="Ollama Icon"><br/>
      <a href="https://ollama.com">Ollama</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/deepseek-color.svg" width="50" height="50" alt="Deepseek Icon"><br/>
      <a href="https://deepseek.com/">Deepseek</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/ppio-color.svg" width="50" height="50" alt="PPIO Icon"><br/>
      <a href="https://ppinfra.com/">PPIO</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/alibabacloud-color.svg" width="50" height="50" alt="DashScope Icon"><br/>
      <a href="https://www.aliyun.com/product/bailian">DashScope</a>
    </td>
  </tr>
  <tr align="center">
    <td>
      <img src="./src/renderer/src/assets/llm-icons/doubao-color.svg" width="50" height="50" alt="Doubao Icon"><br/>
      <a href="https://console.volcengine.com/ark/">Doubao</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/minimax-color.svg" width="50" height="50" alt="MiniMax Icon"><br/>
      <a href="https://platform.minimaxi.com/">MiniMax</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/fireworks-color.svg" width="50" height="50" alt="Fireworks Icon"><br/>
      <a href="https://fireworks.ai/">Fireworks</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/302ai.svg" width="50" height="50" alt="302.AI Icon"><br/>
      <a href="https://302.ai/">302.AI</a>
    </td>
  </tr>
  <tr align="center">
    <td>
      <img src="./src/renderer/src/assets/llm-icons/openai.svg" width="50" height="50" alt="OpenAI Icon"><br/>
      <a href="https://openai.com/">OpenAI</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/gemini-color.svg" width="50" height="50" alt="Gemini Icon"><br/>
      <a href="https://gemini.google.com/">Gemini</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/github.svg" width="50" height="50" alt="GitHub Models Icon"><br/>
      <a href="https://github.com/marketplace/models">GitHub Models</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/moonshot.svg" width="50" height="50" alt="Moonshot Icon"><br/>
      <a href="https://moonshot.ai/">Moonshot</a>
    </td>
  </tr>
  <tr align="center">
    <td>
      <img src="./src/renderer/src/assets/llm-icons/openrouter.svg" width="50" height="50" alt="OpenRouter Icon"><br/>
      <a href="https://openrouter.ai/">OpenRouter</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/azure-color.svg" width="50" height="50" alt="Azure OpenAI Icon"><br/>
      <a href="https://azure.microsoft.com/en-us/products/ai-services/openai-service">Azure OpenAI</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/qiniu.svg" width="50" height="50" alt="Qiniu Icon"><br/>
      <a href="https://www.qiniu.com/products/ai-token-api">Qiniu</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/grok.svg" width="50" height="50" alt="Grok Icon"><br/>
      <a href="https://x.ai/">Grok</a>
    </td>
  </tr>
  <tr align="center">
    <td>
      <img src="./src/renderer/src/assets/llm-icons/zhipu-color.svg" width="50" height="50" alt="Zhipu Icon"><br/>
      <a href="https://open.bigmodel.cn/">Zhipu</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/siliconcloud.svg" width="50" height="50" alt="SiliconFlow Icon"><br/>
      <a href="https://www.siliconflow.cn/">SiliconFlow</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/aihubmix.png" width="50" height="50" alt="AIHubMix Icon"><br/>
      <a href="https://aihubmix.com/">AIHubMix</a>
    </td>
    <td>
      <img src="./src/renderer/src/assets/llm-icons/hunyuan-color.svg" width="50" height="50" alt="Hunyuan Icon"><br/>
      <a href="https://cloud.tencent.com/product/hunyuan">Hunyuan</a>
    </td>
  </tr>
  <tr align="center">
    <td>
      <img src="./src/renderer/src/assets/llm-icons/lmstudio.svg" width="50" height="50" alt="LM Studio Icon"><br/>
      <a href="https://lmstudio.ai/">LM Studio</a>
    </td>
    <td></td>
    <td></td>
    <td></td>
  </tr>

</table>

### Compatible with any model provider in OpenAI/Gemini/Anthropic API format

## 🔍 Use Cases

AgentConnector is suitable for various AI application scenarios:

- **Daily Assistant**: Answering questions, providing suggestions, assisting with writing and creation
- **Development Aid**: Code generation, debugging, technical problem solving
- **Learning Tool**: Concept explanation, knowledge exploration, learning guidance
- **Content Creation**: Copywriting, creative inspiration, content optimization
- **Data Analysis**: Data interpretation, chart generation, report writing

## 📦 Quick Start

### Download and Install

Download the latest version for your system from the [GitHub Releases](https://github.com/jsjfai/releases) page:

- Windows: `.exe` installation file
- macOS: `.dmg` installation file

### Configure Models

1. Launch the AgentConnctor application
2. Click the settings icon
3. Select the "Model Providers" tab
4. Add your API keys or configure local Ollama

### Start Conversations

1. Click the "+" button to create a new conversation
2. Select the model you want to use
3. Start communicating with your AI assistant

For a comprehensive guide on getting started and using all features, please refer to the [User Guide](./docs/user-guide.md).

## 💻 Development Guide
### Install Dependencies

```bash
$ pnpm install
$ pnpm run installRuntime
# if got err: No module named 'distutils'
$ pip install setuptools
```

* For Windows: To allow non-admin users to create symlinks and hardlinks, enable `Developer Mode` in Settings or use an administrator account. Otherwise `pnpm` ops will fail.

### Start Development

```bash
$ pnpm run dev
```

### Build

```bash
# For Windows
$ pnpm run build:win

# For macOS
$ pnpm run build:mac

# For Linux
$ pnpm run build:linux

# Specify architecture packaging
$ pnpm run build:win:x64
$ pnpm run build:win:arm64
$ pnpm run build:mac:x64
$ pnpm run build:mac:arm64
$ pnpm run build:linux:x64
$ pnpm run build:linux:arm64
```

## 👥 Community & Contribution

AgentConnector is an active open-source community project, and we welcome various forms of contribution:

- 🐛 Report issues: [AgentDNS](https://github.com/jsjfai/AgentDNS/issues)
- 💡 Submit feature suggestions: [AgentDNS](https://github.com/jsjfai/AgentDNS/issues)
- 🔧 Submit code improvements: [AgentDNS](https://github.com/jsjfai/AgentDNS/pulls)

## 🙏🏻 Thanks

This project is built with the help of these awesome libraries:

- [DeepChat](https://github.com/ThinkInAIXYZ/deepchat)
- [Vue](https://vuejs.org/)
- [Electron](https://www.electronjs.org/)
- [Electron-Vite](electron-vite.org)
- [Rolldown-Vite](https://github.com/vitejs/rolldown-vite)
- [oxlint](https://github.com/oxc-project/oxc)

## 📃 License

[LICENSE](./LICENSE)

