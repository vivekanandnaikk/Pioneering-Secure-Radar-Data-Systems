# Project Plan

## Phase 1 — Preserve and document the project

- Keep the report-described scope separate from verified repository features.
- Add the project report only if redistribution is approved.
- Extract original hardware, wiring, and results assets from the report.
- Record project team, guides, institution, academic year, and attribution.

## Phase 2 — Recover verified firmware

- Obtain the original sender and receiver source code.
- Confirm whether Arduino IDE or ESP-IDF was used.
- Identify board support packages and libraries.
- Separate firmware into clear sender and receiver folders.
- Remove credentials, secrets, and environment-specific addresses.
- Add a dependency manifest or pinned build instructions.

## Phase 3 — Document hardware

- Record ESP32 board models.
- Confirm AWR1243 integration status and interface.
- Add a wiring table and schematic.
- Document LCD addresses and pin assignments.
- Specify power requirements and operating constraints.

## Phase 4 — Verify cryptographic design

- Identify the AES implementation and exact mode.
- Document key length and provisioning.
- Assess the need for authenticated encryption, replay protection, nonce/IV handling, and integrity checks.
- Replace demonstration credentials with safe local configuration examples.
- Do not describe AES-128 alone as a complete authenticated secure-channel design.

## Phase 5 — Add reproducible setup

- Add verified firmware build steps.
- Document Wi-Fi and UDP setup.
- Document radar and LCD configuration.
- Add sender and receiver run instructions.
- Include troubleshooting and known limitations.

## Phase 6 — Evaluate and report results

- Define distance ground truth and test geometry.
- Measure representative distance error without overstating accuracy.
- Measure end-to-end latency and packet loss using a repeatable procedure.
- Record network conditions and hardware configuration.
- Compare repeated trials and disclose sample counts.
- Clearly distinguish a demonstration from production validation.

## Phase 7 — Repository presentation

- Add a conventional MIT or another reviewed license only after ownership and third-party terms are checked.
- Update README evidence tables as verified artifacts become available.
- Add a tagged release for reproducible source snapshots.
- Keep the safety disclaimer prominent.

## Phase 8 — Safety review

- Document that the prototype is not suitable for certified or safety-critical use.
- Identify failure modes for radar, network, cryptography, power, and display components.
- Require independent validation before any application beyond educational demonstration.
