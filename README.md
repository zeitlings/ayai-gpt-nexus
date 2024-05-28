<img src="assets/images/header.png" width="800px">

__ChatGPT__, __Claude__, __Perplexity__, and __Gemini__ integrations for chat, information retrieval, and text processing tasks, such as paraphrasing, simplifying, or summarizing. 
With support for third party __proxies__ and __local language models__.

---

> __Note:__ This is a preview version (alpha) of the workflow.

---

## B. Usage

### Keyword

<img src="assets/images/preview/keyword.png" width="564px"/>

- <kbd>↩</kbd> to continue the ongoing chat.
- <kbd>⌘</kbd><kbd>↩</kbd> to start a new conversation.
- <kbd>⌥</kbd><kbd>↩</kbd> to view the chat history.
- <kbd>⌘</kbd><kbd>⇧</kbd><kbd>↩</kbd> to open the workflow configuration __(hidden)__.


### Chat Window

<img src="assets/images/preview/chat+websearch.png" width="564px"/>


- <kbd>↩</kbd> to ask a question.
- <kbd>⌘</kbd><kbd>↩</kbd> to start a new conversation.
- <kbd>⌥</kbd><kbd>↩</kbd> to copy the last answer.
- <kbd>⌃</kbd><kbd>↩</kbd> to copy the full conversation.
- <kbd>⇧</kbd><kbd>↩</kbd> to stop generating an answer.

* __Hidden Options__
  - <kbd>⇧⌥⏎</kbd> to show configuration info in HUD
  - <kbd>⇧⌃⏎</kbd> to __speak__ the last answer out loud
  - <kbd>⌘⇧⏎</kbd> to edit __multi-line prompt__ in separate window

### Chat History

- Type to filter archived chats based on your query.
- <kbd>↩</kbd> to continue previous chat.
- <kbd>⌥</kbd> to view the modification date.
- <kbd>⌘</kbd><kbd>L</kbd> to inspect the unabridged preview as [large type](https://www.alfredapp.com/help/features/large-type/).
- <kbd>⌘</kbd><kbd>⇧</kbd><kbd>↩</kbd> to send the conversation to the trash.

## C. Prompting

> A prompt is the text that you give the model to elicit, or "prompt," a relevant output. A prompt is usually in the form of a question or instructions.

### References

- [General prompt engineering guide](https://www.promptingguide.ai/)
- [OpenAI prompt engineering guide](https://platform.openai.com/docs/guides/prompt-engineering) | [Prompt Gallery](https://platform.openai.com/docs/examples)
- [Anthropic prompt engineering guide](https://docs.anthropic.com/en/docs/prompt-engineering) | [Prompt Gallery](https://docs.anthropic.com/en/prompt-library/library) 
- [Google AI prompt engineering guide](https://ai.google.dev/gemini-api/docs/prompting-intro) | [Prompt Gallery](https://ai.google.dev/gemini-api/prompts)

## D. Configuration


### Primary 

The *primary* configuration setting determines the service that is used for conversations.

#### OpenAI Proxies[^1]

If you wish to use a third party proxy, define the correlating `host`, `path`, `API key`, `model`, and if required the `url scheme` or `port` in the [environment variables](https://www.alfredapp.com/help/workflows/advanced/variables/#environment).
The variables are prefixed as alternatives to OpenAI, because *Ayai* expects the returned stream events and errors to mirror the shape of those returned by the OpenAI API.


#### Local LM's[^2]

If you wish to use a local language model, define the correlating `url scheme`, `host`, `port`, `path`, and if required the `model` in the [environment variables](https://www.alfredapp.com/help/workflows/advanced/variables/#environment) to establish a connection to the local HTTP initiated and maintained by the method of your choice.
The variables are prefixed as alternatives to OpenAI, because *Ayai* expects the returned stream events and errors to mirror the shape of those returned by the OpenAI API.


[^1]: Third party proxies such as [OpenRouter](https://openrouter.ai/), [Groq](https://groq.com/), [Fireworks](https://fireworks.ai/)  or [Together.ai](https://www.together.ai/)  
[^2]: Local HTTP servers can be set up with interfaces such as [LM Studio](https://lmstudio.ai/) or [Ollama](https://ollama.com/)