# Data Sanitizer Sweep Process

A JavaScript program that sanitizes log entries by replacing disallowed characters with `#` and tracks the number of processed entries.

## Features

- Replaces disallowed characters in log entries.
- Detects fatal entries containing `$` and stops processing.
- Skips informational entries starting with `/`.
- Tracks total, sanitized, and informational entries.
- Uses separate functions for sanitization and log processing.

## Functions

- `sanitizeLog(entry, disallowedCharacters)` – Sanitizes a single log entry.
- `cleanLogs(logs, disallowedCharacters)` – Processes multiple log entries and returns processing statistics.

## Technologies

- JavaScript

## Usage

```javascript
let logs = [
  "ERROR: Failed to connect to db",
  "/INFO: Cache cleared successfully",
  "WARN: Disk usage at 92%"
];

let disallowedCharacters = ["a", "A", "c", "T"];

console.log(cleanLogs(logs, disallowedCharacters));
```

## Example Output

```text
Total Entry Count: 3. Sanitized Entry Count: 2. Informational Entry Count: 1. Finished sanitizing logs.
```

## Learning Objectives

Practice JavaScript functions, arrays, loops, conditionals, string methods, and counters.
