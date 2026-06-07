# Capture Failed

Capture failed: Failed to launch the browser process:  Code: 127

stderr:
/root/.cache/hyperframes/chrome/chrome-headless-shell/linux-131.0.6778.85/chrome-headless-shell-linux64/chrome-headless-shell: error while loading shared libraries: libnss3.so: cannot open shared object file: No such file or directory

TROUBLESHOOTING: https://pptr.dev/troubleshooting


URL: https://bitbase.com

## What to try

- Re-run with a longer timeout: `--timeout 60000`
- The site may block headless browsers (anti-bot protection)
- Try capturing a different page on the same domain
