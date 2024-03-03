# Fyodorov CLI Tool

The Fyodorov CLI tool is designed to streamline your interaction with Fyodorov services, including authentication, and deployment. Below are the instructions to get started with signing up and deploying your configuration.

## Installation

Before using the Fyodorov CLI tool, ensure you downloaded the correct binary for your system.

## Signing Up

To start using the Fyodorov services, you must first sign up and authenticate. You can do this directly through the CLI tool:

```bash
./fyodorov auth
```

You will need an invite code. If you weren't provided with one you can try this: `GITHUB`

## Deploying the Configuration

If you haven't already created a configuration file, here's an example fyodorov_config.yml to get started:
```yaml
version: 0.0.1
providers:
  - name: openai
    api_url: https://api.openai.com/v1
models:
  - name: chatgpt
    provider: openai
    model_info:
      mode: chat
      base_model: gpt-3.5-turbo
agents:
  - name: My Agent
    description: My agent for chat conversations
    model: chatgpt
    prompt: My name is Daniel. Please greet me and politely answer my questions.
```

Once your configuration is set and saved, you can deploy it using the Fyodorov CLI tool:

```bash
./fyodorov deploy config.yml
```
This command will deploy your current configuration to the Fyodorov platform, making it active and ready to use.

## Getting Help

For more detailed information about each command, you can use the help flag:
```bash
./fyodorov [command] --help
```
For example:

```bash
./fyodorov deploy --help
```
This will provide detailed usage instructions for the deploy command.
