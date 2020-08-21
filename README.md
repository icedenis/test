# PersonalDB

PersonalDB is a demo application built with the [Blazor](https://blazor.net) framework using the client-side hosting model with WebAssembly in the browser invoking .NET Core REST APIs secured by a JWT service.. For authenticated pages and APIs, use the credentials (SYSADM / dsa).

[PersonalDB REST API](http://localhost:8888/swagger/index.html) - A REST API for CRUD with non-read API calls secured with JWT. The API includes a call to authenticate users and receive a JWT bearer token.

* [Bitbucket Source Code Repository](https://rad@git.app.corp.dsa.de/scm/dsapersdb/dsa-personaldb.git) - All source code is stored in the Bitbucket repository, which is where you currently find yourself.

# Get started

* Install the Preview edition of [Visual Studio 2019](https://visualstudio.microsoft.com/de/vs/preview/) (Community, Professional, and Enterprise Editions are all supported) with the ASP.NET and web development workload enabled. PersonalDB works with all editions of Visual Studio from Community to Enterprise. If you do not have a SQL Server available already and you wish to use LocalDB for development, you must ......

* To get started with [Blazor](https://dotnet.microsoft.com/learn/aspnet/blazor-tutorial/intro) , follow the instructions in the Blazor Get Started documentation.

# Features

* Docker container generation as a single deployable Docker image
* Dashboard page- shows the last 4 days changes made on the users and personals and pie charts shows the personal by department,fulltime and  gender
* Edit page - add/edit personal uses FluentValidation and Toastr-style notifications.
* Entity lists with pagination and search
* Modal data entry forms with validations
* Complex data entry with object graph validations
* Javascript Web Token (JWT) authentication and validation.
* Automation of Azure Infrastructure Setup
* Typeahead for entity lookup on modal data entry screens (preview functionality)


# Open Source Used

* [AutoMapper](https://github.com/AutoMapper/AutoMapper) for object-object mappings.
* [BlazorInputFile](https://github.com/SteveSandersonMS/BlazorInputFile) for file upload.
* [BlazorStorage](https://github.com/cloudcrate/BlazorStorage) for local and session storage in the browser.
* [BlazorStrap](https://github.com/chanan/BlazorStrap) Bootstrap 4 components for Blazor.
* [Blazor.Toastr](https://github.com/sotsera/sotsera.blazor.toaster) for Toastr-style notifications.
* [Bogus](https://github.com/bchavez/Bogus) for data generation.
* [ChartJs.Blazor](https://github.com/mariusmuntean/ChartJs.Blazor) Blazor component that wraps ChartJs widgets for dashboard.
* [FluentValidation](https://github.com/JeremySkinner/FluentValidation) For entity validation, including complex object graph validations. 
* [Swashbuckle](https://github.com/domaindrivendev/Swashbuckle) for Swagger document generation.
* [Typeahead](https://github.com/Blazored/Typeahead) for typeahead lookup of key entities.


# Docker Setup

* [Docker desktop for windows](https://hub.docker.com/editions/community/docker-ce-desktop-windows) - donwload docker desktop for your operating system.
* Download PersonalDB and navigate to the project directory on the terminal 
* The docker file should already exists in the directory
### Build image with DSA proxy :

```
docker build --build-arg http_proxy=http://172.29.1.4:3128 --build-arg https_proxy=http://172.29.1.4:3128 -t blazor .
```
### Run the image

```
docker run -p 8080:80 -d blazor
```

### List running container

```
docker ps
```
### Kill running container

```
docker kill CONTAINER_ID
```
###   Forced delete of not running images
```
docker rmi -f imageid
```

# Example Screenshots

