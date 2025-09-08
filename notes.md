# Golem-1.3.0-rc3 notes

* tools and providerOptions should be optional in golem-llm's Config
* binding should generate ? for fields
* bad error messages from typescript
```
[runtime error] failed to invoke function golem-qa:research-agent/research-agent.{reserch}: Worker Service - Error: 500 Internal Server Error, Invocation Failed:
error while executing at wasm backtrace:
    0: 0x479936 - golem_agent.wasm!abort
    1: 0x3e4978 - golem_agent.wasm!std::sys::pal::wasi::helpers::abort_internal::hcc3b2e0cde3c9001
    2: 0x246ed2 - golem_agent.wasm!std::process::abort::h0e38511b4c8b6f04
    3: 0x3de0d6 - golem_agent.wasm!__rustc[5224e6b81cd82a8f]::__rust_abort
    4: 0x3de0cc - golem_agent.wasm!__rustc[5224e6b81cd82a8f]::__rust_start_panic
    5: 0x3e496e - golem_agent.wasm!__rustc[5224e6b81cd82a8f]::rust_panic
    6: 0x3e4525 - golem_agent.wasm!std::panicking::rust_panic_with_hook::h085fb375cd657b2f
    7: 0x3e7b32 - golem_agent.wasm!std::panicking::begin_panic_handler::{{closure}}::he68af7f9d5c53e56
    8: 0x3e7a9e - golem_agent.wasm!std::sys::backtrace::__rust_end_short_backtrace::h4c38003a22ca226f
    9: 0x248142 - golem_agent.wasm!__rustc[5224e6b81cd82a8f]::rust_begin_unwind
   10: 0x246077 - golem_agent.wasm!core::panicking::panic_fmt::h4e32e8d1cab5f47e
   11: 0x32857f - golem_agent.wasm!golem_agent::internal::call_js_export::{{closure}}::{{closure}}::{{closure}}::hfb9adc4dce3b18ed
   12: 0x2ef814 - golem_agent.wasm!<core::pin::Pin<P> as core::future::future::Future>::poll::h19791fc2e80e0f3c
   13: 0x25c0ed - golem_agent.wasm!golem_agent::bindings::exports::golem::agent::guest::_export_invoke_cabi::h2d57e85d7941f225
   14: 0x3c0ff7 - golem_agent.wasm!golem:agent/guest#invoke
   15:   0xbacd - <unknown>!<wasm function 27>
   16: 0x5efb22 - wit-component:shim!indirect-golem:agent/guest-invoke
   17: 0x5e5fe0 - <unknown>!<wasm function 87>
   18: 0x5df4f6 - <unknown>!<wasm function 83>
   19: 0x5c9b51 - <unknown>!<wasm function 79>
   20: 0x5c9a6f - <unknown>!<wasm function 71>: wasm trap: wasm `unreachable` instruction executed
   ```
* results are very annoying to deal with in typescript
* golem-ai web search urls in the templates are wrong. Should be web_search instead of websearch
* we need a way to generate uuids in rib
* worker service does not decode spaces in query params properly: `Are+cucumbers+healthy?`
