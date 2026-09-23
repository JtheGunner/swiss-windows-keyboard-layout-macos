# Swiss Windows Keyboard Layout for macOS

This repository contains a custom keyboard layout configuration for macOS. It allows you to use the German (Switzerland) keyboard layout from Microsoft Windows systems on your Mac.

## Installation and Usage

1. **Download the layout**  
   Download the files from this repository.

2. **Install the layout**  
   Copy both files to `/Library/Keyboard Layouts/`:

    ```bash
    sudo cp CustomSwissGerman.* /Library/Keyboard\ Layouts
    ```

    You will need administrator privileges for this.

3. **Activate the layout**
    - Open System Preferences → Keyboard → Input Sources.
    - Click the plus sign (+) and select the new layout from the list.
    - Add the layout and make sure it is selected.

4. **Restart your Mac**  
   Restart your Mac to ensure the layout is applied correctly.

## Notes

- The layout is based on the German (Switzerland) layout from Windows and enables a seamless transition for users switching from Windows to macOS.
- The basis for this layout comes from the repository [weibeld-setup/install-keyboard-layout](https://github.com/weibeld-setup/install-keyboard-layout). Many thanks to the original project!

## Contributing

Issues and pull requests are welcome — for example, missing or wrong key
mappings.

## License

[MIT](LICENSE)
