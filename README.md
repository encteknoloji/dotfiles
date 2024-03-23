# 🔧  .files used by ENC Teknoloji

[chezmoi](https://www.chezmoi.io) should be downloaded and installed for .file management. Initialization can be done with the following command after the program installation:

    chezmoi init --apply encteknoloji

## On Click Install

As you may not have [chezmoi](https://www.chezmoi.io) installed, you may use following one-line command to install and initialize .files:

    sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply encteknoloji

## Adding Files

A new file can be added with the following command:

chezmoi add ~/.bashrc

To send the added file to the git repository, the following commands can be used:

    chezmoi cd
    git add .
    git commit -m "Added .bashrc file"
    git push

## Editing Files

If a previously added file needs to be edited, the following command can be used:

    chezmoi edit --apply ~/.bashrc

This command opens the file in an editor for editing. When exiting the editor, it reflects the changes to the original file as well.

Alternatively, a re-added original file can be edited with the following command:

    chezmoi re-add ~/.bashrc

## Examining Differences

Differences between files in the git repository and files on your local system can be examined with the following command:

    chezmoi diff

The differences observed in the comparison can be applied to the local with the following command:

    chezmoi -v apply

## Applying Updates

To apply changes from the git repository locally by pulling the changes, the following command can be used:

    chezmoi update -v