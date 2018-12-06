# Salesforce Extensions for VS Code + Mavensmate

Visual Studio Code is becoming more and more popular, Salesforce is now investing on VS Code instead of Eclipse
Follow this article if you want to use Salesforce Extensions for VS Code with a non DX project

## Install Visual Studio Code

Download and install Visual Studio Code from :
https://code.visualstudio.com/Download

![alt text](https://cdn-images-1.medium.com/max/1000/1*4Q5WAp-QwbH7YG6k5nDwtw.png "title")

## Install Salesforce Extensions for VS Code

Click on the extensions icon in VS Code
Search for “Salesforce Extensions for VS Code”
Install the extension and reload your VS Code
![alt text](https://cdn-images-1.medium.com/max/1000/1*KeFGat51oRymF-Vk4YyIwA.png "title")

## Install MavensMate for VS Code

Click on the extensions icon in VS Code
Search for “Mavensmate”
Install the extension and reload your VS Code
![alt text](https://cdn-images-1.medium.com/max/1000/1*NeSTIrwAOTkefK_nteFkaA.png "title")

Install MavensMate
Download and install MavensMate Desktop (Latest version 0.0.11-beta.7) from :

https://github.com/joeferraro/MavensMate-Desktop/releases

## Create & Configure a project

Open the Mavensmate desktop

![alt text](https://cdn-images-1.medium.com/max/1000/1*6XCvmqGgk973XbNjlckIlA.png "title")

Create a new project by authenticating to your Sandbox/Dev org

![alt text](https://cdn-images-1.medium.com/max/1000/1*zlNV3aFJ5PANeW8euDa04A.pngg "title")

Select the metadatas you need and click refresh project

![alt text](https://cdn-images-1.medium.com/max/1000/1*vV7o2gbZSFWtD0H8lnSmng.png "title")

Configure the path to Visual Studio Code executable (Code.exe)

![alt text](https://cdn-images-1.medium.com/max/1000/1*WXtZgBGYGA1XrplYdmBIqw.png "title")

Open the project folder using Visual Studio Code

![alt text](https://cdn-images-1.medium.com/max/1000/1*PSj5VXYfOlEgjWvO6JgurA.png "title")

## Configure Salesforce Extensions for VS Code

Add a dummy sfdx-project.json to your project

![alt text](https://cdn-images-1.medium.com/max/1000/1*IA1pq3h5cSljVL6QLlduYw.png "title")

Content of the dummy sfdx-project.json

```
{
"packageDirectories": [
{
"path": "src",
"default": true
}
],
"namespace": "",
"sfdcLoginUrl": "https://test.salesforce.com",
"sourceApiVersion": "40.0"
}
```

Goto the Visual Studio Code settings
![alt text](https://cdn-images-1.medium.com/max/1000/1*SUZDE_MZl1uRDMWcK0xhUw.png "title")

Change the salesforcedx-vscode-apex.java.home setting to the full pathname of your Java Runtime (example : C:\\Program Files\\Java\\jdk1.8.0_144)

![alt text](https://cdn-images-1.medium.com/max/1000/1*s5OAFgZxjtYilvCzBAGZNg.png "title")

Restart VS Code

## Enjoy code auto-completion

Enjoy the auto-completion of the Apex Language Server

![alt text](https://cdn-images-1.medium.com/max/1000/1*cM1FW8MA4CLs_I-A_Qs_Ow.png "title")

## Links:

- https://code.visualstudio.com/
- https://marketplace.visualstudio.com/items?itemName=salesforce.salesforcedx-vscode
- https://github.com/joeferraro/MavensMate-Desktop
