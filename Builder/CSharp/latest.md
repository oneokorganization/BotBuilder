---
layout: page
title: Releases
permalink: /builder/node/libraries/CSharp/latest/
weight: 560
parent1: Bot Builder for C#
---

Microsoft Bot Builder is a powerful framework for constructing bots that can handle both freeform interactions and more guided ones where the possibilities are explicitly shown to the user. It is easy to use and leverages C# to provide a natural way to write bots.

High Level Features:

* Powerful dialog system with dialogs that are isolated and composable.
* Built-in dialogs for simple things like Yes/No, strings, numbers, enumerations.
* Built-in dialogs that utilize powerful AI frameworks like LUIS.
* Bots are stateless which helps them scale.
* FormFlow for automatically generating a bot from a C# class for filling in the class and that supports help, navigation, clarification and confirmation.
* SDK source code is found on [http://github.com/Microsoft/botbuilder](http://github.com/Microsoft/botbuilder).

## Install
To install Microsoft.Bot.Builder, run the following command in the [Package Manager Console](http://docs.nuget.org/consume/package-manager-console)

    PM> Install-Package Microsoft.Bot.Builder

## Release Notes
The framework is still in preview mode so developers should expect breaking changes in future versions of the framework. A list of current issues can be found on our [GitHub Repository](https://github.com/Microsoft/BotBuilder/issues).

### [v1.1.0](https://www.nuget.org/packages/Microsoft.Bot.Builder/1.1.0)

* __Breaking Change:__ Rename some delegates and methods to be more consistent and to support dynamic field definition. Unless you were using Field or FieldReflector directly this should be transparent.
* Provide a way to dynamically define fields, confirmations and messages.
* Add FormCanceledException which provides information on what steps were completed and where the user quit.
* Add more flexibility on how parenthesis are used when generating prompts.
* Fix a number of bugs around initial state and LUIS entities.
* Extend chain model to support branching (Chain.Switch)
* Add support for resumption of a conversation
* Add Facebook OAuth Example

### [v1.0.2](https://www.nuget.org/packages/Microsoft.Bot.Builder/1.0.2)

* Move to IDialog<T> typed for result type
* Add support for linq query syntax (e.g. Select, SelectMany)
* Multiple IBotToUser.Post(Message) calls
* Move to Autofac dependency injection container
* IConnectorClient instantiated to point to emulator when emulating bot
* Fix CommandDialog<T>
* Update LUIS Models
* Add ChoiceCase, ChoiceParens to Form template attributes

### [v1.0.1](https://www.nuget.org/packages/Microsoft.Bot.Builder/1.0.1)
* Fixed LuisDialog to handle null score returned by Luis. This is because of a behavior change in Cortana pre-built apps by [Luis](http://luis.ai)
* Updated nuspec with better description 
* Added error resilient context store