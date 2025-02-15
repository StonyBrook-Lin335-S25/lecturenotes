---
title: Setting up Google Colab with GitHub
author: Thomas Graf
date: 2025-02-15
geometry: margin=1in, letterpaper
fontsize: 12pt
numbersections: true
fontfamily: mathdesign
fontfamilyoptions: charter
---

# Create a private GitHub repository

1. If you don't already have a GitHub account, go to <https://github.com> and create one.
   GitHub accounts are completely free.
1. Go to GitHub and, if necessary, sign in.
1. On your Dashboard, you will see a green button `New` on the left of your screen to create a new repository.
   Click this button to create a new repository.
    - If you are on a device with a small screen, e.g. your phone, you get a reduced interface that does not include the `New` button.
      In that case, click on the top-right button for your account, select `Your repositories`, and then you will be taken to a separate page that finally has a shiny green button `New` to create a repository.
1. You should now see a new page titled `Create a new repository`.
   As the name, pick `lin335_firstname_lastname`, replacing `firstname` and `lastname` with your first name and last name, respectively.
1. Skip the `Description` field.
1. Select `Private` to create a private repository that only you have access to.
   Do not choose `Public`, you have to create a private repository with the `Private` option.
1. Check the box `Add a README file`.
   Otherwise, GitHub will create an empty repository, which Colab won't be able to save to.
    - If you have already create your repository and it is empty, take the following steps to create at least one file in your repository:
    - Go to your repository. You should see a box `Quick setup - if you've done this kind of thing before`.
      Within that box, there is a link `creating a new file`.
      Click that link.
    - This takes you to a new page where you can create a file.
      Click on the field that says `Name your file...`, and type in `README` (any name will do, but README is a safe choice).
    - Now, hit the green button `Commit changes...`.
      This opens a pop-up window.
      Just hit the green button `Commit changes` within that pop-up window.
1. Congratulations, you should now have a private GitHub repository with at least one file in it.

# Give us access to your private repository

1. Since your repository is private, only you have access to it right now.
   But the instructor and TA also need to be able to access it.
   You will have to give them permission to access the repository.
1. Go to your repository.
1. Click on `Settings` in the top bar.
   This loads a new page.
1. In the bar on the left, select `Collaborators and teams`.
   This loads a new page.
1. Click the green button that says `Add people`, then add the usernames that are specified in the Brightspace announcement for this assignment.
1. When asked for the level of access, pick `Write`.

# Setting up Colab for use with private GitHub repositories

1. Go to `https://colab.research.google.com`.
1. You should get a dialog window that says `Open notebook`.
1. In the left bar, select `GitHub`.
1. You should now see a text box that says `Enter a GitHub URL or search by organization or user`.
   If the box is empty, enter your GitHub user name.
1. Next to the box, check the option for `Include private repos`.
1. This will probably open a new dialog with GitHub asking you if you want to give Google Colab access to your account.
   Confirm and provide your password and/or 2-factor authentication as necessary.
1. Under `Repoistory:`, you should now be able to select your private GitHub repository.
   Also, make sure that the text box `Branch` to the right shows some branch name (usually `main` or `master`).
    - If Colab says that your repository has no branch, you might have created your repository without a README.
    - Go back to the instructions above to see how to create a file in your repo.
      You must have at least one file in it before Colab can save to the repository.
1. Click anywhere outside the dialog window to close it.
   Colab is now set up with access to your private GitHub repositories.

# Saving a Colab notebook to Github

1. Open the notebook that you want to save.
1. In the menu bar at the top, select `File`, then `Save a copy in GitHub`.
1. You will get a dialog where you can choose the repository.
   Pick your private repository for this class.
   Leave everything else as is, and hit `OK`.
