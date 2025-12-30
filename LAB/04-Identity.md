# 1.Authentication
- spray (hydra) > avoid lockout
- dictionary (), KALI: xato-net-10-million-passwords.txt 
- **Despite the existence of known weaknesses, NTLM is still commonly used,** even on new systems, to guarantee compatibility with legacy clients and servers.
- NIST Special Publication 800-63B: Digital Identity Guidelines: Authentication and Lifecycle Management: (https://pages.nist.gov/800-63-3/sp800-63b.html).

```shell
john --format=NT --wordlist=/usr/share/seclists/Passwords/xato-net-10-million-passwords.txt ms10-hashes.txt
john --show --format=NT ms10-hashes.txt > dict-cracked.txt
john --show=left --format=NT ms10-hashes.txt

rm ~/.john/john.pot


Get-ADDefaultDomainPasswordPolicy
Get-ADUser -Filter * | Set-ADUser -PasswordNeverExpires $False
Get-ADUser -Filter * | Set-ADUser -ChangePasswordAtLogon $True

```

# 2.Authorization
- Integrity Control Access Control List.
- The Security tab displays a summary of the NTFS permissions currently defined on the file. These permissions have been inherited from the parent folder.
-In Windows networking, there is a distinction between Share Permissions and NTFS (Security) Permissions.
    - Share Permissions: These only apply when a user accesses a folder over the network. **There are only three options: Read, Change, and Full Control.** "Modify" does not exist as a standard Share permission.
    - NTFS Permissions: These are the local file permissions (what you see in the icacls image). These include Read, Write, Modify, and Full Control.


| Abbreviation | Meaning       | Description                          |
|-------------|---------------|--------------------------------------|
| F           | Full Access   | Complete control over the file/folder. |
| M           | Modify Access | Can read, write, and delete the file. |
| RX          | Read & Execute| Can read contents and run executable files. |
| R           | Read-Only     | Can only view file contents.         |
| W           | Write-Only    | Can only write data to the file.     |

| Abbreviation | Meaning | Description |
|-------------|---------|-------------|
| (I)         | Inherited | Inherited from the parent folder. |
| (OI)        | Object Inherit | Files created in this folder will inherit this ACE. |
| (CI)        | Container Inherit | Subfolders created in this folder will inherit this ACE. |
| (IO)        | Inherit Only | Permission does not apply to the current object, only to children. |

```shell
icacls .\comptia-logo.jpg /deny dylan:R    
icacls .\comptia-logo.jpg /grant dylan:F
icacls .\comptia-logo.jpg /remove:g dylan

Grant-SmbShareAccess -Name "LABFILES" -AccountName "dylan" -AccessRight Change

```

