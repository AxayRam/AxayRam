# Professional GitHub Portfolio Standards (Embedded Systems)

## 1) Profile Branding Guidelines
- Keep profile concise, technical, and authentic
- Use a clear headline with domain keywords
- Avoid exaggerated claims, vanity metrics, and decorative overload
- Prioritize technical clarity over visual effects

## 2) Professional Bio Suggestions
Use one of the following styles:
- "Embedded Systems Engineer focused on firmware architecture, Linux integration, and networked IoT devices."
- "Firmware developer building reliable embedded products with C, RTOS, and hardware-software co-design."

## 3) Clean Badge Set (Recommended)
- C, Linux, ESP32, STM32, Raspberry Pi, Git, GNU Make
- Keep badge style consistent (`flat-square` or `for-the-badge`, not mixed heavily)
- Avoid more than 8–12 badges on profile header

## 4) Contribution Graph Styling Suggestions
- Maintain steady weekly commits via real work logs and docs updates
- Prefer meaningful commits over frequency-only activity
- Use pinned repos and release notes to show impact, not contribution heatmap alone

## 5) Pinned Repository Strategy
Pin 6 repositories:
1. End-to-end IoT firmware project
2. STM32 or ARM Cortex driver stack
3. ESP32-CAM real-world use case
4. Raspberry Pi/Linux embedded integration project
5. RTOS-based multitasking demo with peripherals
6. Protocol-focused project (CAN/Modbus/TCP)

## 6) Professional Repository Description Examples
- "Embedded C firmware for ESP32-based home automation with modular drivers and cloud telemetry."
- "STM32 peripheral abstraction layer and RTOS task framework for sensor-actuator control."
- "Raspberry Pi C project for real-time distance sensing and adaptive GPIO response."

## 7) Embedded Repository Folder Structure (Reference)
```text
project-root/
├── firmware/              # application logic
├── drivers/               # peripheral drivers (gpio, uart, spi, i2c)
├── hal/                   # hardware abstraction layer
├── bsp/                   # board support package
├── include/               # public headers
├── config/                # build and runtime configs
├── tests/                 # unit and integration tests
├── docs/                  # architecture, diagrams, references
├── scripts/               # flash, format, tooling scripts
├── .github/               # issue/PR templates, CI
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

## 8) Documentation Quality Checklist
- Problem statement and use-case
- Hardware + software requirements
- Build/flash/run instructions
- Architecture section and module boundaries
- Protocol/interface documentation
- Troubleshooting section
- Roadmap and known limitations

## 9) Versioning and Release Strategy
- Follow SemVer (`MAJOR.MINOR.PATCH`)
- Tag releases (`v1.2.0`)
- Keep release notes concise: Added / Changed / Fixed
- Use `CHANGELOG.md` with Keep a Changelog format

## 10) Conventional Commit Examples
- `feat(firmware): add non-blocking UART ring buffer`
- `fix(i2c): recover from bus lock during sensor timeout`
- `refactor(drivers): split gpio init and runtime operations`
- `docs(readme): add hardware wiring diagram and flash steps`
- `chore(ci): add cppcheck and build matrix`

## 11) Branch Naming
- `feature/<scope>-<short-description>`
- `fix/<scope>-<short-description>`
- `docs/<scope>-<short-description>`

## 12) CI/CD Recommendations for Embedded Projects
- Static checks: `clang-format`, `clang-tidy`, `cppcheck`
- Build matrix for key targets/toolchains
- Run unit tests on pull requests
- Add artifact upload for firmware binaries and map files
- Add release workflow for tagged versions

## 13) Security Recommendations
- Never commit API keys, Wi-Fi credentials, or tokens
- Use `.env.example` and ignored local config files
- Validate input from serial/network interfaces
- Add basic threat notes for network-exposed devices

## 14) Profile Improvement Roadmap
- [ ] Standardize top 6 repos using README template
- [ ] Add CONTRIBUTING + LICENSE + templates in each active repo
- [ ] Add changelog and semantic version tags to major projects
- [ ] Introduce CI checks (lint/build/test)
- [ ] Add architecture diagrams to flagship projects
- [ ] Improve test evidence (logs/screenshots/videos)
- [ ] Maintain monthly project updates with measurable technical progress
