# adhkar-audio-data

Audio files for the Adhkar / Hisn al-Muslim section of the **Muflihin Pro** app.

أصوات الأذكار (حصن المسلم) المستعملة في تطبيق «مفلحين برو». الملفات في `audio/` وقائمتها مع الأحجام وبصمات SHA-256 في `index.json`.

## Source / المصدر

- The 397 MP3 files are an **unchanged copy** of the `audio/` folder of
  [rn0x/Adhkar-json](https://github.com/rn0x/Adhkar-json) (verified byte-for-byte by Git blob hash against the upstream files).
- Text of the adhkar: *Hisn al-Muslim* by Sa'id bin Ali bin Wahf al-Qahtani. Recitation: Hamad al-Dreihem (as credited by the upstream README).
- Upstream licence statement (Arabic, quoted from its README): the files carry no licence and may be used freely without legal liability.
  All rights in the underlying text and recitation remain with their original authors.
- If you are a rights holder and want a file removed, open an issue in this repository.

## Use / الاستعمال

The app fetches files from a pinned tag, so jsDelivr can cache them permanently:

```
https://cdn.jsdelivr.net/gh/Younes12345698/adhkar-audio-data@v1/audio/<file>.mp3
https://raw.githubusercontent.com/Younes12345698/adhkar-audio-data/v1/audio/<file>.mp3   (fallback)
```

Changing any file means publishing a new tag (`v2`) and updating `ADHKAR_AUDIO_REF` in the app (`src/lib/adhkar-audio.ts`); never move an existing tag.
