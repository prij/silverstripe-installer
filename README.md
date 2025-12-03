# Silverstripe Installer

A Bash script that runs `composer create-project silverstripe/installer` and then prompts you to configure the `.env` file interactively for the following:

- Project directory (leave empty to install in current directory)
- Database server, username, password and name
- Environment type (dev/test/live)
- Admin username and password (optional)

It then creates the `.env` file and removes the `.env.example` that comes with Silverstripe.

## Requirements

- Bash 4.0+
- Composer
- PHP 8.1+

## Installation

```bash
curl -o [YOUR_BIN_PATH]/ss-install https://raw.githubusercontent.com/prij/silverstripe-installer/main/ss-install.sh
chmod +x [YOUR_BIN_PATH]/ss-install
```

## Usage

```bash
mkdir my-project
cd my-project
ss-install
```

Follow the prompts to configure your project directory, database and admin credentials.

## Installation notes

### Finding your bin path

To see which directories are in your PATH:

```bash
echo $PATH | tr ':' '\n'
```

Common locations include `~/bin`, `~/.local/bin`, or `/usr/local/bin`.

### If you don't have a bin folder

Create one and add it to your PATH:

```bash
mkdir -p ~/bin
echo 'export PATH="$HOME/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

Replace `.zshrc` with `.bashrc` if you're using Bash.

## Troubleshooting

### Command not found

Check if the bin folder is in your PATH:

```bash
echo $PATH | tr ':' '\n' | grep -E "(bin)"
```

If your bin folder isn't listed, add it to your PATH (see above).

### Permission denied

Make the script executable:

```bash
chmod +x [YOUR_BIN_PATH]/ss-install
```

## License

MIT