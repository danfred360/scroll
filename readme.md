# scroll

run a webgui server to provide locally hosted ai assistants using ollama.

## web search

generate [a perplexity api key](https://docs.perplexity.ai/guides/getting-started) and paste it into the web search settings of the openwebui service once it's running (with the perplexity search provider selected) to enable web search using perplexity's api.

## recommended models

| model name | description | use |
|- | - | - |
| [dolphin3:8b](https://ollama.com/library/dolphin3) | fine tuned llama3.1:8b with model use guidelines removed | when the content restrictions of commercial llms would interfere with a useful query |
| [qwen3:14b](https://ollama.com/library/qwen3) | cutting edge reasoning model for general use, coding, and tool use | useful for complex reasoning tasks, coding, and tool use like web browsing or mcp servers |

## run it yourself

see [the docs](./docs/index.md)