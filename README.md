<p align="center">
  <strong>Sherlock</strong>
  <br>
  Hunt down social media accounts by username across <a href="https://sherlockproject.xyz/sites">400+ social networks</a>
  <br><br>
  <a href="https://sherlockproject.xyz/installation">Installation</a> •
  <a href="https://sherlockproject.xyz/usage">Usage</a> •
  <a href="https://sherlockproject.xyz/contribute">Contributing</a>
</p>

## Installation

| Method | |
| - | - |
| `pipx install sherlock-project` | `pip` or [`uv`](https://docs.astral.sh/uv/) work too |
| `docker run -it --rm sherlock/sherlock` | |
| `dnf install sherlock-project` | |

Community packages exist for Debian (>= 13), Ubuntu (>= 22.10), Homebrew, Kali and BlackArch, but they are not maintained by this project.

> [!WARNING]
> Third-party packages for ParrotOS and Ubuntu 24.04 are __broken__. Use `uv`, `pipx`, `pip` or Docker on those systems.

More options: [sherlockproject.xyz/installation](https://sherlockproject.xyz/installation)

## Usage

```bash
sherlock user123                  # one username
sherlock user1 user2 user3        # several
```

Results are written to a txt file per username (`user123.txt`).

### Options

| Flag | Effect |
| - | - |
| `-h`, `--help` | Show help |
| `--version` | Version and dependencies |
| `-v`, `-d`, `--verbose`, `--debug` | Extra debug output |
| `-fo`, `--folderoutput DIR` | Output folder for multiple usernames |
| `-o`, `--output FILE` | Output file for a single username |
| `--csv` / `--xlsx` / `--txt` | Also write CSV / XLSX / TXT |
| `--site NAME` | Limit to specific site(s), repeatable |
| `-p`, `--proxy URL` | e.g. `socks5://127.0.0.1:1080` |
| `--dump-response` | Print raw HTTP responses |
| `-j`, `--json FILE` | Load sites from a JSON file or upstream PR number |
| `--timeout SEC` | Request timeout (default 60) |
| `--print-all` / `--print-found` | Show misses / show hits |
| `--no-color` | Disable colored output |
| `-b`, `--browse` | Open all results in the browser |
| `-l`, `--local` | Force the local `data.json` |
| `--nsfw` | Include NSFW sites |
| `--ignore-exclusions` | Ignore upstream exclusions (more false positives) |

`USERNAMES` accepts `{?}` to also try `_`, `-` and `.` variants.

## Credits

Thanks to [everyone who contributed](https://github.com/sherlock-project/sherlock/graphs/contributors). ❤️

## License

MIT © Sherlock Project — created by [Siddharth Dushantha](https://github.com/sdushantha)
