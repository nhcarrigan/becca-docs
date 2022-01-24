# Translating Becca

We are using Crowdin as our translation platform. While Discord supports 30 different languages, our limited budget means at the moment we are relying on Crowdin's free tier. We have selected the top 12 languages that discord supports. As this grows, we may be able to support additional languages.

Be sure to [join our support server](https://chat.nhcarrigan.com) and let us know you're interested in translating. We'll give you a special role so you can access a private channel just for our translation team.

## Getting Started

Navigate to the [Crowdin Project](https://crowdin.com/project/becca-lyria) and sign in (or sign up). From there, you can select the language you wish to translate, and Crowdin will display a list of available files for translation.

The available files are:

- `commands.json` - This is the bulk of the content, containing all of Becca's specific responses for commands. These will include embedded text.
- `contexts.json` - This contains Becca's responses for her context menu commands.
- `defaults.json` - This contains Becca's responses for things like the donation link, the error handler, and the moderation DM module.
- `events.json` - This contains the text for various event logs, such as member joins and thread events.
- `listeners.json` - This contains text for the listeners, such as the automod system.
- `responses.json` - This contains Becca's more default responses, such as when the guild object is missing, or when a user doesn't have permissions for a command.
- `sass.json` - This contains the text for Becca's sass module.

## Translating Text

Once you have selected a language and file, you will be taken to Crowdin's editor where you can see the list of sentences to translate. As you begin applying translations, please note the following:

- Some languages use "gendered" terms - if you aren't sure which to apply, ask in the translators chat or comment on the string on Crowdin.
- Text within `{{braces}}` are placeholders for the bot's responses. These are not translated, and should be left as is.
- Text within `[brackets](https://example.com)` are links to other pages on the website. The link text, `[brackets]`, should be translated, but the `(link)` should not.
- All other text should be good to translate.

## Proofreading Text

As a language nears completion, we will approach active translators and offer them proofreader privileges. Proofreaders are the final source of verification, and can approve a translation as accurate. Once approved, a translation will be included in the next download run.

As a proofreader, it is very important that you confirm translations are accurate and not misleading.
