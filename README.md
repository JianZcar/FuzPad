<h1 align="center">📙FuzPad!</h1>

<p align="center">
    <em>FuzPad is a minimalistic note management solution. Powered by ⚡<a href="https://github.com/junegunn/fzf">junegunn/fzf</a></em>⚡
</p>
<p align="center">
    <a href="https://sourceforge.net/p/fuzpad/"><img alt="Download FuzPad" src="https://sourceforge.net/sflogo.php?type=17&amp;group_id=3845250" width=200></a>
    <br>
    <a href="https://sourceforge.net/projects/fuzpad/files/latest/download"><img alt="SourForgeDownloads" src="https://img.shields.io/sourceforge/dt/FuzPad?style=social&logo=sourceforge"></a>
    <a href="https://github.com/JianZcar/FuzPad/releases/latest"><img alt="GithubDownloads" src="https://img.shields.io/github/downloads/JianZcar/Fuzpad/total?style=social&logo=github"></a>
</p>
<p align="center">
    🎉 Over 400 Downloads 🎉
</p>

<p align="center">
    <img alt="Linux" src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black">
    <img alt="MacOS" src="https://img.shields.io/badge/mac%20os-000000?style=for-the-badge&logo=macos&logoColor=F0F0F0">
</p>

<p align="center">
    <img alt="ReleaseStatus" src="https://img.shields.io/github/actions/workflow/status/JianZcar/FuzPad/release.yml?label=Release">
    <img alt="HomebrewStatus" src="https://img.shields.io/github/actions/workflow/status/JianZcar/FuzPad/homebrew.yml?label=Homebrew">
    <br>
    <img alt="CommitsSinceLatestRelease" src="https://img.shields.io/github/commits-since/JianZcar/FuzPad/latest?style=social">
</p>

<p align="center">
    <img src="https://i.imgur.com/bSydyHY.png" alt="Sample Image" width="350"/>
    <br>
    <img src="https://i.imgur.com/x7BiCmn.png" alt="Sample Image" width="350"/>
    <img src="https://i.imgur.com/bQzZKsX.png" alt="Sample Image" width="350"/>
    <br>
    <img src="https://i.imgur.com/50qKVyw.png" alt="Sample Image" width="350"/>
    <img src="https://i.imgur.com/FsV69UX.png" alt="Sample Image" width="350"/>
</p>

[![Star History Chart](https://api.star-history.com/svg?repos=JianZcar/FuzPad&type=Date)](https://star-history.com/#JianZcar/FuzPad&Date)

## Features
- **New**: Create a new note with the current date and time as the filename.
- **Open**: Open an existing note.
- **Search**: Search within notes for specific content.
- **Delete**: Delete selected notes.
- **Version control**: Automatically commits changes to your notes.
- **Tags**: Tagging system to organize notes.
- **Icons**: Visual icons for better user experience.

## Planned Features
- **CLI**: Create a CLI that allows piping, etc.

## How to tag a note

1. **Create or Open a Note**: Select "New" to create a new note or "Open" to edit an existing note.
2. **Add a Tag**: In the note, ensure the tag is on the 2nd line right after the title. Use the format `#tag`. For example:
   ```
   My Note Title
   #important
   This is the content of the note.
   ```

This will help you organize and search your notes using tags.

## Goals

- Provide a straightforward and minimalistic note management solution using a Bash script.
- Ensure ease of use with intuitive commands and interface.

## Requirements

- Bash
- Git (optional)
- grep
- [fzf](https://github.com/junegunn/fzf) (fuzzy finder)(Latest)
- [bat](https://github.com/sharkdp/bat) (for enhanced preview)
- Your preferred text editor (default is `nano`)

## Installation

<p align="center">
    <a href="https://sourceforge.net/projects/fuzpad/files/latest/download"><img alt="Download FuzPad" src="https://a.fsdn.com/con/app/sf-download-button" width=276 height=48 srcset="https://a.fsdn.com/con/app/sf-download-button?button_size=2x 2x"></a>
</p>

### Using Homebrew

```sh
brew install JianZcar/packages/fuzpad
```

### Using curl

~/.local/bin should be in your PATH
```bash
curl -s https://gist.githubusercontent.com/JianZcar/df050e108b462e469f413f0eec229143/raw | bash
```

### Manual Installation

1. Clone the repository:

```sh
git clone https://github.com/JianZcar/FuzPad.git
cd FuzPad
```

2. Make the script executable:

```sh
chmod +x bin/fuzpad
```

3. Run the script:

```sh
./bin/fuzpad
```

## Configuration

- **Default Directory**: Change the default directory for notes by modifying the `FUZPAD_DIR` variable in the script or by setting it in your `~/.bashrc` file:
  ```sh
  export FUZPAD_DIR="$HOME/Documents/.notes"
  ```

- **Text Editor**: Change the text editor by modifying the `EDITOR` variable in the script or by setting it in your `~/.bashrc` file:
  ```sh
  export EDITOR="nano"
  ```

- **Text Format**: Change the text format by modifying the `TEXT_FORMAT` variable in the script or by setting it in your `~/.bashrc` file:
  ```sh
  export FUZPAD_TEXT_FORMAT="txt"
  ```

- **Date Time Format**: Change the date and time format used for note filenames by modifying the `DATE_TIME_FORMAT` variable in the script or by setting it in your `~/.bashrc` file:
  ```sh
  export FUZPAD_DATE_TIME_FORMAT="%Y-%m-%d-%H-%M-%S"
  ```

- **BAT Theme**: Change the theme used by `bat` for previewing notes by modifying the `BAT_THEME` variable in the script or by setting it in your `~/.bashrc` file:
  ```sh
  export FUZPAD_BAT_THEME="OneHalfLight"
  ```

- **Reverse List**: Set to `true` to reverse the order of the list when opening or deleting notes by modifying the `REVERSE_LIST` variable in the script or by setting it in your `~/.bashrc` file:
  ```sh
  export FUZPAD_REVERSE_LIST="false"
  ```

- **Preview Size**: Change the size of the preview window for `fzf` by modifying the `PREVIEW_SIZE` variable in the script or by setting it in your `~/.bashrc` file:
  ```sh
  export FUZPAD_PREVIEW_SIZE="70%"
  ```

- **Start Line Search Preview**: Set the starting line number for the search preview by modifying the `START_LINE_SEARCH_PREVIEW` variable in the script or by setting it in your `~/.bashrc` file:
  ```sh
  export FUZPAD_START_LINE_SEARCH_PREVIEW="5"
  ```

- **End Line Search Preview**: Set the ending line number for the search preview by modifying the `END_LINE_SEARCH_PREVIEW` variable in the script or by setting it in your `~/.bashrc` file:
  ```sh
  export FUZPAD_END_LINE_SEARCH_PREVIEW="9999"
  ```

- **Icons**: Turn icons on or off by modifying the `FUZPAD_ICON` variable in the script or by setting it in your `~/.bashrc` file:
  ```sh
  export FUZPAD_ICON="1"  # Set to "0" to turn off icons
  ```

After adding the necessary variables to your `~/.bashrc` file, remember to source it to apply the changes:
```sh
source ~/.bashrc
```

## Updates

- **Major Updates**: No clear dates at the moment.
- **Minor Updates**: No clear dates at the moment.
- **Patch Updates**: Released as soon as possible.

## Support
- ⭐ If you like the project, please leave a star!
- 💖 Consider becoming a sponsor to support ongoing development.

## Contributing

We welcome contributions from the community! Please refer to the [Contributing Guidelines](CONTRIBUTING.md) for more details on how to get started.

Feel free to fork the repository and submit pull requests. Contributions are welcome!

## License

This project is licensed under the terms of the GNU General Public License v3.0. For more details, see the [LICENSE](LICENSE) file in the repository.
