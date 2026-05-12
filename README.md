# OmniFlux

Universal torrent-to-MAME filtering engine for qBittorrent automation.

## Overview

OmniFlux is a desktop tool that connects MAME DAT/XML definitions with torrent datasets and automatically generates optimized download selections for qBittorrent.

It processes:

- MAME DAT/XML machine definitions
- Torrent file structures
- qBittorrent Web API file controls

The system performs game-level matching and applies selective download rules directly to qBittorrent.

## Features

- Load multiple torrent files locally
- Parse MAME DAT/XML machine lists
- Game-level matching (not ROM-level)
- Apply keep/skip rules to qBittorrent
- Supports merged, split, and non-merged sets
- Simple desktop GUI interface
- qBittorrent Web API integration

## How it works

MAME DAT → Machine list  
Torrent → Archive file list  
Matching engine → Compare datasets  
qBittorrent → Apply file priorities

## Requirements

- Python 3.10 or higher
- qBittorrent with Web UI enabled
- bencodepy
- requests
- tkinter

## Usage

1. Start qBittorrent and enable Web UI
2. Launch OmniFlux
3. Enter qBittorrent connection details
4. Load torrent files
5. Load MAME DAT/XML file
6. Select a torrent
7. Run filter

## Output

Example result:

Keep: 281  
Skip: 43537  
Filter applied successfully

## Architecture

- GUI layer (Tkinter)
- DAT parser (XML machine extraction)
- Torrent parser (bencode decoding)
- Matching engine (game-level comparison)
- qBittorrent Web API bridge

## Notes

OmniFlux does not download torrents directly.  
It controls file selection inside qBittorrent using priority rules.

## Future improvements

- Per-game selection interface
- Searchable ROM/game list
- Save and load filter profiles
- Real-time qBittorrent sync
- CHD and BIOS-aware filtering
- Multi-torrent batch processing

## License

Private / experimental project
