# Speedrun.com Data Exporter Documentation

## Introduction
### What is the Speedrun.com Data Exporter

The **Speedrun.com Data Exporter** is a command-line tool designed to simplify retrieving and exporting data from the **Speedrun.com API**. Instead of manually writing complex API requests, handling pagination, and managing throttling limits, this tool does everything for you—fetching the data you need and exporting it to easy-to-use **CSV files**.

Whether you're a **developer, researcher, or speedrunning enthusiast**, this tool allows you to extract and work with **runs, categories, and more** from Speedrun.com **without diving into API intricacies.**

### Why should you use it?

- **Seamless Integration:** Perfect for projects that require **Speedrun.com data**. Retrieve the exact data you need and output it into a structured CSV file that can be easily passed into your own **tools, scripts, or databases.**

- **Ease of Use:** No need to learn the details of the **Speedrun.com API.** Just specify what you want, and the tool fetches it.

- **Automated Data Retrieval:** Great for tasks that require **frequent or large-scale data extraction.** Automate tedious processes that would take hours manually.

- **Faster Development:** Spend time working **with** the data instead of **writing API boilerplate code.**

- **Pagination & Throttling Management:** The tool automatically handles **pagination** for large requests and **respects throttling limits** to ensure smooth data retrieval.

- **Perfect for Testing:** Quickly fetch **Speedrun.com data** for testing before integrating it into your production environment.

### What Can It Do?

Currently, the **Speedrun.com Data Exporter** can:

- Retrieve runs for any game in the Speedrun.com API (including pagination and verified runs only).

- Retrieve categories for any game.

- Export the data into CSV files for easy integration into your own projects.


And this is just the beginning! Future updates will include more request types, filtering options, and extended API support.

# Installation

The **Speedrun.com Data Exporter** requires **Go 1.23.0 or later**. You can install it in two ways:

- **By compiling from source** (recommended for latest updates)

- **Using precompiled binaries** (for a quick setup)

## Installation on Linux & macOS

This section covers **Linux (Ubuntu, Debian, Arch, Fedora, etc.)** and **macOS.**

### Installing via Source (Recommended)

If you want the latest version, compile it from source.

#### Step 1: Install Go (1.23.0 or later)

- Download Go from the [official website](https://go.dev/)

- Alternatively, install it via a package manager:

  **Ubuntu/Debian:**
  
    ```bash
    sudo apt install golang
    ```

  **Arch Linux:**

    ```bash
    sudo pacman -S go
    ```

  **Fedora:**

    ```bash
    sudo dnf install golang
    ```

  **MacOS (Homebrew):**

    ```bash
    brew install go
    ```

- Verify installation:

```bash
go version
```
  
  Should return something like this:
  
```bash
go version go1.23.0 linux/amd64
```

#### Step 2: Clone the Repository

```bash
git clone https://github.com/Comichimera/Speedrundotcom-data-exporter.git
cd Speedrundotcom-data-exporter
```

#### Step 3: Build the Executable

```bash
go build -o sdcde
```

#### Step 4: Move to a System Path (Optional)

For easier access, move the binary to /usr/local/bin/:

```bash
sudo mv sdcde /usr/local/bin/
```

Now, you can run it from anywhere using:

```bash
sdcde --help
```

#### Step 5: Run the program

```bash
./sdcde --help
```

### Installing via Precompiled Binary

If you don’t want to compile from source, use a prebuilt binary.

#### Step 1: Download the Binary

- Go to [GitHub Releases](https://github.com/Comichimera/Speedrundotcom-data-exporter/releases)

- Download `sdcde-linux-amd64` (Linux) or `sdcde-macos-amd64` (macOS).

#### Step 2: Make it Executable

```bash
chmod +x sdcde-linux-amd64
```

#### Step 3: Move to a System Path (Optional)

```bash
sudo mv sdcde-linux-amd64 /usr/local/bin/sdcde
```

Now, you can use it anywhere:

```bash
sdcde --help
```

#### Step 4: Run the Program

```bash
./sdcde --help
```

## Installation on Windows

Windows users can install via **source (recommended)** or **precompiled binaries**.

### Installing via Source (Recommended)

#### Step 1: Install Go (1.23.0 or later)

- Download Go for **Windows** from the [official site](https://go.dev/) and install it.

- Verify installation:

```shell
go version
```

Should output something like:

```shell
go version go1.23.0 windows/amd64
```

#### Step 2: Clone the Repository

Open **Command Prompt** (cmd) or **PowerShell**, then run:

```shell
git clone https://github.com/Comichimera/Speedrundotcom-data-exporter.git
cd Speedrundotcom-data-exporter
```

#### Step 3: Build the Executable

```shell
go build -o sdcde.exe
```

#### Step 4: Run the Program

```shell
.\sdcde.exe --help
```

### Installing via Precompiled Binary

If you prefer a quick setup, use a **precompiled binary**.

#### Step 1: Download the Binary

- Go to [GitHub Releases](https://github.com/Comichimera/Speedrundotcom-data-exporter/releases)

- Download `sdcde-windows-amd64.exe`.

#### Step 2: Move to an Easy-to-Use Location

Move `sdcde-windows-amd64.exe` to a folder like `C:\sdcde\` or `C:\Program Files\`.

### Add to System PATH (optional)

For easier use, add the folder to your system’s PATH:

1. Open **Start Menu** > Search **"Environment Variables".**

2. Click **"Edit the system environment variables".**

3. Under **System Properties,** click **"Environment Variables".**

4. Find **"Path"**, click **Edit**, and add the folder where you saved `sdcde.exe` (e.g., `C:\sdcde\`).

5. Click **OK** to save.

Now, you can run the program from any location in Command Prompt or PowerShell:

```shell
sdcde.exe --help
```

#### Step 4: Run the Program

If you didn’t add it to PATH, navigate to the folder where you downloaded it:

```shell
cd C:\sdcde\
.\sdcde-windows-amd64.exe --help
```
