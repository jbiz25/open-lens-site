---
title: OpenLens privacy policy
---

# OpenLens privacy policy

Last updated: 12 November 2026

OpenLens is an iPhone camera app that uploads the photos and videos you take to
your own Google Drive. This policy explains what data the app handles and where it goes.

## The short version

- OpenLens has **no server and no account system** of its own. The developer
  never receives your photos, your Google account details, or any usage data.
- Your photos and videos go from your phone directly to **your** Google Drive,
  and nowhere else.
- One optional feature, off unless you add your own OpenRouter key, sends a
  pump curve sheet or a pump's make and model to an AI service (see "AI curve
  help" below).
- The app contains no analytics, advertising, or tracking code.

## Data the app handles

**Photos and videos you take.** Each photo or video is saved in the app's private storage on your
phone until it has been uploaded to Google Drive, then the local copy is
deleted. A small preview image of each one (without location or other
metadata) stays in the app so the Uploads list can show it, until you clear it
from that list. If you turn on "Also save to Photos", a copy is also written to your
Apple Photos library. If the app can't store a photo or video for upload
(usually because the phone is full), it saves it to your Photos library
instead so it isn't lost, and tells you. Videos include the sound recorded by the microphone.
Files include whatever metadata the camera records, such as date and device
model.

**Google account access.** When you sign in, Google gives the app an access
token and a refresh token, plus your Google account's email address (and, for
a Google Workspace account, its organization's domain). These are stored only
in the iOS Keychain on your phone. The tokens are used only to talk to Google
Drive on your behalf. The email address is shown in Settings and its domain is
checked on the phone to decide whether to show tools made for a particular
organization; it is never sent anywhere. Signing out in the app deletes all of
it from the phone and asks Google to revoke the tokens.

**Photos you add from your library.** If you use "Add from Photos", Apple's
photo picker lets the app see only the items you select; it gets no other
access to your library. Those items are uploaded exactly as stored, with the
metadata they already contain, such as date, camera details and location.

**Location.** Unless you turn off "Save location" in the app's settings, the
app reads your location while the camera is open. It writes the coordinates,
altitude and compass direction into each photo and video, as the iPhone camera
does, and adds them with the nearest street address to the file's description
in your Google Drive. To find that address, the app sends the coordinates to
Apple's location service. The app also remembers on your phone roughly where
you last used each folder, so it can suggest the right folder when you return.
In pump audit mode, each pump's position is worked out from where its photos
were taken (or where you move its pin) and saved in the audit file and the
pump's report in your Google Drive. The pump map shows them on Apple Maps,
which loads the map for the area on screen from Apple, as any map app does.
Location is never sent to the developer.

**Folder names and readings you speak.** If you use the microphone button to
name a folder, or "Say readings" in a pump audit, speech is recognized on your
iPhone and the audio is not sent anywhere, including to Apple, and is not kept.
Readings you then choose to use are saved in the audit like typed ones. Where
the phone cannot do this on the device, the button is hidden.

**Pump audits.** Audit mode appears only when you are signed in with a Google
account of an organization OpenLens has been set up for. In audit mode, what you type (site and contact details,
readings, checks and notes) is saved on your phone and uploaded to the
audit's folder in your Google Drive as `audit.json`, next to the photos.
The text on pump and motor nameplate photos is read on your iPhone with
Apple's built-in text recognition, to fill in the plate fields; nothing is
sent anywhere for that. The text read is kept in `audit.json`.

**AI curve help (optional, off by default).** If you type your own
[OpenRouter](https://openrouter.ai) API key into Settings, three buttons
appear, two of them in the curve tracer. "Read the curve with AI" sends the picture of the curve
sheet you opened, and the pump's manufacturer, model, impeller size, speed and
rated flow and head, to OpenRouter, which passes them to the AI model chosen in
Settings. "Search the web for the sheet" sends the same pump details (no
picture) to OpenRouter, which runs a web search with them. "Read the plates
with AI" on the Pump tab sends that pump's nameplate photos, for plates the
phone could not read by itself. Nothing is sent
until you tap one of those three buttons, and nothing else from the audit (site,
contacts, photos, location, readings) is ever included. Opening a search result
downloads that file straight from the website it is on. OpenRouter and the
model's provider handle what they receive under their own policies; providers
of free models may keep prompts and use them to improve their models. The key
is stored only in the iOS Keychain on your phone and is removed with "Remove
the key". The developer never sees the key or anything sent with it.

**Interviews you record.** If you record an interview in an audit, the audio
is saved on your phone and uploaded to the audit's Drive folder. It is
transcribed on your iPhone with Apple's on-device speech recognition; the
audio is not sent to Apple or the developer for that. The first time, the
phone may download Apple's speech model for your language. The transcript is
uploaded next to the recording and kept in `audit.json`. The phone keeps its
copy of the recording until the audit is finished or discarded. The app asks
you to confirm that everyone agreed to be recorded before it starts.

**Videos in an audit.** A video you record for a pump in audit mode is
uploaded to that pump's Drive folder like any video. On your iPhone, the app
also reads nameplate text off its frames (to fill empty plate fields) and
transcribes its sound with Apple's on-device speech recognition; nothing is
sent to Apple or the developer for that. The transcript is uploaded next to
the video and kept in `audit.json`, with any readings heard in it, which are
only filled in if you tap Use. The phone's working copy of the video is
deleted once it has been read.

**Settings.** Your preferences (folder name, photo format and so on) are
stored on your phone.

## Google user data

OpenLens requests these Google OAuth scopes:

- `https://www.googleapis.com/auth/drive.file`, for Google Drive;
- `openid` and `email`, to read the signed-in account's email address and,
  for Google Workspace accounts, its organization's domain.

With them the app can:

- create the upload folder, daily subfolders, and the folders you name in the
  app in your Drive;
- upload the photos and videos you take into those folders, with their date,
  location and folder in the file's description and properties;
- look up folders that OpenLens itself created earlier;
- download a photo or video that OpenLens uploaded, only when you open it in
  the app's Uploads list, to show it to you on your phone. The downloaded copy
  is temporary and is deleted when you close it.

- read the email address of the account you signed in with, to show it in
  Settings and to check on the phone whether it belongs to an organization the
  app's company tools are made for.

It **cannot** see, read, modify or delete any other file or folder in your
Drive. The app does not read your name, profile picture or contacts, and your
email address never leaves your phone.

Google user data is not shared with, transferred to, or sold to anyone. It is
not used for advertising, and it is not used to develop, improve or train
artificial-intelligence or machine-learning models. OpenLens's use of
information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Permissions on your phone

- **Camera**: to take photos and videos.
- **Microphone** (asked the first time you switch to video or record an
  interview): to record sound with videos, record interviews you start, and
  hear spoken folder names. If you decline, videos are recorded without
  sound and interviews can't be recorded.
- **Photos library**: not needed for "Add from Photos", which uses Apple's
  picker. Only asked for (add-only) if you turn on "Also save to Photos", or
  if a photo can't be stored for upload and is saved to Photos instead.
- **Location** (While Using the App): to save where each photo and video was
  taken and suggest nearby folders.
- **Motion & Fitness** (only when you open an audit's suction conditions):
  to read the air pressure from the iPhone's barometer for the NPSH
  calculation. It is saved in the audit.
- **Speech recognition** (only if you use the microphone button, or record an
  interview on a phone older than iOS 26): to turn speech into text, on the
  phone.
- **Add to Photos** (only if you enable "Also save to Photos", or when a
  photo can't be stored for upload): to save a copy.
- **Notifications** (only if you enable upload-failure alerts): to tell you
  when a background upload failed. These are generated on the phone itself.

## Retention and deletion

- Photos and videos waiting to upload stay on your phone until they upload or you delete
  them in the Uploads screen. Deleting the app removes them.
- Small previews of uploaded items stay on your phone until you delete them in
  the Uploads screen (swipe to delete, or "Clear completed"), or delete the app.
  The app removes them itself 30 days after the upload. Previews of an audit
  in progress stay until that audit is finished.
- Interview recordings stay on your phone until the audit is finished or
  discarded (the uploaded copy is in Drive).
- When a pump audit is finished, a copy of it (what was typed, not the photos
  or recordings) stays on your phone so the next visit to the same site can
  start from it. Only the latest audit per site is kept, for at most 30 sites.
  "Forget past audits" in Settings, or deleting the app, removes them.
- Uploaded photos and videos live in your Google Drive and are governed by your Google
  account. Delete them there as you would any other file.
- To remove the app's access entirely, sign out in the app or remove OpenLens
  at <https://myaccount.google.com/permissions>.

## Children

OpenLens is not directed at children and does not knowingly collect data from
anyone.

## Changes

If this policy changes, the updated version will be published at this address
with a new date.

## Contact

Questions about this policy can be sent to the support email address shown on
the Google sign-in screen for OpenLens.
