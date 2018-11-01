# Web-Security-Week7
# Project 7 - WordPress Pentesting

Time spent: **12** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability Name or ID: Authenticated Stored Cross-site scripting
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.6.1
  - [x] GIF Walkthrough: 
    - <img src='XSS.gif' title='XSS' width='' alt='' />
  - [x] Steps to recreate: Create a new post and insert code in text: ```<a onmouseover= "alert('Hi there!!!')" >click here</a>```.
        Click "Preview" and the post you intend to post appears. When the cursor hovers over the click here link, the alert pops up. 
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/branches/4.2/src/wp-includes/class-wp-editor.php?rev=33361)
2. (Required) Vulnerability Name or ID
  - [x] Summary: 
    - Vulnerability types:
    - Tested in version: 4.2
    - Fixed in version: 4.7.5
  - [x] GIF Walkthrough: 
    - <img src='User Enumeration.gif' title='User Enumeration' width='' alt='' />
  - [x] Steps to recreate: Go to the login page of WordPress and first check for admin with no password, which leads to the empty password field.
        Next, check for admin but with an incorrect password, resulting to incorrect password for admin to display. 
        Then, when we write in a random username and password, it shows error that username doesn't exist.
  - [x] Affected source code:
    - [Link 1](https://www.wpwhitesecurity.com/wordpress-security/wordpress-username-disclosure-vulnerability/)
3. (Required) Vulnerability Name or ID: Authenticated Stored Cross-Site Scripting via Image Filename
  - [x] Summary: 
    - Vulnerability types:
    - Tested in version: 4.2
    - Fixed in version: 
  - [x] GIF Walkthrough: 
    - <img src='XSS2.gif' title='XSS' width='' alt='' />
  - [x] Steps to recreate: Go to create the media page and upload a picture. Once uploaded, click on the image and insert the following code to the title of the image:
    ```filename<img src=a onerror=alert(1)>.png```. Then click on "View attachment page" and the alert will pop up. 
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/branches/4.2/src/wp-admin/includes/media.php)
4. (Optional) Vulnerability Name or ID: Stored XSS through embedded URL
  - [x] Summary: 
    - Vulnerability types:
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [x] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2018] [Connie Wu]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
