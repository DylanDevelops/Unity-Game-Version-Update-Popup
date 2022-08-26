# Welcome to the Version Popup Package for your Unity Game

## Table of Contents

Need to find a specific section? Use the table of contents below to jump to where you need to go!

- [About](#about)
- [How to Use](#how-to-use)
- [How to Set Up a Version Number Host](#how-to-set-up-a-version-number-host)
- [Contributing Guidelines](#contributing-guidelines)
- [Credits](#credits)

## About

In many games that I create, especially when published to itch.io or any hosting service that doesn't update your game on players devices when you push out an update automatically, I have used this system in many of my games. I thought that I would create a package that you could use in your own games to simplify this process, so that you didn't have to create your own system every time.

This project includes a system that allows you to push out updates and then make it so that the user is notified when starting the game. It will display the most recent version number and will display the version number that their current game is.

This project will help you out whether you're making a multiplayer game and need your players to all be running the game on the most recent release or you have a single player game and you want the player to not play on the last bug ridden update and rather your new version that has all of these game-breaking bugs fixed.

Below are the things you will find in this package.

- UI Popup Template
- A C# script containing the code that makes this system work
- A LICENSE file

Hope you enjoy! Feel free to create an issue if you have any issues and I will try my best to answer questions/fix issues!

## How to Use

The following are the instructions for how to use and customize this package to fit the needs of your game.

1) Install the package. Please make sure to download the most recent release of this package in the [releases](https://github.com/DylanDevelops/Unity-Game-Version-Update-Popup/releases) tab of this github repository.

2) The package will have to files. One will be the prefab that contains the UI popup template that you can customize to your liking. The second file will be the script that you can use to make it work. **Note:** *You can copy and paste the code in the script into any other script that you would like to control the version number check. Just remember that you have to change where the buttons look for the functions that they call.*

3) Customize the UI to your liking. Remember my code is just the springboard for whatever you would like to accomplish using this tool.

4) Drag the script onto the Canvas or any game object that you would like. Assign the values in the editor and/or in the code.

5) Link your website that hosts the game version to the `versionWebsite` variable. *([How to Set Up a Version Number Host](#how-to-set-up-a-version-number-host))*

6) **When pushing out a new game build, update the built in `currentVersionNumber` variable to the new game build. Then when updating on the website, all old game builds will show the popup but builds with the new number will not.

You are all set. If you have configured everything right, it should work! 

| **Appearance in Code:** | **Type of  Variable** |                                                                 **Explanation:**                                                                 |
|:-----------------------:|:---------------------:|:------------------------------------------------------------------------------------------------------------------------------------------------:|
|   currentVersionNumber  |         string        | This is the version number that is hard coded into the game. It's the number that is cross referenced with the number on the website.            |
|      versionWebsite     |         string        | This is the link to the website that the UnityWebRequest will use to decide if the players game is outdated.                                     |
|        gameWebsite      |         string        | The link to the website that hosts your file so that the player can go to the website and download the new update.                               |
|   outdatedVersionPopup  |       GameObject      | Connect this to the parent popup window element.                                                                                                 |
|      isRecentVersion    |          bool         | This is an element set up so that can reference this in your game anywhere you would like.                                                       |
|     yourVersionText     |          Text         | Connect this to the your version text element.                                                                                                   |
|      newVersionText     |          Text         | Connect this to the new version text element.                                                                                                    |
|        titleText        |          Text         | Connect this to the title text element.                                                                                                          |
|          XButton        |        GameObject     | Connect this to the X Button if you would like to have a way for the player to close the popup if an error occurs with the web request sent out. |
|         infoText        |          Text         | Connect this to the info box text element.                                                                                                       |

For more information on UnityWebRequests, feel free to visit the official unity documentation for this feature: [UnityWebRequests](https://docs.unity3d.com/2023.1/Documentation/ScriptReference/Networking.UnityWebRequest.html)

Have any questions? Feel free to create an issue and I will try to help you out!

## How to Set Up a Version Number Host

There are multiple ways to go about this but I recommend the following way as it is free and super simple.

### The Pastebin Solution

1) Create a [Pastebin](https://pastebin.com/signup) account.

2) Create a new paste.

3) Type your starting version number into the blank box and only the version number. (My code is set up to use single digit version numbers such as 1, 22, 1534, etc.. If you would like to use a different type of version number format, you will have to configure that in the code yourself. If you need help please create an issue and I will try to help you out!)

4) Set the `Paste Expiration` to `Never`.

5) Set the `Paste Exposure` to `Unlisted`.

6) Name your paste something the suits your project.

7) Click `Create New Paste` and proceed to the next page. **Note: Do not check `Paste as a guest`!**

8) Click on the button that says `raw`.

9) This should bring you to a page that is completely blank with just the number you chose earlier in the top left corner. Copy the url to this page and paste this into the `versionWebsite` variable. It should look something like: `https://pastebin.com/raw/XXXXXXXX`

10) If you would like to edit this number when you push out a new update, increase it by one or change it to any number you would like. You will not need to update the link at all when changing the number. All you need to is change it and click save. The link will stay the same but change the number it holds.. **Note:** *Remember that if you had used a prior number before, using it again may cause issues with people who still are on that version even if it was many numbers before the current one you are on.*

## Contributing Guidelines

Feel free to contribute! I not an incredibly skilled programer, so if you see something that you think you could improve apon, please feel free to work on the project. Just please follow the few rules below.

1) Always create a **NEW** branch when working on this project. **EDITS ON A BRANCH THAT IS NOT YOURS WILL BE DENIED!** Make your branch's name something specific so that it helps explain what the branch is for! For example, `fixed-typo` or `added-*SHORT DESCRIPTION OF CHANGE*`.

2) Test your changes!

3) Create a pull request! Make sure to check for any merge issues before creating your pull request. Name your request something unique and specific to help explain what the pull request is doing. You can then go into more detail inside of the description. If your pull request isi fixing an issue, reference the issue number by typing `Closes: #XXXXX` and replace the XXXXX with the issue number.

4) Understand that changes may be requested to your pull request. You can always discuss these changes within the pull request.

5) Once your pull request has been accepted, it will be merged into the main branch. Once merged, you may feel free to delete your branch that you created for the pull request.

6) Thanks for contributing to this project!

## Credits

Created by: Dylan Ravel [License](License)

Contact Email: [dylanm.ravel@gmail.com](dylanm.ravel@gmail.com)
