# find-in-rekordbox
Find and query stuff from your rekordbox.xml file but from a command line. 
I mainly made this to find things and sort quickly without having to load Rekordbox everytime.  

Requirements: 
- Rekordbox.xml file available (created by pioneer rekordbox)
- terminal window open or (xterminal, iTerm, etc - default zsh or bash should be fine)  
- an export of the rekordbox.xml file in the same directory as this code base.
- Python installed (if on Windows you may need to install Python - already there on a Macbook)

💾 Install  
1. Download the file from this repo. 
2. If you already have an export of your rekordbox.xml file great, if not you can easily make one in Rekordbox. You can name it whatever you want, but I recommend keeping it `rekordbox.xml`.  If you change the name, use the `-f <name of file>` option.
3. Make the command executable otherwise you have to invoke python to run it. To do that, run this in the terminal - `chmod +x find-in-rekordbox`, but  if that gives you an error because your python installed in a different location, run `python3 find-in-rekordbox -h` 
     


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
