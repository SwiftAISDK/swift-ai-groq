# Changelog

## 1.1.0

- GPT-OSS portable none maps to low with compatibility warning; exact Qwen qwen/qwen3.6-27b accepts none directly; nonreasoning families omit none with unsupported warning. Other portable effort levels use the shared nearest-supported mapping; explicit native effort remains independent. Reviewed upstream: @ai-sdk/groq 4.0.70 to 4.0.74. Validation passed: node Scripts/test-packages.mjs (all 52 owning package suites and the compatibility facade); node Scripts/sdk.mjs generate --check; node --test Scripts/tests/*.test.cjs (27 passed); docs-site check and build (100 pages). Live provider calls were not run.
  Compatibility: Minor release for additive native API; existing static settings and call sites remain compatible. Updated direct dependency minimums are recorded in the manifest. Existing documented JS/framework and native product gaps remain; version-delta review does not imply full parity or live-service testing. Explicit custom authentication skips an unused credential supplier, a deliberate native callback-order adaptation.
