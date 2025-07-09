#!/bin/bash
set -e

echo "📦 Copying letter-prefixed files to ~/dotfiles (with backup)..."

mkdir -p ~/dotfiles

for file in [a-zA-Z]*; do
  [ -f "$file" ] || continue

  dest="$HOME/dotfiles/$file"

  if [ -f "$dest" ]; then
    echo "↪ Backing up $dest → $dest.bak"
    cp -f "$dest" "$dest.bak"
  fi

  echo "→ Copying $file → $dest"
  cp -f "$file" "$dest"
done

echo "✅ Done!"
