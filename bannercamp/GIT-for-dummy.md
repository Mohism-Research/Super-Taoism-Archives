# Clone the project repository #

Simplely I take the Super-Taoism-Archives for example, the URL of the STA on github is: https://github.com/Mohism-Research/Super-Taoism-Archives.git, the git clone command is below:

```bash
git clone https://github.com/Mohism-Research/Super-Taoism-Archives.git
```

Then you find the STA directory appears in the current directory.

# Update the repository #

Before starting your work on the repository or pushing your commits into the repository, you need to synchronise with the remote service, so you firstly enter the STA directory, then run the update command:

```bash
cd Super-Taoism-Archives
git pull
```

# Make your contributions to the commnunity #

After editing the content under the STA, you can use several commands to check your changes,

- Using "git status" to view the summary of your changes

```bash
git status
```

- Using "git diff" to view the details differences between your changes and the riginal contents.

```bash
git diff
```

Then use the "git add" command to add your changed files into the adding buffer:

```bash
git add .  //Add the all files under the current directory.
git add yourfile   //Add the one single file
```

Next step you need "git commit" command to generate one commit in your local machine:

```bash
git commit -m "message"  //The message is your description about your changes.
```

Finally you should push your commit into the remote service, there is one very important thing you must do before your pushing, update the repository as the previous section I said, otherwise there will be conflicts if anyone changed the file you also changed.

```bash
git pull
git push
``` 
# The Road is long #

With these commands I mentioned, we can do baisc remote developments. However, the git is a very powerfull tool to manage the source, and unfortunately it's very complicated, the banner have to read more help mannuls to get deeper undserstanding of it.
