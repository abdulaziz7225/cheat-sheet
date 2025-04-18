# Linux related useful information

## 🧹 Basic Clean-up Commands

1. **Remove orphaned dependencies** (packages that were installed as dependencies but are no longer needed):

   ```bash
   sudo apt autoremove
   ```

2. **Clean up downloaded `.deb` files** from `/var/cache/apt/archives`:

   ```bash
   sudo apt clean
   ```

3. **Remove obsolete package entries** from the local cache:

   ```bash
   sudo apt autoclean
   ```

---

## 🔍 Find and Remove Manually Installed Packages (Optional & Advanced)

1. **List all manually installed packages** (this includes packages that were explicitly installed):

   ```bash
   apt-mark showmanual
   ```

   You can go through this list and decide which ones you no longer need.

2. **Check what a package depends on** before removing it:

   ```bash
   apt depends <package-name>
   ```

3. **Remove a specific package** (e.g., an unused text editor):

   ```bash
   sudo apt remove <package-name>
   ```

   or if you want to remove configuration files too:

   ```bash
   sudo apt purge <package-name>
   ```

---

## 🧰 Remove Snap Packages (if you ever installed them)

WSL doesn't ship with Snap by default, but if you've used it:

```bash
snap list   # List installed snap packages
sudo snap remove <package-name>
```

---

## 📦 Identify Large Packages

To find what’s taking up space:

```bash
dpkg-query -Wf '${Installed-Size}\t${Package}\n' | sort -n | tail -n 20
```

This will show the 20 largest packages installed. You can check if any of them are unnecessary.

---

## 🧪 Optional: Use `deborphan` to find orphaned libraries

```bash
sudo apt install deborphan
deborphan
```

This will list unused libraries. You can remove them with:

```bash
sudo apt remove --purge $(deborphan)
```

> ⚠️ **Be cautious** with `deborphan`—review the packages before removing them.

---
