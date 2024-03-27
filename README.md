#### Contextual Constraints in Safari

- Safari only allows Clipboard API usage during direct user interaction.

#### Issue Encountered

- In asynchronous Promise chains triggered by user interaction, Safari blocks Clipboard API usage.

#### Problem Scenario

- Fetching data and copying it to the clipboard works in Chrome and Firefox but fails in Safari.

#### Error in Safari

- Safari throws an Unhandled Promise Rejection with the message: `NotAllowedError: The request is not allowed by the user agent or the platform in the current context, possibly because the user denied permission`.

#### Implementation Technique

- Create a ClipboardItem and add it to the clipboard instead of adding plain text, ensuring that the Clipboard API is called from a synchronous context directly triggered by user interaction.

**Disclaimer:** This repository and its contents are provided for personal documentation purposes only.
