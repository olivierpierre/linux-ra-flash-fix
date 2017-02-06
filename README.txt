Linux patch for JFFS2 / YAFFS2 readahead disabling
==================================================
07/24/2013 - Pierre Olivier <pierre.olivier@univ-brest.fr>

The JFFS2 patch must be applied on a vanilla kernel version. As YAFFS2 is not included in the kernel mainline, one must first have a kernel patched with YAFFS2, then apply this patch.

JFFS2 patch is based on 2.6.37.1. YAFFS2 patch is based on 2.6.37.1 + latest YAFFS2 (commit reference was 'bc76682d93955cfb33051beb503ad9f8a5450578' at this time).

Applying the patches:
=====================
For jffs2: just place jffs2_disable_readahead.patch at the root of your kernel source tree and type 'patch -p1 < jffs2_disable_readahead.patch'
For yaffs2: make sure your kernel source tree is patched with YAFFS2, place yaffs2_disable_readahead.patch at the root level and type 'patch -p1 < yaffs_disable_readahead.patch'