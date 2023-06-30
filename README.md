## MonoGame Intellisense Documentation
When MonoGame 3.8.1.303 (a hotfix) was released, the NuGet packages did not include the XML documentation file.  This means no intellisense with those nice juicy descriptions as to what things do when you hover over them.

Why were they not included?  Oversight? Mistake? I dunno, things happen.

So, if you want to include them yourself, you would need to manually clone the MonoGame git repo, update the csproj files to tell them to generate the documentation file, then build the projects to get them.

But that's a lot of work, I hear you.

So I've done it for you, in this repo.

## How to Include the Missing Intellisense
To get the intellisense back, you'll need to include the `MonoGame.Framework.xml` file inside the NuGet package folder that is downloaded on your computer.  It's not as complicated as it might sound, steps are provided below.  Where you place the file will be dependent on your operating system.

### Step 1: Download the file
First download the `MonoGame.Framework.xml` file found in the [Releases](https://github.com/AristurtleDev/monogame-xml-documentation/releases/tag/v3.8.1.303) page in this repo

### Step 2: Where to put the file
The following paths assume that your NuGet packages are downloaded to the default global NuGet path.

* **Windows**: `%USERPROFILE%/.nuget/packages/monogame.framework.desktopgl/3.8.1.303/lib/net6.0`/`
* **Mac/Linux** `~/.nuget/packages/monogame.framework.desktopgl/3.8.1.303/lib/net6.0/`

> 💡NOTE  
> &nbsp;  
> In the above paths, i used the `monogame.framework.desktopgl` directory.  This may be different depending on which project type you are using (e.g. DesktopGL vs WindowsDX).  Adjust the path accordingly.

Inside the directories listed above should be the `MonoGame.Framework.dll` file. Just put the `MonoGame.Framework.xml` file in that same directory.

## Step 3: Restart
If you have Visual Studio/VSCode/Rider open, close it out. Then open it again and load your project.  You should now have intellisense.  

## License
The documentation file is part of the MonoGame project which is licensed under the Microsoft Public License.  You can find their license information at https://github.com/MonoGame/MonoGame/blob/develop/LICENSE.txt

I am just providing these files that were missing from the NuGet so others may access them and use them. If any maintainer of the MonoGame project wishes me to take these down, please let me know and I'll remove them immediately.