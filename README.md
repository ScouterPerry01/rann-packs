# RANN recognition packs

Free face and object recognition packs for **RANN Ultra Searcher**. The app lists them in
**Settings → Recognition engines → Available online** and downloads them from here; there is nothing to do by hand.

| Pack | What it does | Models and licences |
| --- | --- | --- |
| Free face recognition | Finds faces and tells people apart | YuNet (MIT) and SFace (Apache 2.0), from [OpenCV Zoo](https://github.com/opencv/opencv_zoo) |
| Free object recognition | Finds the 80 everyday kinds of object of the COCO dataset | YOLOX-S by Megvii (Apache 2.0), from [OpenCV Zoo](https://github.com/opencv/opencv_zoo) |

Every pack runs on your own computer; nothing is sent anywhere.

## What is here

- **Releases:** one per pack version, tagged `<pack id>-<version>` (for example `rann.free-faces-1.0`), with the
  `.rannpack` file attached.
- **packs.json:** the list the app reads, with each pack's size, SHA-256 and download address.
- **packs.json.sig:** RANN's signature on packs.json.

## Why you can trust a download

A `.rannpack` holds model data only, never code: the app runs the models with its own built-in code. RANN signs every
pack's manifest, which lists the SHA-256 of every model, and signs packs.json too. The app refuses a list or a pack
that isn't signed by RANN, and a download that isn't exactly the listed file. The models are unmodified, and each
pack includes their licence texts (LICENCE.txt).
