# SWeRPD Deployment
### Basically a ReadMe.md file that describes how to set up the swerpd app<br>
### (On windows server 2016 Datacenter)

<br>

# Installing Features with Windows Server Manager

<br>

Click on "Add roles and features"
>![Server Manager Window](./imgs/servermngr.png?raw=true "Server Manager Window")

Select your installation type, use Role-based unless you plan to run the app on a virtual machine / virtual hard disk. Then click "Next"
>![Server Manager Window](./imgs/servermngr2.png?raw=true "Server Manager Window")

Then choose the server you want to install the features onto
>![Server Manager Window](./imgs/servermngr3.png?raw=true "Server Manager Window")

Now you should be on this page, you gotta make sure these features are ticked

<ul>
    <li>
    Web Server (IIS)
        <ul>
            <li>Web Server
                <ul>
                    <li>Common HTTP Features
                        <ul>
                            <li>Default Document</li>
                            <li>Directory Browsing</li>
                            <li>HTTP Errors</li>
                            <li>Static Content</li>
                        </ul>
                    </li>
                    <li>Health and Diagnostics
                        <ul>
                            <li>HTTP Logging</li>
                            <li>ODBC Logging</li>
                            <li>Request Monitor</li>
                            <li>Tracing</li>
                        </ul>
                    </li>
                    <li>Performance
                        <ul>
                            <li>Static Content Compression</li>
                            <li>Dynamic Content Compression</li>
                        </ul>
                    </li>
                    <li>Security
                        <ul>
                            <li>Request Filtering</li>
                        </ul>
                    </li>
                    <li>Application Development
                        <ul>
                            <li>.NET Extensibility 3.5</li>
                            <li>CGI</li>
                            <li>ISAPI Extensions</li>
                            <li>ISAPI Filters</li>
                            <li>Server Side Includes</li>
                            <li>WebSocket Protocol</li>
                        </ul>
                    </li>
                </ul>
            <li>FTP Server
                <ul>
                    <li>FTP Service</li>
                </ul>
            <li>Management Tools
                <ul>
                    <li>IIS Management Console</li>
                    <li>IIS 6 Management Compatibility</li>
                </ul>
            </li>
            </li>
            </li>
        </ul>
    </li>
</ul>

>![Server Manager Window](./imgs/servermngr4.png?raw=true "Server Manager Window")

Proceed until you reach the Confirmation page, and then click install. We're about done here.

<br>

# Installing the App

<br>

### First thing to do is to clone the repo into 2 different folders, namely "backend" and "frontend" for easy identification

Open up a cmd and cd into the "backend" folder : 
                <ul>
                    <li>npm i --force <br>
                    (There is a known [nodejs] bug where it won't install if you just use "npm -i" due to multer-gridfs, so you have to install it with --force or by using a package manager like yarn to manually install the package)
                    </li>
                </ul>