# Project 7 - WordPress Pentesting

Time spent: **X** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. WordPress <= 4.2.2 - Authenticated Stored Cross-Site Scripting (XSS)
  - [*] Summary: xss vulnerability in creating posts or pages
    - Vulnerability types: XSS
    - Tested in version: 4.0
    - Fixed in version: 4.2.3
  - [*] GIF Walkthrough: [here](http://i.imgur.com/3geOSUP.png)
  - [*] Steps to recreate: create a post with this text: (<a href="[caption code=">]</a><a title=" onmouseover=alert('test') ">link</a>)
  - [*] Affected source code:
    - [new post](https://core.trac.wordpress.org/browser/trunk/src/wp-admin/post-new.php)
1. Title: WordPress 3.6.0-4.7.2 - Authenticated Cross-Site Scripting (XSS) via Media File Metadata
  - [*] Summary: you can exploit the site through audio playlist metadata
    - Vulnerability types: XSS
    - Tested in version: 
    - Fixed in version: 4.7.3
  - [*] GIF Walkthrough: [here](http://i.imgur.com/7CprZpd.png)
  - [*] Steps to recreate: upload a certain mp3 file to an audio playlist in a post
  - [*] Affected source code:
    - [wp playlist](https://core.trac.wordpress.org/browser/trunk/src/wp-includes/js/mediaelement/wp-playlist.js)
1. Title: WordPress  4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [*] Summary: you can execute js through youtube embeds
    - Vulnerability types: XSS
    - Tested in version: 4.0
    - Fixed in version: 4.7.3
  - [*] GIF Walkthrough: [here](http://i.imgur.com/3EZNQVR.png)
  - [*] Steps to recreate: create a post with this text: ([embed src='https://youtube.com/embed/12345\x3csvg onload=alert(1)\x3e'][/embed])
  - [*] Affected source code:
    - [embed](https://core.trac.wordpress.org/browser/trunk/src/wp-includes/embed.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
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

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.