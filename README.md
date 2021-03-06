# Library Catalog

#### _Advanced Database ASP.NET MVC Core 2.2 Project for Epicodus_, _Mar. 24 2020_

#### By _**Michelle Morin, Patrick Kille, Keturah Howard**_

## Description

This application is a library catalog to catalog a library's books and let patrons check them out.

## Specifications:
* As a librarian, the application allows me to create, read, update, delete, and list books in the catalog, so that we can keep track of our inventory.
* As a librarian, the application allows me to search for a book by author or title, so that I can find a book when there are a lot of books in the library.
* As a librarian, the application allows me to enter multiple authors for a book, so that I can include accurate information in my catalog.
* As a patron, the application allows me to check a book out, so that I can take it home with me.
* As a patron, the application allows me to know how many copies of a book are on the shelf, so that I can see if any are available.
* As a patron, the application allows me to see a history of all the books I checked out, so that I can look up the name of that awesome sci-fi novel I read three years ago.
* As a patron, the application allows me to know when a book I checked out is due, so that I know when to return it.
* As a librarian, the application allows me to see a list of overdue books, so that I can call up the patron who checked them out and tell them to bring them back.

![Database relationships:](https://media.discordapp.net/attachments/692032456085471342/692471586191573022/unknown.png)
![Website navigation](https://cdn.discordapp.com/attachments/692032456085471342/692059330270461982/unknown.png)

## Setup/Installation Requirements

### Install .NET Core

#### on macOS:
* _[Click here](https://dotnet.microsoft.com/download/thank-you/dotnet-sdk-2.2.106-macos-x64-installer) to download a .NET Core SDK from Microsoft Corp._
* _Open the file (this will launch an installer which will walk you through installation steps. Use the default settings the installer suggests.)_

#### on Windows:
* _[Click here](https://dotnet.microsoft.com/download/thank-you/dotnet-sdk-2.2.203-windows-x64-installer) to download the 64-bit .NET Core SDK from Microsoft Corp._
* _Open the .exe file and follow the steps provided by the installer for your OS._

#### Install dotnet script
_Enter the command ``dotnet tool install -g dotnet-script`` in Terminal (macOS) or PowerShell (Windows)._

### Install MySQL and MySQL Workbench

#### on macOS:
_Download the MySQL Community Server DMG File [here](https://dev.mysql.com/downloads/file/?id=484914). Follow along with the installer until you reach the configuration page. Once you've reached Configuration, set the following options (or user default if not specified):_
* use legacy password encryption
* set password (and change the password field in appsettings.json file of this repository to match your password)
* click finish
* open Terminal and enter the command ``echo 'export PATH="/usr/local/mysql/bin:$PATH"' >> ~/.bash_profile`` if using Git Bash.
* Verify MySQL installation by opening Terminal and entering the command ``mysql -uroot -p{your password here, omitted brackets}``. If you gain access to the MySQL command line, installation is complete. An error (e.g., -bash: mysql: command not found) indicates something went wrong.

_Download MySQL Workbench DMG file [here](https://dev.mysql.com/downloads/file/?id=484391). Install MySQL Workbench to Applications folder. Open MySQL Workbench and select Local instance 3306 server, then enter the password you set. If it connects, you're all set._

#### on Windows:
_Download the MySQL Web Installer [here](https://dev.mysql.com/downloads/file/?id=484919) and follow along with the installer. Click "Yes" if prompted to update, and accept license terms._
* Choose Custom setup type
* When prompted to Select Products and Features, choose the following: MySQL Server (Will be under MySQL Servers) and MySQL Workbench (Will be under Applications)
* Select Next, then Execute. Wait for download and installation (can take a few minutes)
* Advance through Configuration as follows:
  - High Availability set to Standalone.
  - Defaults are OK under Type and Networking.
  - Authentication Method set to Use Legacy Authentication Method.
  - Set password to epicodus. You can use your own if you want but epicodus will be assumed in the lessons.
  - Unselect Configure MySQL Server as a Windows Service.
* Complete installation process

_Add the MySQL environment variable to the System PATH. Instructions for Windows 10:_
* Open the Control Panel and visit _System > Advanced System Settings > Environment Variables..._
* Select _PATH..._, click _Edit..._, then _Add_.
* Add the exact location of your MySQL installation and click _OK_. (This location is likely C:\Program Files\MySQL\MySQL Server 8.0\bin, but may differ depending on your specific installation.)
* Verify installation by opening Windows PowerShell and entering the command ``mysql -uroot -p{your password here, omitted brackets}``. It's working correctly if you gain access to the MySQL command line. Exit MySQL by entering the command ``exit``.
* Open MySQL Workbench and select Local instance 3306 server (may be named differently). Enter the password you set, and if it connects, you're all set.

### Clone this repository

_Enter the following commands in Terminal (macOS) or PowerShell (Windows):_
* ``cd desktop``
* ``git clone`` followed by the name of this repository
* ``cd Library.Solution``

_Confirm that you have navigated to the Library.Solution directory (e.g., by entering the command_ ``pwd`` _in Terminal)._

_Recreate the ``library_catalog`` database using the following commands (in Terminal on macOS or PowerShell on Windows):_
* ``dotnet ef migrations add Initial``
* ``dotnet ef database update``

_Run this application by entering the following command in Terminal (macOS) or PowerShell (Windows):_
* ``cd Library``
* ``dotnet restore``
* ``dotnet build``
* ``dotnet run`` or ``dotnet watch run``

_To view/edit the source code of this application, open the contents of the Library.Solution directory in a text editor or IDE of your choice (e.g., to open all contents of the directory in Visual Studio Code on macOS, enter the command_ ``code .`` _in Terminal)._

## Technologies Used

* C#
* ASP.NET Core MVC 2.2
* dotnet script
* Entity Framework Core 2.2
* Identity
* Razor
* MySQL + MySQL Workbench version 8.0.15
* Git
* HTML
* CSS

## License

Licensed under the MIT license.

&copy; 2020 - Michelle Morin, Patrick Kille, Keturah Howard