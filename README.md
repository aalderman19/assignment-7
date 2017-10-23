# Project 7 - WordPress Pentesting

Time spent: 3 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.0
    - Fixed in version: 4.2
  - [ ] GIF Walkthrough: https://i.imgur.com/lUkj8sf.gifv
  - [ ] Steps to recreate: In the comments section of a post (as administrator) post code with script tags as a comment. The code will run after the page refreshes.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
2. WordPress <= 4.2.3 - Nav Menu Title Cross-Site Scripting (XSS)
  - [ ] Summary: Allows a user to inject HTML via the Nav link title in a menu.
    - Vulnerability types: XSS
    - Tested in version: 4.2.3
    - Fixed in version: 4.2.4
  - [ ] GIF Walkthrough: https://i.imgur.com/UNsFUMi.gifv
  - [ ] Steps to recreate: In the admin menu section, add a link to a new menu. In the Nav Link Title box, place your code. Then save the menu, and it will run.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/changeset/33541)
3. WordPress 3.6.0-4.7.2 - Authenticated Cross-Site Scripting (XSS) via Media File Metadata
  - [ ] Summary: Users can insert HTML in the meta data of media items. (in this case, I use an image)
    - Vulnerability types: XSS Injection
    - Tested in version: 4.2.3
    - Fixed in version: 4.2.11
  - [ ] GIF Walkthrough: https://i.imgur.com/BNt7dNl.gifv
  - [ ] Steps to recreate: Upload an image to wordpress and in the caption box, place your javascript. Attach the image to a page and view the page, the script should run.
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/28f838ca3ee205b6f39cd2bf23eb4e5f52796bd7)

## Assets


## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright 2017 Alec Alderman

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.