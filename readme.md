# Pokemon API

## Requirements
* Written using Visual Studio 2022 with .NET (Core) 5 installed. 
* You will need the ASP.NET and Web Development module installed


## Usage
* Make a GET request to `[domain]/api/pokemon/{pokemonName}`
* NB: Default host running from VS is `https://localhost:44353`. When using EXE, you will be given the host in the console.
* When running, you can call from swagger at the URL: `https://localhost:44353/swagger/index.html`

## Running
From Visual Studio:
* Run `RafeW.TrueLayer.Pokemon.Api` to access the endpoint.

Via exe:
* Unzip PokemonApiExe.zip
* Open `RafeW.TrueLayer.Pokemon.Api.exe`
* Console window will open, leave open whilst using API.

## Usage notes
* Translation API is rate limited to 5 requests. Appropriate response will be given when this limit is reached.
* Requests to PokeAPI and Translation API are cached for 10 minutes each.

## Project notes
* `Api` contains the web API code, which essentially is just the endpoint with some error handling.
* `Api` also contains the appsettings.json file which configures the paths for the APIs
* `Engine` is the main library, which is using Repository pattern and configures dependency injection requirements.
* `Engine.Tests` contains tests for Engine library. Containers are used to provide services with mocked entities for easy usage in tests. Test project isn't "fully" done, but I've covered the different types of tests, and in the interest of time not done areas where the tests are very similar to existing tests or trivial.
