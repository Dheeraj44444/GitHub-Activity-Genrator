# GitHub Activity Generator

This script helps you instantly generate a beautiful GitHub Contributions Graph for the last year. It's a fun and educational tool for creating visually appealing contributions, but remember, it is not designed to encourage cheating in any way. Use it responsibly!

**Disclaimer**  
This script is not intended to deceive anyone or manipulate GitHub’s activity graphs. GitHub's contributions graph doesn't reflect your true professional skills, and basing your skills solely on it is misleading. Use this tool for educational purposes only to learn about GitHub actions, automation, and contributions.

---

## What It Looks Like

Before:  
![Before](images/before.png)  

After:  
![After](images/after.png)

---

## How It Works

The script works by creating a new GitHub repository and generating daily commits for the past year (up to 20 commits per day). Each commit adds some changes to a text file, simulating contributions over time. Once the commits are generated, it links the repository to your remote GitHub repository and pushes the changes.

The main goal of this script is to help you understand how to automate contributions and work with GitHub's commit and push workflows.

---

## How to Use

1. **Create a New GitHub Repository**  
   - Create a new, **empty** GitHub repository.  
   - **Do not initialize** it with a README or any other files.

2. **Download the Script**  
   Download the `contribute.py` script from this repository.

3. **Run the Script**  
   Execute the script in your terminal, providing the link to your GitHub repository as follows:

   ```bash
   python contribute.py --repository=git@github.com:user/repo.git
   ```

4. **Wait for Activity Update**  
   It may take a few minutes for GitHub to reindex your activity and display the updated contributions on your profile.

---

## Customizations

You can customize how often the script commits and how many commits per day to generate:

- **Adjust Frequency and Max Commits**  
   For example, with the following command, the script will make from 1 to 12 commits a day and will commit 60% of the days in the year:

   ```bash
   python contribute.py --max_commits=12 --frequency=60 --repository=git@github.com:user/repo.git
   ```

- **Exclude Weekends**  
   If you don’t want the script to make commits on weekends, use the `--no_weekends` option:

   ```bash
   python contribute.py --no_weekends --repository=git@github.com:user/repo.git
   ```

- **Set Specific Time Range**  
   Use `--days_before` and `--days_after` to specify how many days before and after the current date the script should start committing:

   ```bash
   python contribute.py --days_before=10 --days_after=15 --repository=git@github.com:user/repo.git
   ```
