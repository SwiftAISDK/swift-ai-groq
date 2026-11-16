# Changelog

## 1.3.0

- Tool results send only their value, assistant reasoning is kept in history, partial image types and `tools: []` match upstream, streamed usage reads `x_groq.usage` and function tools send only their input schema.
  Compatibility: Source-compatible; changes are additive. Request bodies, results, warnings and errors change to match the reviewed upstream package.
