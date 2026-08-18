# -DarkSword-two
 DarkSword Secondary Development

 The complete project (including the Stage 1 WASM exploit compatible with iOS 16.2, 16.6, and 17.x; the Stage 3 native bridge; and the dylib injected into powerd) is not available for free.
 
<img width="3071" height="1595" alt="image" src="https://github.com/user-attachments/assets/99ca9192-0fc3-4370-bb86-1cf00f99dfb1" />

Admin Dashboard (Vue Frontend)
Dashboard: 16 statistical cards + 6 charts (device status, command status, top models, top channels, exfiltration category distribution, 7-day trends)
Device Management: Device list, details, heartbeat timeline, utilization progress bar (7-stage visualization), access log terminal
Command Execution: Command history, status filtering, manual retry, quick templates, batch execution
Data Exfiltration: Categorized preview and download (Sandbox data, Keychain, WiFi, Contacts, SMS, Call logs, Photos, Files, Wallet)
Channel Management: Phishing landing page configuration, domain whitelisting, template binding
Template Management: Editable HTML templates (e.g., Apple ID login simulation)
Audit Logs: Full audit of logins, commands, and data operations
C2 Backend (FastAPI, Port 7000)
JWT authentication + 2FA support + Rate limiting
8 major modules: Devices, Commands, Exfiltration, Channels, Templates, Proxies, Users, Audit
SSE real-time notification stream (device online status, command execution, data callback)
Single-port hosting for bundled frontend (no separate Nginx server required for frontend)
Exploit Service (Port 7070)
Channel phishing landing: `/ch/<slug>?tpl=<tpl>`
Device registration: `_ensure_device_registered` with 3-level UUID resolution (query → cookie → referer) + blocking of 40+ crawler User-Agents
C2 command distribution: 5-step state machine (Fake-completed reset → Stale reset → Safari prefix filtering → Deferred backoff → Concurrency protection)
Result write-back: `/cmd_result` + Exfiltration data persistence (Prefix '34' → 9 major categories → Automatic file extension selection)
Asynchronous reporting: 3 daemon threads → Port 7000 (device registration, vulnerability reports, device data)


Purchased for 5,000 USDT; this is a re-skinned/customized version. Please contact me if interested.

 Fixed price: 1,000 Send the source code directly.
 
| Contact Information         | address                     |
| ------------ | ---------------------- |
| **Telegram** | <https://t.me/weizhentian9527> |
