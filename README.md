<!-- Generated distribution; edit the canonical repository. -->
# swift-ai-groq 1.2.0

Independent Swift-native port of Vercel AI SDK. Source and upstream dispositions are in PROVENANCE.json and Porting/.

## Distribution manifest

Add this package to your SwiftPM dependencies:

```swift
.package(url: "https://github.com/SwiftAISDK/swift-ai-groq.git", from: "1.2.0")
```

Products: `SwiftAIGroq`.
Contribute and report issues in the canonical SwiftAISDK repository.

## Authored usage guide

# SwiftAIGroq

Swift-native port of `@ai-sdk/groq`. Maintained in the canonical SwiftAISDK repository and exported as an independent Swift package.

The canonical repository owns all source edits. This package owns its provider
configuration and wire behavior, using only the declared shared dependencies.
Existing upstream baselines, capabilities and documented gaps remain unchanged.
See `Porting/map.json` and the canonical provider guide.

See [provider usage and capabilities](https://github.com/SwiftAISDK/SwiftAISDK/blob/main/docs-site/scripts/provider-guides/groq.md) for authentication, options and supported surfaces.
## Behavior notes

`transcribeFromURL` sends HTTP(S) audio URLs without userinfo directly to Groq and removes fragments. It returns nil only for Groq's HTTP 400 redirect-fetch limitation, allowing the facade to use its secure downloader; authentication and other media failures propagate. Plain-text transcription responses work for both URL and file input. Tool replay preserves valid JSON argument text and quotes malformed text.
