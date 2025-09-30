# Example MCP Remote Client connector within AI Orchestrated workflow

[Source code](https://github.com/jlwjohnson/mcpWCamunda)

This repository contains a sample Camunda BPMN process that uses a Camunda AI agent to interact with a public [MCP Server called DeepWiki MCP](https://docs.devin.ai/work-with-devin/deepwiki-mcp). This MCP server exposes tools for interacting with [Devin, a AI software engineer](https://docs.devin.ai/), capable of answering questions about GitHub repositories.

# How to Run this Example

Create a new Process Application in Camunda Modeler and import the following files:

* [Make a Request (form)](Make%20a%20Request.form)
* [Get More Information (form)](Get%20More%20Information.form)
* [Display Results (form)](Display%20Results.form)
* [AI Agent Chat with MCP (BPMN)](AI%20Agent%20Chat%20with%20MCP.bpmn)

Set the [AI Agent Chat with MCP](AI%20Agent%20Chat%20with%20MCP.bpmn) process as the Main process.

The AI Agent is configured to use AWS Bedrock and needs to be configured with your AWS credentials. To do so, configure the following Connector Secrets: 

`AWS_REGION_ID`
`AWS_ACCESS_KEY_ID`
`AWS_ACCESS_KEY_SECRET`

Deploy the [AI Agent Chat with MCP](AI%20Agent%20Chat%20with%20MCP.bpmn) process and start an instance using the Start Form.



