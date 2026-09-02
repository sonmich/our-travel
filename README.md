# Japan Travel Map — iPhone & Android App

This project packages the existing `index.html` as a native iOS/Android app using Capacitor.

## 1. Put media files in `www/`

The current HTML references local media files such as:
- `japan_map.jpg`
- `sctc_airport.jpeg`
- `toya_lake.jpeg`
- `sfox.MOV`
- and the other images referenced by `spotData`.

Copy those files from the same folder as the original HTML into `www/`.

## 2. Install dependencies

On the Mac:

```bash
cd japan-travel-app
npm install
```

## 3. Create native projects

```bash
npx cap add ios
npx cap add android
npx cap sync
```

## 4. Open iPhone project

```bash
npx cap open ios
```

Xcode will open. Select an iPhone or simulator and Run.

For a real iPhone, sign the app with your Apple Developer account/team in Xcode.

## 5. Open Android project

```bash
npx cap open android
```

Android Studio will open. Select an emulator or connected Android phone and Run.

## Important

The existing local `.mov` video can be included in the app bundle, but iPhone/Android support depends on the video's codec/container. If `sfox.mov` does not play reliably, convert it to H.264 MP4 and change the URL in `spotData` to the `.mp4` file.
