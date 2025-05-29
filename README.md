# find-in-rekordbox
Find and query stuff from your rekordbox.xml file but from a command line. 

Requirements: 
- Rekordbox.xml file available (created by pioneer rekordbox)
- terminal // xterminal
- an export of the rekordbox.xml file in the same directory as this code base.

🧰 Usage
```
find-in-rekordbox [-h] -a ARTIST [-f FILE]
                  [--genre GENRE]
                  [--bpm-min BPM_MIN] [--bpm-max BPM_MAX]
                  [--unplayed]
                  [--after AFTER] [--before BEFORE]
                  [--sort {bpm,key,title}]
                  [--csv CSV]
```

🧩 Options
| Option           | Description                                        |
| ---------------- | -------------------------------------------------- |
| `-h`, `--help`   | Show help and exit                                 |
| `-a`, `--artist` | **Artist name** to search for (**required**)       |
| `-f`, `--file`   | Path to `rekordbox.xml` (default: `rekordbox.xml`) |
| `--genre`        | Filter by genre (partial match, case-insensitive)  |
| `--bpm-min`      | Minimum BPM                                        |
| `--bpm-max`      | Maximum BPM                                        |
| `--unplayed`     | Only include tracks with `Play Count = 0`          |
| `--after`        | Include only tracks added after `YYYY-MM-DD`       |
| `--before`       | Include only tracks added before `YYYY-MM-DD`      |
| `--sort`         | Sort by `bpm`, `key`, or `title`                   |
| `--csv`          | Path to export matching tracks as a CSV            |


🧪 Examples  

```find-in-rekordbox -a "Nora"```  
→ Find all tracks by artists containing the word "Nora"


```find-in-rekordbox -a "Ben Böhmer" --genre "Melodic" --bpm-min 115 --bpm-max 125 --sort bpm```  
→ Melodic house vibes with specific tempo control


```find-in-rekordbox -a "" --unplayed --csv unplayed.csv```  
→ Dump your unplayed tracks to a CSV for discovery


🐟 Made with special BASSpro gear by DJ Wootsie Woot  
Bass Pro certified. 🎣🕺
