# DiscordHooks (Simple discord webhooks for Go)
Simple package to send embeds to a Discord Webhook with Go
## Installation

```go get github.com/JuandeJuni/discordhooks```

## Usage

### Send Webhook with a single Embed

```
//Import the package

import (
    "github.com/JuandeJuni/discordhooks"
)

//Creating the Embed

embed = discordhooks.Embed{
    Title: "Title",
    Description: "Description",
    Color: 0x00ff00,
    Url: "https://google.com",
    Thumbnail: discordhooks.Thumbnail{
        Url: "https://www.trecebits.com/wp-content/uploads/2015/09/google.jpg",
    },
    Fields: []discordhooks.Field{
        discordhooks.Field{
            Name: "Field 1",
            Value: "Value 1",
        },
        discordhooks.Field{
            Name: "Field 2",
            Value: "Value 2",
        },
    },
}

//Sending the webhook

discordhooks.SendEmbed("https://discordapp.com/api/webhooks/your/webhook", embed)

```