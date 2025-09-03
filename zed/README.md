# Zed Configuration Guide

## Setting Up Zed

Zed uses REST API from Github to fetch for latest updates of the extensions. But if you are not authenticated with your Github account, you will likely to hit the rate limit of the API. To avoid this, you can use Github CLI to authenticate yourself.

See: <https://docs.github.com/en/rest/using-the-rest-api/getting-started-with-the-rest-api?apiVersion=2022-11-28#rate-limiting%5C>

```sh
brew install gh
gh auth login
```

```sh
// Zed settings
//
// For information on how to configure Zed, see the Zed
// documentation: https://zed.dev/docs/configuring-zed
//
// To see all of Zed's default settings without changing your
// custom settings, run `zed: open default settings` from the
// command palette (cmd-shift-p / ctrl-shift-p)
{
  "features": {
    "edit_prediction_provider": "copilot"
  },
  "vim_mode": true,
  "ui_font_size": 15,
  "buffer_font_size": 14,
  "buffer_font_family": "Source Code Pro",
  "theme": {
    "mode": "system",
    "light": "Ayu Light",
    "dark": "Gruvbox Dark"
  },
  "relative_line_numbers": true,
  "autosave": "on_window_change",
  "cursor_blink": false,
  "scroll_beyond_last_line": "off",
  "vertical_scroll_margin": 5,

  // mimimap and scrollbar settings
  "minimap": {
    "show": "always",
    "thumb": "always",
    "thumb_border": "left_open",
    "current_line_highlight": null
  },
  "scrollbar": {
    "show": "never"
  },

  // llm ability
  // agent
  "agent": {
    "inline_assistant_model": {
      "provider": "google",
      "model": "gemini-2.5-flash-lite-preview"
    },
    "default_profile": "ask",
    "default_model": {
      "provider": "google",
      "model": "gemini-2.5-pro"
    }
  },
  "language_models": {
    "openai_compatible": {
      "Poe": {
        "api_url": "https://api.poe.com/v1",
        "available_models": [
          {
            "name": "Claude-Sonnet-4",
            "display_name": null,
            "max_tokens": 200000,
            "max_output_tokens": 32000,
            "max_completion_tokens": 200000,
            "capabilities": {
              "tools": false,
              "images": false,
              "parallel_tool_calls": false,
              "prompt_cache_key": false
            }
          },
          {
            "name": "GPT-5",
            "display_name": null,
            "max_tokens": 200000,
            "max_output_tokens": 32000,
            "max_completion_tokens": 200000,
            "capabilities": {
              "tools": false,
              "images": false,
              "parallel_tool_calls": false,
              "prompt_cache_key": false
            }
          }
        ]
      }
    }
  }
}
```
