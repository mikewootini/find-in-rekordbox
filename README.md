# find-in-rekordbox
Find and query stuff from your rekordbox.xml file but from a command line. 

Requirements: 
- Rekordbox.xml file available (created by pioneer rekordbox)
- terminal // xterminal
- an export of the rekordbox.xml file in the same directory as this code base.

usage: find-in-rekordbox [-h] -a ARTIST [-f FILE] [--genre GENRE] [--bpm-min BPM_MIN] [--bpm-max BPM_MAX]
                         [--unplayed] [--after AFTER] [--before BEFORE] [--sort {bpm,key,title}] [--csv CSV]

Search Rekordbox collection by artist, genre, bpm, and more.

options:
  -h, --help            show this help message and exit
  -a, --artist ARTIST   Artist name to search for
  -f, --file FILE       Path to rekordbox.xml
  --genre GENRE         Filter by genre (partial match)
  --bpm-min BPM_MIN     Minimum BPM
  --bpm-max BPM_MAX     Maximum BPM
  --unplayed            Only include tracks with 0 play count
  --after AFTER         Only include tracks added after YYYY-MM-DD
  --before BEFORE       Only include tracks added before YYYY-MM-DD
  --sort {bpm,key,title}
                        Sort output
  --csv CSV             Optional path to export matching tracks as CSV
