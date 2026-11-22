<p align="center">
  <img src="assets/icons/takara-256.png" alt="Takara icon" width="128">
</p>

<h1 align="center">Takara</h1>

<p align="center">
  <strong>Your S3 buckets, on your Mac.</strong><br>
  Connect, browse, upload, download, and share, on Garage, Amazon S3, Cloudflare R2, MinIO, and
  any other S3-compatible store.
</p>

<p align="center">
  <a href="https://github.com/kakilangit/takara/releases/latest"><img src="https://img.shields.io/github/v/release/kakilangit/takara?label=download" alt="Latest release"></a>
  <img src="https://img.shields.io/badge/macOS-Apple%20silicon%20%26%20Intel-black" alt="macOS, Apple silicon and Intel">
  <img src="https://img.shields.io/badge/price-free-brightgreen" alt="Free">
</p>

<p align="center">
  <em>Takara</em> (宝, Japanese for "treasure"). Say it "ta-ka-ra".
</p>

<p align="center">
  <img src="https://raw.githubusercontent.com/kakilangit/static/64fed1da510a9a0e4bdf7a9f59f230bfc6505d90/takara/takara_screenshot.png" alt="Takara showing the local pane, a bucket's contents, and the inspector" width="900">
</p>

---

Takara is a native macOS app for managing objects in an S3-compatible store. Built for
[Garage](https://garagehq.deuxfleurs.fr) first, the store Takara was written for, and at home on
Amazon S3, Cloudflare R2, MinIO, and whatever else speaks S3.

## What it does

- **A tab per task.** Each tab is a whole place: connection, bucket, prefix, local folder. You
  get eight. Chips in the title bar switch connection or bucket without leaving the listing, and
  `⌘[` / `⌘]` walk back through where you've been.
- **Connect to what you run.** The form asks each service for what it needs: a region for Amazon
  S3, an account id for Cloudflare R2, an address for Garage and MinIO. It builds the endpoint
  for you and tests the connection before saving, and a failure comes with the one fix that gets
  further. Credentials live in your Keychain, never in a file.
- **Browse.** Two panes: your Mac's folders on the left, the bucket on the right. Path bars,
  sortable columns, a filter that counts what it shows, a prefix search that asks the server, and
  a listing that stays quick at 100,000 keys. `⌘K` jumps to a connection, bucket, or typed path.
- **Move files.** Select rows and a send bar names where they'll land, so "upload" finally
  answers the question it used to raise. Folders keep their structure, and you can pause, resume,
  cancel, and retry. The Activity drawer says what's moving and how fast, and one queue serves
  the window, so a job outlives the tab that started it.
- **Edit the listing.** Rename files and folders, delete, make folders, and copy a presigned
  link for an object.
- **Production looks like Production.** The inspector shows size, type, dates, ETag, storage
  class, visibility, and metadata. A connection can wear an environment color across the window,
  and a delete on a Red one names the bucket and the count before it acts. At 2 a.m., that
  matters.

Takara asks the server what it supports and offers only what works there; where a feature isn't
available it says why instead of showing a dead control.

## Install

With [Homebrew](https://brew.sh):

```sh
brew install --cask kakilangit/tap/takara
```

Or download `Takara-<version>-universal.dmg` from
[Releases](https://github.com/kakilangit/takara/releases/latest) and drag Takara to Applications.
Runs on Apple silicon and Intel Macs.

> [!NOTE]
> Takara isn't notarized yet, so macOS blocks it at first. Homebrew takes care of that for you. If
> you installed from the `.dmg`, run:
>
> ```sh
> xattr -cr /Applications/Takara.app
> ```

To remove the secrets Takara keeps in your Keychain, delete the `dev.kakilangit.takara` items in
Keychain Access.

## Feedback

Bug reports and ideas are welcome in [Issues](https://github.com/kakilangit/takara/issues).

## License

Free to use, not open source. See [LICENSE](LICENSE).
