# I just got a new business partner. Now what?

The Team RISE new partner deck as a website. Works on a phone, tablet, or computer, and anyone can edit it.

| Link | For |
|---|---|
| https://dwightrfm.github.io/rise-new-partner/ | Presenting. Send this to anyone. |
| https://dwightrfm.github.io/rise-new-partner/?edit | Editing. Words, pictures, and QR codes. |
| https://dwightrfm.github.io/rise-new-partner/how-to-edit.html | One-page guide for whoever edits. |

## Two ways to edit

- **Anyone, no key:** edits save on that device by themselves. "My copy" downloads their version as one self-contained file (presents offline on any computer).
- **Team key holders:** "Publish to team" commits the change to `index.html` here, so the presenting link changes for everyone in 1 to 2 minutes.

## How it is built

- Built from `Paul/Templates/rise-deck` (the Orientation look) with `python3 build.py <deck_dir> --site ~/rise-new-partner`.
- Once anyone publishes from the web, **this repo's `index.html` is the source of truth**. Rebuilding from the template would erase web edits.
- Every block of words carries a `data-e` number and every picture a `data-img` number. Keep them when editing by hand.

## The edit key

Publishing needs a GitHub fine-grained token that can only touch this one repo:
Settings, Developer settings, Fine-grained tokens, Generate new token. Repository access: only `rise-new-partner`. Permissions: Contents, Read and write. Nothing else.

To cut someone off, delete their token on that same page. To undo any publish, revert its commit.
