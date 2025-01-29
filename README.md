## Getting Started

First, let's get a newer and smarter model called **DeepSeek R1** with the following command:

```sh
ollama run deepseek-r1
```

You can modify the token sizes depending on your computer's capabilities.

### Setting Up Your AI Environment

Start your AI setup using the shell script (link available in the video description). Then:
1. Browse to `localhost:8080`
2. Click on **Workspace** from the left sidebar

## Creating a Knowledge Base

### Example 1: AMD CPU Specifications

#### What are you working on?
**AMD CPU Specifications**

#### What are you trying to achieve?
Creating a **comprehensive, searchable database** to provide quick and accurate insights into AMD CPU specifications for developers, tech enthusiasts, and consumers.

This knowledge base will consolidate information about AMD processors from official specification CSV files. Users can query details such as **model names, cores, threads, clock speeds, TDPs, and supported technologies**.

#### Objective:
To empower users with a tool that provides **instant, reliable answers** about AMD processors, reducing the need to manually search the AMD website.

---

### Example 2: Intel CPU Specifications

#### What are you working on?
**Intel CPU Specifications**

#### What are you trying to achieve?
Developing a **comprehensive database** that allows users to search and analyze Intel CPU specifications, making it easy to compare processors and access detailed information.

This knowledge base will include detailed information about **Intel CPUs**, such as:
- Model numbers
- Core counts
- Thread counts
- Base/boost clock speeds
- Cache sizes
- TDP values
- Supported technologies

#### Objective:
To provide developers, tech enthusiasts, and end-users with a tool for **efficiently retrieving reliable data** about Intel processors.

---

## Creating ModelFiles with DeepSeek R1

### Steps:
1. Go to the **Models** menu.
2. Click the little **plus (+) icon** to add a new model.

### Example 1: AMD CPU Expert Model

```yaml
Model Name: AMD CPU Expert
Base Model From: deepseek-r1

Description: This model is optimized for querying and analyzing AMD CPU specifications using a comprehensive knowledge base. It enables fast, detailed responses to technical queries.

Tags: AMD, CPU
Visibility: Public

Model Params:
  System Prompt:
    You are an expert in AMD CPUs. Use the attached knowledge base to provide precise and concise answers to technical questions about AMD processors, such as specifications, performance details, and comparisons.

Advanced Params: Leave as default unless you have specific customization requirements (temperature, token limits, etc.).

Prompt Suggestions:
  - What are the specifications of the Threadripper PRO 7995WX?
  - Compare the Threadripper PRO 5995WX with the Threadripper PRO 7995WX.

Tools: Attach additional tools if required, such as calculation tools or external APIs for comparisons.
Filters: Add filters for specific preprocessing or content restrictions (e.g., only showing CPUs with certain attributes).
Actions: Define actions beyond answering queries, such as exporting data or generating reports.
Capabilities: Disable Vision, Enable Usage and Citations.
```

---

### Example 2: Intel CPU Expert Model

```yaml
Model Name: Intel CPU Expert
Base Model From: deepseek-r1

Description: This model is optimized for querying and analyzing Intel CPU specifications using a comprehensive knowledge base. It provides detailed and accurate responses to technical questions about Intel processors.

Tags: Intel, CPU
Visibility: Public

Model Params:
  System Prompt:
    You are an expert in Intel CPUs. Use the attached knowledge base to provide precise and concise answers to technical questions about Intel processors, such as specifications, performance details, and comparisons.

Advanced Params: Leave as default unless you have specific customization requirements (temperature, token limits, etc.).

Prompt Suggestions:
  - What are the specifications of the Intel Core i9-12900KS?
  - Compare the Intel Core i9-12900KS and Intel Core i9-13900KS.
  - What is the base and turbo clock speed of the Intel Core i9-14900KS?

Tools: Attach additional tools if required, such as calculation tools or external APIs for comparisons.
Filters: Add filters for specific preprocessing or content restrictions (e.g., only showing CPUs with certain attributes).
Actions: Define actions beyond answering queries, such as exporting data or generating reports.
Capabilities: Disable Vision, Enable Usage and Citations.
```

---

## Conclusion

Now that you've created your **knowledge base** and **models**, you are ready to start leveraging **DeepSeek R1** for enhanced CPU analysis and queries. Customize the settings as needed and start exploring the powerful capabilities of your AI models!
