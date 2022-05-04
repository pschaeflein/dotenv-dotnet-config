# dotenv-dotnet-config

A fork of Dotenv that supports specifying a colon (':') in the variable name. This allows [.Net configuration binding to objects](https://docs.microsoft.com/en-us/dotnet/core/extensions/configuration).

These .env file entries:

```dosini
KeyOne=1
KeyTwo=true
KeyThree:Message= "Thanks for checking this out!"
```

are equivalent to the following appsettings.json:

```json
{
    "KeyOne": 1,
    "KeyTwo": true,
    "KeyThree": {
        "Message": "Thanks for checking this out!"
    }
}
```

```csharp
// Get values from the config given their key and their target type.
int keyOneValue = config.GetValue<int>("KeyOne");
bool keyTwoValue = config.GetValue<bool>("KeyTwo");
string keyThreeNestedValue = config.GetValue<string>("KeyThree:Message");
```

## Install

```bash
# install locally (recommended)
npm install dotenv-dotnet-config --save
```

## Usage

Refer to [dotenv documentation](https://www.npmjs.com/package/dotenv).







## Contributing Guide

See [CONTRIBUTING.md](CONTRIBUTING.md)

## CHANGELOG

See [CHANGELOG.md](CHANGELOG.md)
