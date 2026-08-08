# Karaokid

  **Sing along with lyrics right in your Rokid Glasses!**

  Karaokid is an Android karaoke system for Rokid Glasses. Search for a song on your phone, download and process it locally, remove the vocals, and display synchronized lyrics inside your glasses.

  The phone handles song discovery, audio processing, playback, and synchronization. The glasses display the lyrics on a smooth, head-tracked window.

  ## Features

  ### Phone app

  - Search for songs and synchronized lyrics.
  - Find matching audio and process it directly on the phone.
  - On-device vocal separation—no external processing server required.
  - Queue multiple songs for processing.
  - Export the bundled glasses app using **Save Rokid Glasses APK**.
  - Automatically runs a Bluetooth foreground service after initial setup.

  ### Rokid Glasses app

  - Active lyrics displayed prominently on a floating window.
  - Upcoming lyrics appear below the active line.
  - Per-line progress indicators.
  - Optional gyro movement.
  - Smooth Follow mode that returns lyrics to the center of your view.
  - Stationary Lyrics mode that disables head tracking.
  - Adjustable lyric-box height and size.

  ## How it works

  Audio processing and playback happen entirely on the Android phone. Internet access is required when searching for and aquiring new songs, but saved songs can be played locally afterward.

  ## Requirements

  - An Android phone.
  - Rokid Display Glasses capable of installing Android APKs.
  - Bluetooth
  - The phone and glasses must be paired through Android Bluetooth settings.
  - A reasonably modern ARM64 Android phone is recommended for vocal separation.

  ## Installation

  ### 1. Install the phone app

  Install:

  ```text
  Karaokid-Android.apk

  Install the app (may need to enable 'Install from Unknown Sources' or disable Google Play Protect temporarily.

  Open the app once and grant the requested Bluetooth and notification permissions. App may need to be restarted.

  The notification allows Karaokid’s foreground service to maintain the glasses connection while the main phone interface is closed.

  ### 2. Export the glasses app

  In the phone app, press:

  'Save Rokid Glasses APK'

  Choose a location on your phone. The app will save:

  Karaokid-Glasses.apk

  Transfer this APK to the glasses and install it manually via the Hi Rokid App or through other means.

  You may need to enable installation from unknown sources on the glasses.

  ### 3. Pair the devices

  Ensure glasses and phone are already paired via Bluetooth.

  ### 4. Start Karaokid

  1. Open Karaokid on the phone at least once.
  2. Open Karaokid on the glasses.
  3. The glasses will search their paired devices for a phone running Karaokid.
  4. After the process completes, the glasses should display Phone connected.

  The glasses automatically retry the connection if the phone is temporarily unavailable.

  ## Using the app

  ### Searching and processing

  1. Enter a song title or artist.
  2. Press Search.
  3. Select a result from the popup.
  4. Wait for downloading and vocal separation to finish.
  5. Playback begins when the song is ready.

  Additional selections can be placed in the processing queue while another song is running.

  ### Saved Songs

  Open the hamburger menu to access Saved Songs.

  - Tap a song to play it.
  - Long-press a song to open its deletion menu.

  ### Playback controls

  - Play/Pause: Start or pause playback.
  - Rewind/Restart:
      - Single tap normally rewinds 10 seconds.
      - When pressed during the first three seconds, it plays the previous Saved Song when available.
      - Double tap restarts the current song.

  - Next: Plays the next Saved Song.
      - When the final song is reached, playback loops to the first saved song.

  ## Lyrics tracking settings

  Open the gear icon to configure the glasses display.

  ### Accelerometer Movement

  Allows small positional lyric movements based on motion detected by the glasses.

  Disabling this option can improve tracking responsiveness on slower hardware.

  ### Lyrics Smooth Follow

  Smoothly returns the lyric window to the front of your view when your head movement settles.

  ### Stationary Lyrics

  Disables sensor-based movement and keeps the lyric interface fixed in the viewport.

  ### Lyric Box Height

  Moves the complete lyric box vertically.

  ### Lyric Box Size

  Adjusts the overall size and wrapping width of the lyric display.

  ### Debug UI

  Shows or hides sensor and tracking information on the glasses.

  ## Bluetooth connection

  For automatic connection:

  - Bluetooth must be enabled on both devices.
  - The phone and glasses must already be paired.
  - Bluetooth permissions must be granted to both apps.
  - Compatible versions of Karaokid must be installed.
  - The phone service must have been started at least once.

 
  If multiple phones are paired with the glasses, the glasses try paired phone-class devices until they find one running the compatible Karaokid service.

  ## Troubleshooting

  ### The glasses cannot find the phone

  - Confirm the devices are paired in Android Bluetooth settings.
  - Open the phone app once.
  - Confirm Bluetooth permissions are granted.
  - Confirm the Karaokid foreground-service notification is present.
  - Restart the glasses app.
  - Toggle Bluetooth off and on.
  - Remove and pair the devices again if necessary.

  ### Lyrics do not appear

  - Confirm the glasses display Phone connected.
  - Make sure a song has finished processing.
  - Verify the selected result contains synchronized lyrics.
  - Try seeking slightly forward in the song.

  ### Processing is slow

  Vocal separation is computationally expensive. Processing time depends on:

  - Phone processor.
  - Available memory.
  - Thermal throttling.
  - Song duration.
  - Other applications running in the background.

  Keep the phone cool and avoid running other demanding applications during separation.

  ### Installation fails on the glasses

  - Enable installation from unknown sources.
  - Export a fresh copy using the phone app.
  - Remove an older incompatible installation if Android reports a signature conflict.
  - Confirm that you are installing Karaokid-Glasses.apk, not the phone APK.
