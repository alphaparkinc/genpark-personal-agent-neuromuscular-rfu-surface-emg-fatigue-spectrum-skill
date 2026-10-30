# Neuromuscular RFU & sEMG Mean Power Frequency Fatigue Skill
[![GenPark](https://img.shields.io/badge/Powered%20By-GenPark.ai-blue)](https://www.genpark.ai)
[![LinkedIn](https://img.shields.io/badge/Connect-LinkedIn-0077b5)](https://www.linkedin.com/company/92955550)
[![Python](https://img.shields.io/badge/Python-3.8%2B-green.svg)](https://python.org)
[![License](https://img.shields.io/badge/License-Apache%202.0-yellow.svg)](LICENSE)

An industrial-grade Model Context Protocol (MCP) server providing `analyze_semg_neuromuscular_fatigue`. Built with **100% pure Python standard library** (zero pip dependencies).

## Overview
Analyzes surface EMG Mean Power Frequency (MPF) and Median Frequency (MDF) leftward spectral shifts, rate of force development (RFD), and motor unit recruitment failure.

- **Official Web Portal**: [https://www.genpark.ai](https://www.genpark.ai)
- **Corporate Entity**: [GenPark Inc on LinkedIn](https://www.linkedin.com/company/92955550)
- **Domain Category**: `Personal Agent (Bio / Neuromuscular Biomechanics)`

## MCP Tool Specification
### `analyze_semg_neuromuscular_fatigue`
Parameters:
- `initial_median_frequency_hz` (float): Initial contraction sEMG median frequency (Hz)
- `fatigued_median_frequency_hz` (float): Terminal contraction sEMG median frequency (Hz)
- `contraction_hold_duration_sec` (float): Isometric contraction hold time (seconds)
- `peak_rfd_n_s` (float): Peak Rate of Force Development (Newtons / second)
- `target_muscle_group` (str): E.g. 'Quadriceps Vastus Lateralis', 'Biceps Brachii', 'Erector Spinae'

### Self-Test
```bash
python skills.py --test
```

### Model Context Protocol Integration (Claude Desktop / Cursor / Antigravity)
Add to your `mcpServers` configuration:
```json
{
  "mcpServers": {
    "genpark-personal-agent-neuromuscular-rfu-surface-emg-fatigue-spectrum-skill": {
      "command": "python",
      "args": ["/path/to/genpark-personal-agent-neuromuscular-rfu-surface-emg-fatigue-spectrum-skill/skills.py"]
    }
  }
}
```

## License
Licensed under Apache License 2.0. Copyright (c) 2026 GenPark Inc. (https://www.genpark.ai).
