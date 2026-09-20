# 🔍 Port Detective

A Windows desktop developer utility that helps you find which process or application is using a TCP port on your computer.

Developers often face errors like:

> "Port 5000 is already in use."

Port Detective makes it easy to identify the process using the port and provides useful information such as the Process ID, process name, executable path, and connection details.

## ✨ Features

- 🔍 Find which process is using a specific port
- 📊 Scan a range of TCP ports
- 🆔 Display Process ID (PID)
- 📁 Display executable path
- 🔎 Search by port, PID, or process name
- 🔄 Refresh active ports
- 🛑 Stop a selected process with confirmation
- 📋 Copy PID, port, and process information
- 📂 Open process file location
- ⚡ Quick access to common developer ports
- 📝 Application logging
- ⚙️ Configurable settings
- 🔐 Safe process termination with confirmation
- 🚫 Handles permission and process errors gracefully

## 🛠️ Technologies

- C#
- .NET 8
- WPF
- MVVM
- Dependency Injection
- Windows APIs
- System.Diagnostics
- System.Net.NetworkInformation

## 🖥️ Supported Ports

Port Detective provides quick access to commonly used development ports:

```text
3000  - React / Node.js
4200  - Angular
5000  - .NET / Flask
5173  - Vite
5432  - PostgreSQL
6379  - Redis
8000  - Development servers
8080  - Java / Spring Boot
1433  - SQL Server
3306  - MySQL


📸 Screenshots

<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/617aeccc-bd19-40e9-879d-50425a990718" />


Add application screenshots here after the UI is complete.

Coming soon...
🚀 Getting Started
Prerequisites
Windows 10 or later
.NET 8 SDK
Clone the repository
git clone https://github.com/saurabhkumaryadav2001/PortDetective.git
Navigate to the project
cd PortDetective
Run the application
dotnet run
🔎 Example

Suppose your application fails with:

Unable to start application.
Port 5000 is already in use.

Open Port Detective and search:

5000

The application can show:

Port:       5000
PID:        8212
Process:    dotnet.exe
Status:     Running
Path:       C:\Projects\MyApi\MyApi.exe

You can then inspect the process or stop it after confirmation.

🏗️ Architecture
┌──────────────────────────────┐
│          WPF UI              │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│         ViewModels           │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│           Services           │
│                              │
│ Port Scanner                 │
│ Process Service              │
│ Port Monitor                 │
└──────────────┬───────────────┘
               ↓
┌──────────────────────────────┐
│      Windows/.NET APIs       │
└──────────────────────────────┘
🔐 Security

Port Detective does not automatically terminate processes.

A confirmation is required before stopping a process.

The application also validates port numbers and handles permission errors without crashing.

📦 Publish

To create a Windows release build:

dotnet publish -c Release -r win-x64 --self-contained true

The published application will be available under the bin directory.

🛣️ Future Improvements
 UDP port detection
 Docker container port detection
 IIS port detection
 Windows Service monitoring
 Export results to CSV
 System tray mode
 Start with Windows
 Port conflict notifications
 Network connection monitoring
 Dark/light theme
🤝 Contributing

Contributions, issues, and feature requests are welcome.

📄 License

This project is licensed under the MIT License.


---

# 2. Create `.gitignore`

Very important before pushing.

Create:

```text
.gitignore

Put:

bin/
obj/
.vs/
.idea/
*.user
*.suo
publish/
TestResults/

This prevents build files from going to GitHub.

3. Create GitHub repository

Go to GitHub.

Click:

New repository

Repository name:

PortDetective

Description:

A Windows developer utility for finding processes using TCP ports.

I recommend Public for your portfolio.

Don't select:

Add README
Add .gitignore
Add license

because you already created them locally.

Click:

Create repository

4. Open terminal in your project

Your folder should look approximately like:

PortDetective/
│
├── PortDetective.csproj
├── App.xaml
├── MainWindow.xaml
├── Models/
├── Services/
├── ViewModels/
├── Views/
├── README.md
└── .gitignore

Open this folder in VS Code and open:

Terminal → New Terminal

5. Initialize Git

Run:

git init

Then:

git add .

Check what will be committed:

git status

You should not see bin/ or obj/ files.

6. Create your first commit
git commit -m "Initial commit - Port Detective"

You should get something similar to:

[main abc1234] Initial commit - Port Detective
7. Connect your GitHub repository

GitHub will show you your repository URL.

It will look like:

git remote add origin https://github.com/YOUR_USERNAME/PortDetective.git

Then:

git branch -M main
8. Push 🚀

Finally:

git push -u origin main

You should see:

Enumerating objects...
Writing objects...
[new branch] main -> main

Then refresh your GitHub repository.

Your project should be there. 🎉

After pushing, your GitHub should look like:
PortDetective
│
├── Models/
├── Services/
├── ViewModels/
├── Views/
├── App.xaml
├── MainWindow.xaml
├── PortDetective.csproj
├── .gitignore
└── README.md

Important: Don't upload bin, obj, or your publish folder. Keep those out of GitHub using .gitignore.
