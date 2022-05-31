# GUFI Filesystem Traces
----
The GUFI Filesystem Traces are a series of formatted text files containing metadata taken from
the filesystems of LANL HPC systems. Each line is an entry from the filesystem, containing the entry's
name, stat(2) data, link name (if applicable), several filesystem specific fields (unused in these traces),
and the entry's pinode. The entry name, link name, uid, and gid fields have been anonymized to
preserve privacy. These traces allow for source filesystem trees (without any file contents) to be
regenerated in various ways, allowing for experiments with filesystem metadata from real HPC systems
without needing access to the real filesystems. yellusers is a scan of the yellow NFS home directory from
April 2019. yellprojs is a scan of the yellow NFS projects directory from April 2019. ttscratch and anony
are Trinitite user scratch space scans from March 2019 and April 2019, respectively. scr4 is from the
yellow Lustre scratch space in June 2020.

LA-UR-21-21017

# Reconstruction
----
This repository contains the bz2 file found at ftp://hpc-ftp.lanl.gov/data/storage/GUFI/GUFITraces.tar.bz2
split into 1GB files and uploaded through Git LFS. To reconstruct the bz2 file, cat the files together.

# Usage
----
After extracting the traces, use `gufi_trace2index` from the
[Grand Unified File Index](https://github.com/mar-file-system/GUFI) to
build indicies.
