= clickonce =

* Deployment manifest—A file used by the ClickOnce engine to figure out what application to deploy, when to deploy it, and where to find the application files. File has .application extension.

* Application manifest—A file used by the ClickOnce engine to deter mine what files an application is composed of and what permissions the application requires to run. This is different from the application configu ration file, which is sometimes referred to as a manifest for the application. File has .exe.manifest extension.

* Deployment server—The server on which you place your manifests and application files, which lets end users perform a ClickOnce deployment.

* Deployment provider—The URL or address that gets embedded in the deployment manifest. It is used by ClickOnce to determine the address used to launch the application.

ClickOnce deployment modes:
1. Install Mode:
After the initial installation from the deploy ment server, an installed application is available whether or not the client machine can connect to the deployment server to check for updates. Shortcuts are added to start menu. An entry is added in Programs and Features to remove the app.
2. Online-only install mode
Users must always launch the application with a full URL to the deployment manifest on the server, and therefore must be connected to the network. No shortcut is added to start menu or in Programs & Features.
3. CD deployment
Allows deployment via CD.
