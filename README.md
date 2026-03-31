
# Memory-Artifact-Extraction-Script

A python script that takes a memory image as input, runs Volatility 3 commands against it, parses the results, and generates a report.

## Notes For Building

**Four main functions:**

1. Takes a memory image as input
2. Runs Volatility plugins
3. Parses the results
4. Saves a clean report of any artifacts

**Core Features:**

1. Identify image profile / OS details
2. Extract Process info
3. List network connections
4. Build parent/child process tree
5. Pull artifacts:
    pslist, pstree, psscan
    netscan, cmdline, dlllist, handles, malfind

**Predicted Files/File Structure:**

1. main.py: CLI 
2. vol_runner.py: for running volatility plugins
3. parser.py: helpers for normalizing the plugin outputs
4. detectors.py: detection rules
5. report_gen.py: creates JSON, CSV, and text summary outputs
6. utils.py: hashing, timestamps, directory helpers, etc.
7. README.md: setup and use instructions


**Stages while building:**

1. CLI that runs one plugin
2. Support multiple plugins
3. Parse output into dictionaries
4. Export JSON
5. Add suspicious artifact rules
6. Add correlation/scoring
7. Add HTML or dashboard reporting
