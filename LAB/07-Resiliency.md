# 1. Backups
- Windows Server Backup, "a **periodic scheduled backup** is more likely to be used in a real-world scenario"
- Volume Shadow Copy Service (VSS), Previous Version, Volume Shadow Copy Service (VSS) will retain previous versions of files, but it is **not a backup**. If a file is removed **from a drive**, the VSS cannot be used to restore it. However, Windows File History and potentially a system restore point can be used to restore lost files.
- Recycle Bin

**How much data can be lost and still be able to restore business functions**
**BP: Store essential backups offsit**

```shell
diskpart
select disk 1
online
attribute disk clear readonly
create partition primary
format fs=nfs label="Backup01" quick
assign letter=f

wmic shadowcopy call create Volume=c:\
```

# 2. Drive Sanitizatino
- Deletion and formatting are not specifically data destruction operations. A deletion marks a file's **storage locations** (typically clusters, a.k.a. allocation unit, storage allocation unit, or storage node, on an HDD or a block on an SSD) as **available for re-use** but does not actually remove the original data. Formatting does this across an entire partition. As long as the data clusters/blocks are not overwritten, the data is typically recoverable. To truly remove data, it needs to be overwritten by something else.
- (-z) add a final orverwrite with zero
- **The contents of the directory structure still retain** the filenames from the Passwords directory.
- **formatting is not considered a secure sanitization** or data destruction technique.


**Overwriteing** is primary way to sanitize
**Remnants** refered to material that might be **recoverbale**

```shell
testdisk
shred
dd if=/dev/zero of=/dev/sdb bs=1M status=progress
dd if=/dev/random of=/dev/sdb bs=1M status=progress
```