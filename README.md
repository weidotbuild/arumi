<p align="center">
  <a href="https://arumi.ai"><img src="https://arumi.ai/og-arumi.jpg" alt="Arumi — AI images, video, audio and music in one studio" width="720"></a>
</p>

# Arumi

**[Arumi](https://arumi.ai) is an AI studio for images, video, audio and music.** Write a prompt, pick the model that fits the job, see the price in credits before you generate, and keep every result in one history.

- **55 models in one place** — 18 image, 35 video and 2 audio models, each with the settings its own model allows.
- **The price comes first** — every run shows its credit cost before you click. A successful run costs exactly that; a failed run costs nothing, or only what it already used — never more than the price shown.
- **No subscription** — credit packs are one-time payments. Nothing renews and there is nothing to cancel.
- **Works from your AI assistant** — a remote MCP server lets Claude Code, Codex, Cursor and other clients generate with your credits.

## What you can make

| | |
|---|---|
| [AI Image Generator](https://arumi.ai/ai-image-generator) | Images from a text prompt, or edits of your own pictures with reference images. |
| [AI Video Generator](https://arumi.ai/ai-video-generator) | Video from text or a still image, up to 30 seconds and 4K, many models with sound. |
| [AI Audio Generator](https://arumi.ai/ai-audio-generator) | Natural speech for voice-overs, narration and read-alouds. |
| [AI Music Generator](https://arumi.ai/ai-music-generator) | Instrumentals or full songs from a description or your own lyrics. |
| [AI Canvas](https://arumi.ai/canvas) | Chain prompts, images and video on one board and rerun any step. |

### One-step AI tools

[Background remover](https://arumi.ai/ai-tools/ai-background-remover) ·
[Image upscaler](https://arumi.ai/ai-tools/ai-image-upscaler) ·
[Object remover](https://arumi.ai/ai-tools/ai-object-remover) ·
[Background changer](https://arumi.ai/ai-tools/ai-background-changer) ·
[Old photo restoration](https://arumi.ai/ai-tools/ai-photo-restoration) ·
[Video upscaler](https://arumi.ai/ai-tools/ai-video-upscaler) ·
[Animate old photos](https://arumi.ai/ai-tools/animate-old-photos)

### Trends to try on your own photo

[Hotel Lobby AI video](https://arumi.ai/explore/hotel-lobby-ai-trend) ·
[Photo to anime](https://arumi.ai/explore/photo-to-anime) ·
[Photo to collage poster](https://arumi.ai/explore/photo-to-collage-poster) ·
[Photo to ugly doodle](https://arumi.ai/explore/photo-to-ugly-doodle) —
see them all in [Explore](https://arumi.ai/explore).

### Free tools that never upload your files

These run entirely in your browser: no sign-up, no credits, no watermark.

[Split image](https://arumi.ai/free-tools/split-image) ·
[Join images](https://arumi.ai/free-tools/join-images) ·
[Add watermark](https://arumi.ai/free-tools/add-watermark) ·
[Audio trimmer](https://arumi.ai/free-tools/audio-trim) ·
[MP3 to video](https://arumi.ai/free-tools/mp3-to-video) ·
[Video trimmer](https://arumi.ai/free-tools/video-trimmer) ·
[Add audio to video](https://arumi.ai/free-tools/add-audio-to-video)

## Use Arumi from Claude Code, Codex or Cursor (MCP)

Arumi is a remote [MCP](https://modelcontextprotocol.io) server over Streamable HTTP. Create an API key on the [API keys page](https://arumi.ai/api-keys), set a monthly credit limit for it, and add it to your assistant.

**Claude Code**

```sh
claude mcp add --transport http arumi https://api.arumi.ai/mcp --header "Authorization: Bearer YOUR_API_KEY"
```

**Codex**

```sh
export ARUMI_API_KEY="YOUR_API_KEY"
codex mcp add arumi --url https://api.arumi.ai/mcp --bearer-token-env-var ARUMI_API_KEY
```

**Cursor and other clients**

```json
{
  "mcpServers": {
    "arumi": {
      "url": "https://api.arumi.ai/mcp",
      "headers": { "Authorization": "Bearer YOUR_API_KEY" }
    }
  }
}
```

Then ask in plain words — *"Make a 5-second video of a lighthouse at dusk."* Your assistant checks the price first, then generates.

| Tool | What it does |
|---|---|
| `list_models`, `get_model` | Browse the 55 image, video and audio models and read one model's inputs and settings. |
| `quote`, `get_balance` | Get the credits a generation would cost and check the balance before anything is spent. |
| `generate`, `get_generation`, `list_generations` | Start a generation, follow it to the end and get links to the results. |
| `create_upload`, `complete_upload` | Upload your own image, video or audio and use it as a reference. |

Your assistant only spends credits within the monthly limit you set on the key. Full guide: [arumi.ai/mcp](https://arumi.ai/mcp).

## Pricing

One-time credit packs from $9.99 for 1,000 credits. Paid credits stay valid for 120 days from your latest purchase, and an unused pack can be refunded within 14 days. Sign-up credits are free. See [pricing](https://arumi.ai/pricing).

## Links

- Website: [arumi.ai](https://arumi.ai)
- MCP server: [arumi.ai/mcp](https://arumi.ai/mcp)
- Blog: [arumi.ai/blog](https://arumi.ai/blog)
- Support: support@arumi.ai
