# primevue-nuxt-example

## Github

1. To create a new repository, go to [github.com](github.com). If you do not have one, create a new account. 
2. If you want to duplicate this repository completely, click *fork*. Be sure to set the owner to yourself and name the repo as described below in step 3.1
    - **Note** - If you fork this repository (or copy it in any way other than manually) you will need to go to the "Actions" tab on your repository after it is created and press the button there to enable the GitHub Actions included.
3. If you want to manually copy content, then go ahead and click the new button (or the + button) in order to create a repository manually. 
    1. You need to name it **"\<user>.github.io"** where `<user>` is your GitHub username. For example, mine is named “weeser.github.io”. 
    2. For settings, leave the repository as "Public" and also check the "Add a README File" box. Then you can click the "Create repository" button at the bottom.
4. Configure **GitHub Pages**
    1. Open your repo’s settings. The link to these can be found under your repository name. If you do not see the "Settings" tab, click the … to reveal the drop down menu. 
    2. On the settings page, there should be a menu on the left. Under the "Code and automation" section, click on "Pages"
    3. Now, under "Build and deployment", under "Source" select the "GitHub Action" option.
        - The Github action that auto-compiles your Vue web app is already setup and can be found in the repo's ".github" folder
    4. This step might take a small amount of time, but once done, you should see a "Visit site" button on the this settings page (you may need to refresh a few times after a couple of minutes). The URL for the website should be should be something like `http://<user>.github.io`. You might have to refresh your page if you don’t see the webpage url. But you should be able to visit your site now. 
        - *Note that between changes to your website (after committing and pushing as described below), changes can take a few minutes to show on your live webpage. You can see any active running deployments (if it is still compiling) under the "Actions" tab on your repository.

## Installing Software

1. If you are working in the web browser in GitHub Codespaces, skip this section.
2. If you are on your local machine, you will need to install 
    - [VS Code](https://code.visualstudio.com/) for writing code.
    - [Git](https://git-scm.com/downloads) so you can work with a Github repository on your own machine. _Note_ if you are on a Mac, I recommend using the homebrew method of installing git.
    - [GitHub CLI](https://cli.github.com/) greatly simplifies the cloning process and helps get you authenticated to GitHub. It is a quick install. Once installed you will need to run `gh auth login` as indicated in [https://cli.github.com/manual/](https://cli.github.com/manual/)
    - Install Node.js so we can make use of npm: [https://nodejs.org/en/download/prebuilt-installer](https://nodejs.org/en/download/prebuilt-installer)

## Cloning the Repository

1. If you want to work locally on your own computer, you will need to clone the repository. Assuming you installed GitHub CLI from the previous section, you can click on the "Code" button then copy the GitHub CLI command under the "Local" tab.
    1. Paste this into a terminal window to clone the repository. *Note that if you want this at a specific location, use the "cd" command to navigate to the correct directory before running the `gh` command you copied*
2. Alternatively, you can also clone this through VS Code. Instructions on how to do so can be found here: [https://code.visualstudio.com/docs/sourcecontrol/intro-to-git](https://code.visualstudio.com/docs/sourcecontrol/intro-to-git)

## Running Locally
1. Now that you have the repo on your computer, if you did not "fork" this example repository, you need to download it as a "zip" folder by clicking the "Code" button on your GitHub repository page, under the local tab, click "Download ZIP". Once you unzip it, you can copy the files manually over into your own repository.
2. Open your respository's folder in VS Code if you have not done so.
3. Open the terminal in VS Code and then run `npm install`. This installs all the dependencies required for running and developing a Vue.js website with PrimeVue and NUXT
3. Then run `npm run dev` in order to start the web server in development mode.

## Running in GitHub Codespaces
1. Once you have duplicated everything from this repository to yours, you will have a working configuration for a development container. This will let you develop without installing anything on your local machine. To open your repository in Github Codespaces, click the "Code" button on your Github repository page. Under the Codespaces tab, you can either launch a codespace if it is already created, or create a codespace. 
    - *Note: you should request the free student developer pack if you have not already...it provides lots of benefits including more free usage of github codespaces.*
2. Once created, the codespace should already have all dependencies installed for you. You should be able to run the app by running `npm run dev` in the terminal window or by clicking on the "Run" menu and selecting "Run without debugging" (you may also run it with debugging).

## Making changes
1. Any changes (make sure you save your files!) made in your repository need to be *committed* and *pushed* so that it uploads the new changes to Github. Once pushed, your website should auto-deploy as described in the earlier section when setting up the repo.
2. To commit and push changes, click the "Source Control" tab in VS Code (menu on the left hand side of the screen).
3. Type a descriptive message about the changes made.
4. Click "Commit" then "Sync". You can also click "Commit and push" from the dropdown button next to the commit button to shortcut this.
    - It may ask you to "stage" changes. If so, typically you will want to stage all changed files to commit.
5. Your changes should now be uploaded to the GitHub repository. You can verify this by looking to see if you commit shows on your github page (more details on where the commits link is can be found here [https://docs.github.com/en/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/about-commits](https://docs.github.com/en/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/about-commits))
6. As noted before, the GitHub Action that auto-deploys this website may take a few minutes to finish running before your changes are visible on your live page/url.
7. **NOTE** Be sure to commit and push changes periodically so you don't lose any changes!

## Helpful resources.

There are many additional resources on the web for learning more about HTML, CSS, and Vue. This project is only intended to get your feet wet into developing dynamic web apps and auto-deploying them to GitHub Pages. Note though that the server-side features of Vue, Nuxt, and PrimeVue are not really applicable to this project as we are deploying this to GitHub Pages, which does not allow server-side logic etc. to run. But none the less, below are links to the primary technologies used in this demo. You might find more tutorials online in addition to many videos.

1. [https://primevue.org/introduction/](https://primevue.org/introduction/) - This page contains a lot of helpful examples and documentation on PrimeVue. You might find the "Components" section particularly helpful. Note that this webapp is configured to use the "Prime" prefix in front of any Primevue Component...so `Button` would be `PrimeButton` in this project.
2. [https://nuxt.com/](https://nuxt.com/) - This app utilizes Nuxt.js for simplifying some setup and management of the site...particularly links. But you can use other Nuxt features as well. 
3. [https://tailwindcss.com/](https://tailwindcss.com/) - This is a CSS framework used in this project for applying styles.

