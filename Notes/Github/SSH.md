---
aliases: 
tags: 
date created: Sunday, August 18th 2024, 11:13:44 pm
date modified: Sunday, August 18th 2024, 11:20:29 pm
---
SSH significa secure shell, ao qual é um fluxo que permite que você não precise digitar seu email e sua senha toda hora que precisa interagir com o git, tornando assim os fluxos mais rápidos e dinâmicos.

Aqui exemplifica um fluxo em ingles de como configurar sua chave SSH (gerado pelo CHAT GPT):

To generate an SSH key pair on Windows 11, you can follow these steps:

### Step 1: Open Windows Terminal or Command Prompt
1. **Right-click** the Start button and select **Windows Terminal** or **Command Prompt** from the menu.

### Step 2: Generate the SSH Key Pair
1. In the terminal or command prompt, type the following command:
   ```bash
   ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
   ```
   - `-t rsa`: Specifies the type of key to create (RSA in this case).
   - `-b 4096`: Specifies the length of the key in bits (4096 bits is a common choice for RSA).
   - `-C "your_email@example.com"`: Provides a comment to identify the key (usually your email).

2. Press **Enter**. The command will prompt you to specify the file where the key will be saved:
   ```
   Enter file in which to save the key (C:\Users\YourName/.ssh/id_rsa):
   ```
   - Press **Enter** to save it in the default location (`C:\Users\YourName/.ssh/id_rsa`).

3. Next, you'll be prompted to enter a passphrase:
   ```
   Enter passphrase (empty for no passphrase):
   ```
   - You can enter a passphrase for added security or press **Enter** to leave it empty for no passphrase.

### Step 3: Add the SSH Key to the SSH Agent
1. Start the SSH agent by running the following command in the terminal:
   ```bash
   eval $(ssh-agent -s)
   ```
2. Add your SSH private key to the SSH agent:
   ```bash
   ssh-add ~/.ssh/id_rsa
   ```

### Step 4: Copy the SSH Public Key to the Clipboard
1. To copy the public key to the clipboard, use the following command:
   ```bash
   clip < ~/.ssh/id_rsa.pub
   ```
   - This copies the content of your public key (`id_rsa.pub`) to the clipboard.

### Step 5: Add Your SSH Key to a Service (e.g., GitHub, GitLab)
1. **Login** to the service (e.g., GitHub, GitLab).
2. Navigate to **SSH and GPG keys** under your account settings.
3. Click **New SSH key** (GitHub) or **Add SSH Key** (GitLab).
4. **Paste** the public key from your clipboard into the key field.
5. **Save** the key.

### Step 6: Test the SSH Connection
1. Test your connection to the service using:
   ```bash
   ssh -T git@github.com
   ```
   - Replace `git@github.com` with the appropriate URL for other services like GitLab.
2. You should see a message like:
   ```
   Hi username! You've successfully authenticated, but GitHub does not provide shell access.
   ```

You're now ready to use SSH on Windows 11 for secure connections to various services!