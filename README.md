# Locale en_PK

## Usage

1. Place the locale file (`en_PK`) under the system locales directory, typically `/usr/share/i18n/locales/`.

```
# cp ./en_PK /usr/share/i18n/locales/
```

2. Add the line `en_PK.UTF-8 UTF-8` to your supported locales file (typically `/usr/share/i18n/SUPPORTED`), preferrably in an alphabetically ascending way. For example, I had to add mine between `en_PH` and `en_SC`:

```
...
en_PH ISO-8859-1
en_PK.UTF-8 UTF-8
en_SC.UTF-8 UTF-8
...
```

3. Add the line `en_PK.UTF-8 UTF-8` to `/etc/locale.gen`.

```
# echo 'en_PK.UTF-8 UTF-8' >> /etc/locale.gen
$ # OR:
$ echo 'en_PK.UTF-8 UTF-8' | sudo tee -a /etc/locale.gen
```

4. Use `locale-gen` to regenerate your system locales.

```
# locale-gen
```

5. Set your locale values to `en_PK.UTF-8` and reboot (sometimes, re-login is enough). Locale settings can be set in special local files or in your profile files. Some *NIXs and some DEs have their own locations for locale files. Read their documentation or search online if the following files don't work for you:

Locale files can be found at (in no order):
- `/etc/locale.conf`
- `/etc/default/locale`
- `$XDG_CONFIG_HOME/locale.conf`
- `~/.config/locale.conf` (usually same as above file)
- etc.

Profile files:
- `/etc/profile`
- `/etc/profile.d/*`
- `~/.bash_profile`
- `~/.zprofile`
- etc.

## Note

This Project is NOT part of the GNU C Library. It is NOT affiliated with the Free Software Foundation in any way. It contains a file containing locale data originally written for private use by the Author of this Project, malijaffri. As such, it is provided AS IS, and the Author holds NO liability for any other use of this Project. This Project is Copyright of malijaffri, 2024. It is released under the BSD 3-Clause License, a copy of which is also provided. Anyone may use this Project, with or without modification, provided that they uphold the terms outlined in the aforementioned License.

## Copyright

Copyright (c) 2024, malijaffri

This project is Copyright of malijaffri, 2024, and is released under the BSD 3-Clause License (copy provided). Anyone is free to use, modify, and redistribute this locale as they see fit, as long as the do so under the terms of the aforementioned License, as well as keep the copyright notice embedded inside the locale (as comments) intact. It would be preferrable to keep the original License file with it, but it is acknowledged that that may not be possible under normal personal use (locales directory).
