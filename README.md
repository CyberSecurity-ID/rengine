<br />
<p align="center">
  <a href="https://github.com/yogeshojha/rengine">
    <img src="static/img/logo.png" alt="Logo" width="80" height="80">
  </a>

  <h3 align="center">reNgine</h3>
</p>

![Version](https://img.shields.io/badge/version-1.0-blue.svg?cacheSeconds=2592000)
[![first-timers](https://img.shields.io/badge/first--timers--only-friendly-blue.svg?style=flat-square)](https://www.firsttimersonly.com/)
[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![python](https://img.shields.io/badge/python-3.8-blue.svg?logo=python&labelColor=yellow)](https://www.python.org/downloads/)
[![platform](https://img.shields.io/badge/platform-osx%2Flinux%2Fwindows-green.svg)](https://github.com/yogeshojha/rengine/)
[![Vulnerabilities](https://sonarcloud.io/api/project_badges/measure?project=yogeshojha_rengine&metric=vulnerabilities)](https://sonarcloud.io/dashboard?id=yogeshojha_rengine)
[![Maintainability Rating](https://sonarcloud.io/api/project_badges/measure?project=yogeshojha_rengine&metric=sqale_rating)](https://sonarcloud.io/dashboard?id=yogeshojha_rengine)
[![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=yogeshojha_rengine&metric=alert_status)](https://sonarcloud.io/dashboard?id=yogeshojha_rengine)
![GitHub issues](https://img.shields.io/github/issues/yogeshojha/rengine)

<p align="center">
    A automated recon framework for web applications
    <br />
    <a href="https://github.com/yogeshojha/rengine/blob/master/CONTRIBUTING.md">Contribute</a>
    ·
    <a href="https://github.com/yogeshojha/rengine/issues">Report Bug</a>
    ·
    <a href="https://github.com/yogeshojha/rengine/issues">Request Feature</a>
</p>

## Table of Contents

* [About reNgine](#about-reNgine)
  * [What is reNgine](#about-reNgine)
  * [What it is not](#what-it-is-not)
  * [Screenshots](#screenshots)
* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#usage)
* [Contributing](#contributing)
* [License](#license)
* [Acknowledgements](#acknowledgements-and-credits)

## About reNgine

![](https://user-images.githubusercontent.com/17223002/86762294-2e0ba880-c064-11ea-91d1-267ebc8deffe.png)

reNgine is a automated reconnaissance framework meant for gathering information during penetration testing of web applications. reNgine has customizable scan engines, which can be used to scan the websites, endpoints and gather information. The beauty of reNgine is that, it gathers everything in one place. It has a pipeline of reconnaissance, which can be customized.

reNgine can be very useful when you have a domain, you want to recon the domain, gather endpoints, directory and file search, performing visual reconnaissance and gather the results at one place.

Suppose, if you have a domain hackerone.com, reNgine can perform the scan based on your defined scan engine, gather all the results at one place. reNgine makes it possible for use cases like, "I want to search the subdomain which has page title "Dashboard" and has page status as 200, and quickly want to have a look at the screenshot", reNgine makes it possible.

Another use-case could be, "I want to list all subdomains that uses php and the http status is 200!"

On the endpoints part, reNgine is capable of gathering the URL endpoints using tool like `gau`, gathers url from many sources like commoncrawl, waybackengine etc.

reNgine makes it possible for the use case like, "search the urls that has extension .php and http status is 200!"

**Also, Suppose if you are looking for open redirection, you can quickly search for `=http` and look for http status 30X, this will give high accuracy of open redirection with minimal efforts.**

### What it is not

reNgine is not a:
* Vulnerability scanner!
* Reconnaissance with high accuracy (No! reNgine infact uses other open source tools, to make this pipeline possible. The accuracy and capability of reNgine is also dependent on those tools)
* Speed oriented recon framework with immediate results

### Screenshots
#### Scan results

![](https://user-images.githubusercontent.com/17223002/86752434-f9482300-c05c-11ea-954b-b0f538c1ecef.png)

![](https://user-images.githubusercontent.com/17223002/86508685-ba696180-bdff-11ea-9def-f45e5b059f0f.png)

#### Gathered Endpoints

![](https://user-images.githubusercontent.com/17223002/86753221-8c815880-c05d-11ea-816b-9c2dce11335a.png)

Of course, at this point in time, reNgine does not give the best of the best result compared other tools, but reNgine has certainly minimal efforts. Also, I am continuously adding new features. You may help me on this journey by creating a PR filled with new features and bug fixes. Please have a look at the [Contributing](#contributing) section before doing so.

## Getting Started

To get a local copy up and running follow these simple example steps.

```sh
git clone https://github.com/yogeshojha/rengine.git
cd rengine
```

### Prerequisites

* Docker
Install docker based on your OS from [here](https://www.docker.com/get-started)
* docker-compose
Installation instructions for docker-compose from [here](https://docs.docker.com/compose/install/)



### Installation

Assuming that you have followed the above steps and inside rengine directory
```sh
docker-compose up --build
```
Build process may take some time.

## Usage

> :warning: reNgine does fingerprinting, port scanning and banner grabbing which might be illegal in some countries. Please make sure you are authorized to perform reconnaissance on targeted domain before using this tool.

If the installation is successful, then you can simply run reNgine by using the command
```sh
docker-compose up -d
```

The web application can then be accessed from [http://localhost:8000](http://localhost:8000)

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**. Your contributions could be as simple as fixing the indentations or fixing UI to as complex as bringing new modules and features.

See [the contributing guide](CONTRIBUTING.md) to get started.

### First-time Open Source contributors
Please note that reNgine is beginner-friendly. If you have never done any open-source yet, we encourage you to do so. **We will be happy and proud of your first PR ever.**

You can begin with resolving any [open issues](https://github.com/yogeshojha/rengine/issues).

## License

Distributed under the GNU GPL v3 license License. See [LICENSE](LICENSE) for more information.

## Acknowledgements and Credits
reNgine is just a pipeline of recon. reNgine would not have been possible without the following individuals/organizations.

* Amass: [OWASP](https://github.com/OWASP/)
* httpx, subfinder, naabu: [ProjectDiscovery](https://github.com/projectdiscovery/)
* Sublist3r: [Ahmed Aboul-Ela](https://github.com/aboul3la/)
* gau, assetfinder: [Tom Hudson](https://github.com/tomnomnom/assetfinder)
* dirsearch: [maurosoria](https://github.com/maurosoria/dirsearch)
* pulsar: [FooBallZ](https://github.com/FooBallZ/pulsar)

Also, Some of the icons and images used here in reNgine are from Freepik and flaticons.
