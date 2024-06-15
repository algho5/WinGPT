# WinGPT

## How to use

1. Install [AutoHotkey v2](https://www.autohotkey.com/). Note that this script will not work on earlier versions of AutoHotkey.
2. Copy your OpenAI API key [here](https://platform.openai.com/account/api-keys) (you may need to create a new secret key‍)
3. Open `ChatGPT AutoHotkey Utility.ahk` using your favorite text editor
4. Launch `ChatGPT AutoHotkey Utility.ahk`
5. Paste your OpenAI API key on the `API_Key` variable
6. Highlight a text that you want to process using ChatGPT API and press the `back quote` key to bring up the menu

## Customizing menu, prompts, APIs, and hotkey

You can customize prompts and the menu order by doing the following:

## Menu

Under `Menus and ChatGPT prompts`, add a menu by adding this code:

```AutoHotkey
MenuPopup.Add("&8 - Text_To_Appear", Function_To_Execute_When_Selected)
```

The character next to the "and" sign (&) is the hotkey for that particular menu that, when pressed, activates it.

You can also add a line separator using this code:

```AutoHotkey
MenuPopup.Add()
```

## Prompt

You can add a prompt using this code:

```AutoHotkey
Function_To_Execute_When_Selected(*) {
    ChatGPT_Prompt := "Your prompt here:"
    Status_Message := "Status message that will show while processing the request"
    API_Model := "gpt-4" ; or API_Model := "gpt-3.5-turbo"
    ProcessRequest(ChatGPT_Prompt, Status_Message, API_Model, Retry_Status)
}
```

## APIs

You can edit the API used for each prompt by changing the `API_Model` under each prompt. Visit [this page](https://platform.openai.com/docs/models/gpt-4-turbo-and-gpt-4) to explore a selection of available API models.

## Hotkey

You can change the activation hotkey under Hotkey. See [here](https://www.autohotkey.com/docs/v2/KeyList.htm) for the list of possible hotkeys.
