---
title: OpenLens privacy policy
---

# OpenLens privacy policy

Last updated: 4 November 2026

OpenLens is an iPhone camera app that uploads the photos you take to your own
Google Drive. This policy explains what data the app handles and where it goes.

## The short version

- OpenLens has **no server and no account system** of its own. The developer
  never receives your photos, your Google account details, or any usage data.
- Your photos go from your phone directly to **your** Google Drive, and nowhere
  else.
- The app contains no analytics, advertising, or tracking code.

## Data the app handles

**Photos you take.** Each photo is saved in the app's private storage on your
phone until it has been uploaded to Google Drive, then the local copy is
deleted. If you turn on "Also save to Photos", a copy is also written to your
Apple Photos library. Photos include whatever metadata the camera records,
such as date and device model.

**Google account access.** When you sign in, Google gives the app an access
token and a refresh token. These are stored only in the iOS Keychain on your
phone and are used only to talk to Google Drive on your behalf. Signing out in
the app deletes them from the phone and asks Google to revoke them.

**Settings.** Your preferences (folder name, photo format and so on) are
stored on your phone.

## Google user data

OpenLens requests a single Google OAuth scope:
`https://www.googleapis.com/auth/drive.file`.

With it the app can:

- create the upload folder (and daily subfolders) in your Drive;
- upload the photos you take into those folders;
- look up folders that OpenLens itself created earlier.

It **cannot** see, read, modify or delete any other file or folder in your
Drive. The app does not read your Google profile, email address or contacts.

Google user data is not shared with, transferred to, or sold to anyone. It is
not used for advertising, and it is not used to develop, improve or train
artificial-intelligence or machine-learning models. OpenLens's use of
information received from Google APIs adheres to the
[Google API Services User Data Policy](https://developers.google.com/terms/api-services-user-data-policy),
including the Limited Use requirements.

## Permissions on your phone

- **Camera**: to take photos.
- **Add to Photos** (only if you enable "Also save to Photos"): to save a copy.
- **Notifications** (only if you enable upload-failure alerts): to tell you
  when a background upload failed. These are generated on the phone itself.

## Retention and deletion

- Photos waiting to upload stay on your phone until they upload or you delete
  them in the Uploads screen. Deleting the app removes them.
- Uploaded photos live in your Google Drive and are governed by your Google
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
