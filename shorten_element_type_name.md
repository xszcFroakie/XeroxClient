# Shorten Name Table

| Shorten Element Name | Element Type | Shorten Animation Type Name | Animation Type |
| :-: | :-: | :-: | :-: |
| p | panel | aa | alpha |
| vsp | vertical stack panel | ao | offset |
| hsp | horizontal stack panel | acl | clip |
| cp | collection panel | ac | color |
| ip | input panel | afb | flip |
| l | label | as | size |
| i | image | au | uv |
| cr | custom renderer | w | wait |
| g | grid | aafb | aseprite flip book |
| f | factory |||
| b | button |||
| t | toggle |||
| sl | slider |||
| slb | slider box |||
| s | screen |||

## Simple Example

### Before

```json
{
    "namespace": "your_namespace",

    "example_panel": {
        "type": "panel",
        "size": [1, 1],
        "controls": [
            {
                "example_image": {
                    "type": "image",
                    "texture": "your/texture/path",
                    "size": [1, 1]
                }
            }
        ]
    },

    "example_anim": {
        "anim_type": "alpha",
        "from": 1.0,
        "to": 0.0,
        "easing": "out_cubic",
        "duration": 1.0
    }
}
```

### After

```json
{
    "namespace": "your_namespace",

    "example_panel@xerox_lib.p": {
        "size": [1, 1],
        "controls": [
            {
                "example_image@xerox_lib.i": {
                    "texture": "your/texture/path",
                    "size": [1, 1]
                }
            }
        ]
    },

    "example_anim@xerox_lib.aa": {
        "from": 1.0,
        "to": 0.0,
        "easing": "out_cubic",
        "duration": 1.0
    }
}
```
