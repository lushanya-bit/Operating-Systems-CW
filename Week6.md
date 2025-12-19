# Week 6 - Performance Evaluation and Analysis

## Overview
This week focuses on understanding Linux file system structure. It explored how files are organised and managed.

## File System Structure and Organisation

### File System Hierarchy

![File System](images/week6/file_hierarchy.png)

The Linux file system hierarchy was explored to understand the role of each of the key directories listed:
- `/` - Root of the file system hierarchy
- `/etc` - System wide configuration files
- `/var` - variable data for eg. logs
- `/home` - user's home directories
- `/usr` - user applications and shared data
- `/tmp` - temporary files
- `/boot` - Bootloader and kernel files

### Inodes and Links**
**Metadata**
Metadata and inode information were examined. This revealed the file size, inode number, permissions, link count, and access timestamps.

**Hardlinks vs Symboliclinks**
-Hard links share the same inode number as the original file.
-Symbolic links have a different inode and reference to the original path file
