---
title: "translationPreferences resource type"
description: "A resource representing the user's translation settings preferences."
localization_priority: Normal
author: "jasonbro"
ms.prod: "microsoft-identity-platform"
doc_type: resourcePageType
---
# translationPreferences resource type

Namespace: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

An entry into the translation language override list 

## Properties

|Property             |Type                 		  			    |Description                                                            |
|---------------------|-------------------------------------------------------------|-----------------------------------------------------------------------|
|translationBehavior  |[translationBehavior](#translationBehavior-values)  	    |The user's preferred translation behavior.<br><br>Returned by default. |                   
|languageOverrides    |[translationOverride](translationLanguageOverride.md) collection                |The override behavior for the language tag.<br><br>Returned by default.|
|untranslatedLanguages|String collection| The list of languages the user does not need translated. This is computed from [regionalAndLanguageSettings](regionalandlanguagesettings.md) authoring languages collection and the languageOverrides collection. The list returned will contain neutral language cultures. <br><br> Read only. Returns by default.| 

### translationBehavior values

|Values |Description                                                                  |
|-------|-----------------------------------------------------------------------------|
|Ask    |Prompt the user before translating the messages/chats/web pages for the user.|
|Yes    |Automatically translate the messages/chats/web pages for the user.           |
|No     |Do not offer prompted or automatic translation for the user.                 |



## JSON representation

The following is a JSON definition of the resource.

<!--{
  "blockType": "resource",
  "optionalProperties": [],
  "baseType": "",
  "@odata.type": "microsoft.graph.translationPreferences"
}-->

```json
{
    "translationBehavior": "string",
    "languageOverrides": {"@odata.type":"microsoft.graph.translationLanguageOverride"},
    "untranslatedLanguages": ["string"]
}
```
<!-- {
  "type": "#page.annotation",
  "description": translationPreferences resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

