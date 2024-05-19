## **📌 Getting Started with Installing and Using Git**

> 📣 아래 글은 GPT-4를 이용하여 작성한 글이다. <br>작성자가 아래 유투브를 이용하여 정리한 글은 **🔥[블로그 바로가기](https://blog.naver.com/zzzxxx3166/223449846508)** 에서 볼 수 있습니다!!<br>
> [Git으로 시작하는 협업 및 오픈소스 프로젝트](https://www.youtube.com/playlist?list=PLRx0vPvlEmdD5FLIdwTM4mKBgyjv4no81) 를 공부하여 Git의 설치부터 활용 방법까지 단계별로 배워보자 !

# Getting Started with Installing and Using Git

## Installing Git

### On Windows:
1. **Download the Git installer**:
   - Go to the [Git official website](https://git-scm.com/).
   - Click on "Download" and select the version for Windows.
2. **Run the installer**:
   - Open the downloaded `.exe` file.
   - Follow the installation instructions. You can use the default settings unless you have specific preferences.
3. **Verify the installation**:
   - Open Command Prompt (you can search for "cmd" in the Start menu).
   - Type `git --version` and press Enter. You should see the installed Git version.

### On macOS:
1. **Using Homebrew (recommended)**:
   - If you don’t have Homebrew installed, install it by running this command in Terminal:
     ```sh
     /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
     ```
   - Once Homebrew is installed, run:
     ```sh
     brew install git
     ```
2. **Verify the installation**:
   - Open Terminal.
   - Type `git --version` and press Enter. You should see the installed Git version.

### On Linux:
1. **Using the package manager**:
   - For Debian/Ubuntu-based distributions:
     ```sh
     sudo apt update
     sudo apt install git
     ```
   - For Fedora-based distributions:
     ```sh
     sudo dnf install git
     ```
2. **Verify the installation**:
   - Open Terminal.
   - Type `git --version` and press Enter. You should see the installed Git version.

## Getting Started with Git

### Configuring Git:
1. **Set your username**:
   ~~~sh
   git config --global user.name "Your Name"
   ~~~
2. **Set your email**:
   ~~~sh
   git config --global user.name "Your Name"
   ~~~

## Basic Git Commands:
1. **Initialize a new Git repository**:
    - Navigate to your project directory in the terminal and run:
    ~~~sh
    git init
    ~~~

2. **Clone an existing repository**:
    - To clone a repository from GitHub, use:
    ~~~sh
    git clone https://github.com/username/repository.git
    ~~~

3. **Check the status of your repository**:
    ~~~sh
    git status
    ~~~

4. **Add changes to the staging area**:
    - To add a specific file:
    ~~~sh
    git add filename
    ~~~
    - To add all changes:
    ~~~sh
    git add .
    ~~~

5. **Commit changes**:
    - To commit with a message:
    ~~~sh
    git commit -m "Your commit message"
    ~~~

6. **Push changes to a remote repository**:
    - First, ensure you have a remote repository set up. To add a remote origin:
    ~~~sh
    git remote add origin https://github.com/username/repository.git
    ~~~
    - Push changes:
    ~~~sh
    git push origin main
    ~~~

7. **Pull changes from a remote repository**:
    ~~~sh
    git pull origin main
    ~~~

## Using GitHub Desktop :
1. Download and install GitHub Desktop:
    - Go to the [GitHub Desktop website](https://desktop.github.com/).
    - Download and install the application for your operating system.

2. Set up GitHub Desktop:
    - Open GitHub Desktop and sign in with your GitHub account.
    - You can clone repositories, create new repositories, and manage your projects directly from the application interface.

<br>

> By following these steps, you should be able to install Git, configure it, and start using it for version control in your projects.<br> Additionally, GitHub Desktop provides a user-friendly interface to manage your repositories and collaborate with others.