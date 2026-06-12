# Day 13 - File and Folder Transfer in Linux

## Objective

Today I learned different methods to transfer files between local systems and Linux servers securely.

File transfer is an important concept in Linux administration, cloud environments, and DevOps workflows.

---

# 1. File Transfer Using MobaXterm

MobaXterm provides a graphical way to upload and download files.

## Steps

1. Connect to the Linux server using SSH.
2. Open the SFTP panel.
3. Use Upload to send files to the server.
4. Use Download to retrieve files from the server.

This method is beginner-friendly and easy for managing files.

<img width="1918" height="948" alt="Screenshot 2026-06-12 191405" src="https://github.com/user-attachments/assets/1875e02a-3632-4a0d-83ac-b0ddcd8d3069" />


---

# 2. File Transfer Using WinSCP

WinSCP is another GUI-based tool used to transfer files securely.

## Steps

1. Open WinSCP.
2. Enter:

   * Server IP Address
   * Username
   * PEM Key (if required)
3. Connect to the server.
4. Upload or download files using drag-and-drop.

WinSCP uses secure protocols like SFTP and SCP.

---

# 3. SFTP (Secure File Transfer Protocol)

SFTP is used to transfer files securely between systems.

## Syntax

```bash
sftp -i <pem-file> username@server-ip
```

Upload a file:

```bash
put filename
```

Example:

```bash
sftp -i Myserv2.pem ubuntu@25.xx.xx.xx
put .Omg
```

You can also automate upload operations.
<img width="1605" height="980" alt="Screenshot 2026-06-12 235213" src="https://github.com/user-attachments/assets/fedb6891-dc53-402b-80fc-b8db98558fa3" />
<img width="1482" height="931" alt="Screenshot 2026-06-12 235750" src="https://github.com/user-attachments/assets/96197563-eb58-47c3-a0e0-0a5ee117828e" />


---

# 4. SCP (Secure Copy)

SCP is used to securely copy files between systems.

## Syntax

```bash
scp -i <pem-file> source destination
```

Example:

```bash
scp -i Myserv1.pem /home/ec2-user/file.txt ubuntu@25.xx.xx.xx:/home/ubuntu/
```

Example:

```bash
scp -i Myserv1.pem /home/ec2-user/file.txt ubuntu@25.xx.xx.xx:/home/ubuntu/
```<img width="1482" height="931" alt="Screenshot 2026-06-12 235750" src="https://github.com/user-attachments/assets/83cba370-3ae1-4ff5-a9ba-3fde7b7c8b8f" />


---

# Difference Between SFTP and SCP

| SFTP                            | SCP                     |
| ------------------------------- | ----------------------- |
| Interactive file transfer       | Direct file copy        |
| Supports navigation             | Faster for quick copy   |
| Allows upload/download sessions | Single command transfer |

---

# Key Takeaways

Today I learned:

* Uploading and downloading files using MobaXterm
* Connecting and transferring files using WinSCP
* Using SFTP for secure file transfer
* Using SCP for secure file copying

These commands are commonly used in Linux administration, cloud environments, and DevOps workflows.
