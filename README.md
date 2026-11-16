<!-- Generated distribution; edit the canonical repository. -->
# swift-ai-groq 1.3.0

Independent Swift-native port of Vercel AI SDK. Source and upstream dispositions are in PROVENANCE.json and Porting/.

## Distribution manifest

Add this package to your SwiftPM dependencies:

```swift
.package(url: "https://github.com/SwiftAISDK/swift-ai-groq.git", from: "1.3.0")
```

Products: `SwiftAIGroq`.
Contribute and report issues in the canonical SwiftAISDK repository.

## Authored usage guide

# Groq for Swift

`SwiftAIGroq` adds Groq to [SwiftAISDK](https://github.com/SwiftAISDK/SwiftAISDK), an independent Swift port of the Vercel AI SDK. It ports `@ai-sdk/groq` and supports text generation and transcription.

Provider guide with models, options, streaming and errors:

- [Groq](https://swiftaisdk.github.io/SwiftAISDK/providers/groq/)

## Usage

Add the `SwiftAI` product from `swift-ai-core` and the `SwiftAIGroq` product from this package to your target, then create the provider:

```swift
import SwiftAI
import SwiftAIGroq

let provider = try AIProviders.groq(configuration: GroqProviderSettings())
```

By default the provider reads `GROQ_API_KEY` from the environment; values set in `GroqProviderSettings` take precedence.

To use every provider through one dependency, add the complete [SwiftAISDK](https://github.com/SwiftAISDK/SwiftAISDK) package instead; see [Install](https://swiftaisdk.github.io/SwiftAISDK/getting-started/install/).

## Contributing

This package is exported from `Packages/swift-ai-groq` in the canonical [SwiftAISDK](https://github.com/SwiftAISDK/SwiftAISDK) repository. Open issues and pull requests there.
