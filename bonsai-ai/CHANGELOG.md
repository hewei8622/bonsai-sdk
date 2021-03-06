# Changelog

## 2.0.20
- #9524: Fix WS read timeout log
- #8355: Fix for Config object to print clean JSON
- #9658: Config update should not fail if profile does not exist in .bonsai
- #1049: Addressed some issues in Python code that were uncovered by static analysis

## 2.0.19
- #7652 Remove redundant close code check from bonsai-ai reconnect policy
- #7801 - Add `--access-key` as an alias for `--accesskey`
- #7328: Network logs in bonsai-ai
- #7729: Added keep-alive pongs on a separate thread

## 2.0.18
- #7653: Braind service closes websocket with 1001, 3000-3099 or 4000-4099 when the Sim should not reconnect.
- #7746: Do not reconnect on ws close code 1000-1099. This is a permanent change.
- #7666: Fix bonsai-ai unit tests for Windows
- #6694: Remove warning spam in config
- #7650: Accept websocket close codes 4000-4099 to mean Do Not Reconnect
- #7648: ThreadPoolExecutor's shutdown method should not be called in OSX

## 2.0.17
- #7587 Turn PINGs on by default in bonsai-ai
- #7247: HTTP 401 and 404 should not initiate retries
- #7289: Add network timeout to brain http requests
- #7359: Fix a predictor test
- #7347: write "safe" accepted for `use_color` in config
- #7283: Add strict to tests marked with xfail

## 2.0.16
- Hotfix: `None` check in disconnect handler

## 2.0.15
- Bug fix in reconnect logic
- Add `Brain.sim_exists`
- Add guards for sim name existence/matching
- Add threading on sim calls in run loop for Unix/Windows
- Add configurable network timeout (websocket handshake)

## 2.0.14
- Improved loading of proxy settings.
- ping_interval parameters in Config
- sim_connection sends pings over specified interval
- change default retry timeout from 3000 seconds to 300 seconds.
- Added `file_path` to config
- Added input validation around ping-intervals

## 2.0.13
- Add reconnect parameters to config
- Add reconnect behavior with exponetial backoff
- Add Brain.exists and Brain.ready

## 2.0.12
- Fix bug related to default url not being set on the Config object

## 2.0.11
- Flush record buffer on every call to `run`
- Improved config file error reporting
- Generate `FinishedEvent` in response to server errors
- Log Sim ID to the console immediately after registration
- Fix Config bug involving `DEFAULT` profile
- Added `use_color` flag to Config
- Fix bug where default url was getting assigned before config is parsed
- Fix Config tests
- Added `Brain.exists` and `Brain.state` for better status checking

## 2.0.10
- Fix sequencing bug in predict mode

## 2.0.9
- Make testing logs quieter
- update http to https for all setup.py

## 2.0.8
- Event pump API (feature parity with libbonsai)

## 2.0.7
- Fixed sequencing in prediction mode after terminal conditions.
- Fixed IOLoop collision when running in Jupyter
- Reliability improvements in analytics recorder

## 2.0.6
- Recording file controllable on a per-Sim basis
- Adds a mechanism to uniformly record simulation data to a file
- change README files to use reStructuredText instead of Markdown, per pip standards

## 2.0.5
- `Predictor` added to bonsai-ai
- `bonsai-cli` is now a requirement for bonsai-ai
- Add statistics collection and introduce an `episode_finish()` callback
- Added `wheel` as a requirement for bonsai-ai
- `Predictor` context manager bug fix
- Add mechanisms (library, config, command line) to record simulation data to a file.

## 2.0.4
- `Config.verbose` field to enable/disable verbose logging
- Updated Config to be used in the cli

## 2.0.3
- User-Agent added to bonsai-ai requests
- Adds logging module

## 2.0.2
- Fix for objective_name returning None

## 2.0.1
- Updated doc strings
- Added missing Simulator properties

## 2.0.0
- Initial release
