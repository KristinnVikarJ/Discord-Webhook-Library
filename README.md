# Discord-Webhook-Library
[![NuGet](https://img.shields.io/nuget/v/DiscordWebhooks?color=brightgreen?style=plastic)](https://www.nuget.org/packages/DiscordWebhooks) 

Easy to use Simple Discord Webhooks in C#

# Usage
Create a Webhook
```C#
Webhook webhook = new Webhook(WebhookURL);
```

Create the Webhook Data Object
```C#
WebhookObject obj = new WebhookObject()
{
  username = "example username",
  content = "example message"
} 
```

Then Post the Object
```C#
webhook.PostData(obj);
```

# Embed Example
```C#
Embed embed = new Embed()
{
  fields = new Field[]
  {
    new Field()
    {
      name = "Field1",
      value = "Field Value"
    }
  }
}
```

Here's An embed being used to post an image of a cat
```C#
Webhook webhook = new Webhook("");

WebhookObject obj = new WebhookObject()
{
  embeds = new Embed[]
  {
    new Embed()
    {
      image = new Image()
      {
        url = "https://cdn.pixabay.com/photo/2018/04/20/17/18/cat-3336579__340.jpg" //Image Of A Cat
      }
    }
  },
  username = "this is my username"
};

webhook.PostData(obj);
```
