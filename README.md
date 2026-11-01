# Cull

A free photo culling tool that runs in your browser. Drop in a RAW shoot, and Cull sorts it into Keep, Maybe and Reject before you ever open Lightroom.

No install. No account. Your photos never leave your computer.

## What it does

- Flags soft focus, closed eyes and near-duplicate bursts
- Stacks bursts so you can pick your favorite frame fast
- Picks the best of each burst
- Marks your best-of-the-best shots with a blue Highlight
- Keeps a Library of every shoot you've culled
- Writes star ratings and color labels to XMP files so Lightroom picks them up

## Use it

Open the live version: **https://nikkerdoo.github.io/cull/**

Or download `index.html` and open it in Chrome or Edge. That's it.

You need **Chrome or Edge on a computer**. Safari and Firefox can't open folders this way.

## Quick start

1. Click **Add a folder**.
2. Drag in a shoot folder (or click **Choose folder**) and allow access.
3. Wait while Cull analyzes the photos.
4. Review, change any call you disagree with, then click **Write XMP ratings**.
5. Import the folder into Lightroom. Your ratings come along.

## Supported files

CR2, CR3, NEF, NRW, ARW, DNG, RAF, ORF, RW2, PEF, SRW, JPG and JPEG.

## What the colors mean

| Color | Meaning |
| --- | --- |
| Green | Keep |
| Gold | Maybe |
| Red | Reject |
| Blue | Highlight |
| Orange pill | Soft focus |
| Purple pill | Eyes closed |
| Pink pill | Best of burst / Burst dupe |

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| Left / Right | Next stack or photo |
| Up / Down | Move through a burst stack |
| K / M / X | Keep / Maybe / Reject |
| H | Highlight |
| S | Move the Keep or Highlight to this frame |
| Z | Zoom to 100% on a face |
| Esc | Close |

## What goes to Lightroom

| Your call | Lightroom gets |
| --- | --- |
| Keep | 3 stars, green |
| Maybe | 2 stars, yellow |
| Reject | Rejected, red |
| Highlight | 5 stars, blue |

Cull adds an `.xmp` file next to each photo. If one already exists, Cull adds to it and leaves your other edits alone. In Lightroom, import the folder, or for a folder already in your catalog choose **Metadata > Read Metadata from Files**.

## Important: where your info is saved

Cull has no server. Your Library, analysis and calls live in your browser's storage on that one computer.

- Clearing site data, cookies or history can erase them.
- A different browser, profile, incognito window or computer starts empty.
- Click **Write XMP ratings** when you finish a shoot, and use **Library > Export backup** now and then.

### Switching computers

1. Export a backup on the old computer.
2. Copy the `.json` file over.
3. Open Cull on the new one and click **Import backup**.
4. Click each shoot marked **FOLDER NEEDS LINKED** and pick its folder.

Backups hold names, counts, covers and your calls. They don't hold photos or folder locations.

## Good to know

- Eye detection loads a small face model from the internet the first time it analyzes new photos.
- 100% zoom shows the preview embedded in the RAW, not the full sensor image.
- RAW + JPEG pairs count as one photo (the RAW).
- Remove from Library never touches your photos.

## Privacy

Everything runs locally in your browser. Photos are never uploaded. The only network request is loading the face detection model (MediaPipe) when needed.

## Built with

A single HTML file, plain JavaScript, the File System Access API and [MediaPipe Face Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/face_landmarker).

## License

Free to use, change and share. Not for resale.

[PolyForm Noncommercial 1.0.0](https://polyformproject.org/licenses/noncommercial/1.0.0), plus a note: photographers can use Cull in their own work, including paid client work. You can't sell it or put it inside a paid product. See [LICENSE](LICENSE).

Made by [Nicole Marie Portraits](https://nicolemarieportraits.com).
