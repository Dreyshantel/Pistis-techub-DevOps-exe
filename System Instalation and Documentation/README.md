# System Installation and Documentation
This is a comprehensive documentation on how i installed and configure a development enviroment.  First of, i created a GitHub account by navigating to the GitHub website and selecting the **Sign up** option. The required details, including an email address, username, and password, were entered, followed by completing the verification steps. The **Free** plan was selected during the setup process, and the email address was verified to finalize the account creation. Upon completion of these steps, the GitHub account was successfully created. Afterward, Chocolatey, a Windows package manager, was installed to enable software installation through the command line. This was done by opening Windows PowerShell with administrative privileges from the Start menu. An installation command was then executed in PowerShell, which configured the execution policy and downloaded and installed Chocolatey from its official source. Upon completion, Chocolatey was successfully installed and ready for use.

```
Set-ExecutionPolicy Bypass -Scope Process -Force; 
[System.Net.ServicePointManager]::SecurityProtocol = 
[System.Net.ServicePointManager]::SecurityProtocol -bor 3072; 
iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```
<img width="1920" height="909" alt="image" src="https://github.com/user-attachments/assets/a88621a3-c45a-4320-80f9-162e35590e64" />



Once i am done with the installation, i verified if chocolatey was verified by cheking using the `choco --version` command.


Moving on, i installed Windows Terminal using the command-line interface by executing the appropriate Chocolatey installation command. After the installation completed successfully, Windows Terminal was launched from the Start menu to confirm that it was properly installed and ready for use. Futhermore, Git, the version control system that allows us to track our application versions, work and collaborate seamlessly as developers was required for use with GitHub, it was installed using the command-line interface through Chocolatey.  After the installation completed, the installation was verified by checking the Git version from the command line, confirming that Git was successfully installed and available for use.

<img width="1888" height="1003" alt="image" src="https://github.com/user-attachments/assets/549a8e8b-d7f9-485c-ac48-eb11225922fc" />



## Install Visual Studio Code and Openssh (VS Code)
To set up my development environment, I installed and opened Visual Studio Code and navigated to the Extensions view by clicking the Extensions icon on the left sidebar. From there, I installed the required extensions, namely **GitHub Pull Requests and Issues and Markdown All in One**, to support version control collaboration and Markdown documentation. After completing the VS Code extension setup, I proceeded to install OpenSSH using Chocolatey by running the command choco install openssh -y in the terminal. Once the installation was completed, I verified that OpenSSH was successfully installed by checking the SSH version with the command ssh -V.

<img width="1896" height="1063" alt="image" src="https://github.com/user-attachments/assets/d464f4ef-f8f5-4129-85d4-363de52fe865" />
<img width="1905" height="982" alt="image" src="https://github.com/user-attachments/assets/7cc749ff-c7fd-4c85-8a31-7ab9ae0f905b" />

After the successful installation and configuration of VScode, i installed openSSH using the Chocolatey package manager to enable secure, encrypted communication between the local development environment and GitHub. Prior to installation, the presence of SSH was checked using the ssh -V command to determine whether OpenSSH was already installed. Since SSH was not available or required an update, the installation was performed by running choco install openssh -y, which automatically downloaded and configured the necessary components. During the installation process, administrative privileges were required, and Chocolatey added OpenSSH to the system PATH to ensure global access from the command line. After installation, the SSH version was verified again using ssh -V, confirming that OpenSSH was successfully installed and ready for authentication with GitHub using SSH keys, allowing repositories to be securely cloned, accessed, and updated without repeatedly entering credentials.

<img width="1920" height="1031" alt="image" src="https://github.com/user-attachments/assets/68c4a9ab-fcca-43f8-aa6d-b3478773035e" />
<img width="821" height="195" alt="image" src="https://github.com/user-attachments/assets/9970a443-b98d-447f-b21f-81ce05d192f3" />

## Generate SSH Keys and configuring ssh-agent
I generated an SSH key pair using the Ed25519 algorithm, accepting the default file location and optionally setting a passphrase. The successful creation of the keys was confirmed by verifying the presence of `id_ed25519` and `id_ed25519.pub` in the **~/.ssh** directory. Also, the SSH agent was started, and the private key was added to the ssh-agent. The loaded keys were then verified, completing the SSH configuration required for secure GitHub authentication. Through this process, I learned how SSH enables secure, passwordless authentication with GitHub, how SSH agents manage private keys, and how to verify successful key-based access using the command line.

<img width="1910" height="770" alt="image" src="https://github.com/user-attachments/assets/c3f1cf39-50d8-4644-ad6f-a87d2dfd024f" />


I created a new GitHub repository named **Pistis-techub** by selecting New repository, choosing the desired visibility (public), and leaving the repository uninitialized (no README). The repository was then cloned locally using the SSH URL obtained from GitHub. After cloning the repo, Visual Studio Code was opened in the project directory, and a README.md file was created to document the setup process. The changes were reviewed using git status, staged with git add ., which i committed with an appropriate message, and finally pushed to GitHub, making the documentation available in the remote repository.
<img width="987" height="574" alt="image" src="https://github.com/user-attachments/assets/847c16b4-93c6-4285-aa39-e845015fc871" />
