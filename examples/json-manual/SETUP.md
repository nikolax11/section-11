# Manual JSON Export

Export Intervals.icu data locally for different time ranges.

## Prerequisites
- Python 3.8+
- `requests` library: `pip install requests`

## First-Time Setup
```bash
python sync.py --setup
```
Enter your Intervals.icu credentials when prompted.

## Usage

### Export to local file
```bash
# Last 7 days (default)
python sync.py --output latest.json

# Last 14 days
python sync.py --days 14 --output 14days.json

# Last 90 days
python sync.py --days 90 --output 90days.json
```

### Common time ranges
| Days | Use case |
|------|----------|
| 7 | Weekly review |
| 14 | Two-week block |
| 28 | Four weekly analysis |
| 90 | Quarterly / block review |
| 180 | Season review |

### Push to GitHub (optional)
```bash
python sync.py --days 14
```
Pushes to your configured GitHub repo.

## Use with AI
Paste the JSON contents directly, or upload the file to your AI chat.
