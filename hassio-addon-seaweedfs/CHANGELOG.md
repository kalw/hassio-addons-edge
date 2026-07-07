- fix: raise volume count ceiling to stop uploads failing after 8 volumes

SeaweedFS defaults -volume.max to a fixed count of 8, unrelated to
actual free disk space. Once a node has 8 volumes (easily reached
with small default 30GB volume size and normal usage), the master
reports "0 node candidates" for any further volume growth and all
new uploads fail permanently, even with abundant free disk space.

Root cause confirmed via /vol/status on a production instance:
"Free":0,"Max":8 despite 163GB free on the host.

Fix: -volume.max=0 lets the volume count auto-scale with actual free
disk space, and -master.volumeSizeLimitMB=1000 (down from the 30GB
default) keeps individual volumes small so more of them fit, which
matters on typical HA installs with limited storage.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>
