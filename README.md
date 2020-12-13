# A workspace for developing plug-ins and themes for WordPress.

This repository contains a workspace for the development of plugins and themes for WordPress, with my snippets and extensions used to ensure that the code developed complies with WordPress standards in a Windows 10 enviroment.


# Requirements
 1. PHP 7.4+
 2. Fira Code font 
 3. Git
 4. Composer  
 5. PHP CodeSniffer 
 6. WPCS  
 7. Extensions 
	 - phpcbf
	 - phpcs
	 - Prettier - Code formatter
	 - SFTP (to upload e download code to my host)
	 - vscode-icons
![Extensions Image](https://github.com/alangustavo/wp_workspace_vscode/raw/main/img/extensions.JPG)
## Download PHP
For this example, I will use [PHP version 7.4 64 Bits Thread Safe](https://windows.php.net/downloads/releases/php-7.4.13-Win32-vc15-x64.zip) which is also compatible with my computer and the libraries and extensions we are going to use. You can see others versions [here](https://windows.php.net/download#php-7.4).
 1. After the download, extract the files to **`c:\php`**.
 2. Copy the file **`c:\php\php.ini-development`** to **`c:\php\php.ini`** .

Edit the file **`c:\php\php.ini`**  and search for  **`;extension = openssl`** remove the "**`;`**" to activate openssl,  as shown in the figure.
![php.ini enable openssl extension](https://raw.githubusercontent.com/alangustavo/wp_workspace_vscode/main/img/php_ini.png)

On the control panel look for **System Variables** and click on **Environment Variables**.
![System Variable image](https://raw.githubusercontent.com/alangustavo/wp_workspace_vscode/main/img/system_variables.png)
And then add **`c:\php`** to the windows path, conforme a imagem a seguir.
![enter image description here](https://raw.githubusercontent.com/alangustavo/wp_workspace_vscode/main/img/path_php.jpg)

## Install Composer
You can download the [Composer-Setup.exe](https://getcomposer.org/Composer-Setup.exe) from the composer site. 

## Install Fira Code Font
Download and install [Fira Code Font](https://fonts.google.com/specimen/Fira+Code)

## Install Git
Download and install [Git](https://git-scm.com/download/win)

## WordPress Coding Standards in Visual Studio Code
Why follow standards? Each programmer programs in a different way. Some indent with spaces, others with tabs. Some prefer two spaces, others four. Some break the line with the CRLF, others only with the LF, etc. This variety exists in any language and nothing less than a personal preference. However, when we develop for WordPress we must follow the standards that they set. For this, we will configure the workspace to check if our code adheres to the standards defined by them.

### Installing PHP CodeSniffer (PHPCS)
PHPCS is a development tool that checks for violations of the coding standard and automatically corrects them and specifies what problems are encountered. Note that PHP 5.4+ is required. To install use the terminal and the composer according to the command below.

 ```bash
composer global require "squizlabs/php_codesniffer=*"
```
### Instaling WPCS (WordPress Code Standards)
First, you need to download the WPCS to a folder in your computer.
```bash
 git clone -b master https://github.com/WordPress/WordPress-Coding-Standards.git wpcs
```
On my computer I downloaded it to the folder **c:\dev\utils\wpcs**.

Then you need to configure PHPCS to find WordPress standards in the folder where you placed the WPCS files.
```bash
phpcs --config-set installed_paths **c:\dev\utils\wpcs**
```
Now, download [my code](https://github.com/alangustavo/wp_workspace_vscode/archive/main.zip), extract the files in a folder and open your VSCODE, click on File, Open WorkSpace point to the folder and be happy!