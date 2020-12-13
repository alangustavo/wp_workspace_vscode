# A workspace for developing plug-ins and themes for WordPress.

This repository contains a workspace for the development of plugins and themes for WordPress, with my snippets and extensions used to ensure that the code developed complies with WordPress standards.


# Requirements
 - PHP 7.4+
 - Fira Code font 
 - Git
 - Composer  
 - PHP CodeSniffer 
 - WPCS  
 - Extensions 
	 - PHPCS
	 - PHPCBS

## Install Fira Code Font
Download and install [Fira Code Font](https://fonts.google.com/specimen/Fira+Code)

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