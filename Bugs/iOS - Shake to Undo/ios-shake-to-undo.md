# Important Bug Found: iOS Real-world QA Testing: Shake-to-Undo

Today as we continue our series of `crowdtested bugs` we're taking a look at the latest iOS bug discovered by the testers here at Test.io: the `iOS Shake-to-Undo` bug.  This bug causes affected apps to crash when attempting to use the `Shake-to-Undo` feature provided on iOS versions 10 and above.  Let's dig a bit deeper into what steps we found that could reproduce the bug and how these sorts of defects are often overlooked during production testing, only to be later discovered by `crowdtesting` after release.

## Reproducing the Bug

To reproduce the `iOS Shake-to-Undo` bug, we need to follow just a handful of simple steps:

1. Run the `Red Bull TV` application version `3.3.0.38`.
2. Click on the magnifying glass.
3. Type at least one letter into the input field.
4. Click on the `X (delete)` button on the right end of the input field.
5. Shake the device.
6. When the confirmation window pops up with option `Undo typing`, click on `Undo`.

__Expected Result__

The application should do nothing, since there is no text to undo at this point, as it was already deleted by clicking the `X (delete)` button.

__Actual Result__

The application simply crashes completely. It attempts to delete the letters that were last entered, but fails to do so since that text no longer exists.  Instead of gracefully resolving this conflict and ignoring the missing text, it crashes entirely.

## Similar Examples

This is hardly the first time Apple has released a version of iOS with a faulty feature that presents a bug which could potentially impact hundreds of applications.  In late November of 2016, another similar `crowdtested` bug was discovered by users of the common discussion site [`Reddit`].  This defect, which was known as the `corrupt .mp4` bug, would cause most iOS devices to slow down and eventually freeze up entirely when playing a corrupt `.mp4` video file.  The reproduction of the bug in this case was simply a matter of opening a corrupted video file in a variety of iOS application, which when then cause iOS to generate an endless loop in the video player.

It was discovered that this issue would occur on a variety of modern iOS versions from 9 - 10+, and could also occur within a variety of applications from `AirDrop` and `Photos App` to `Mail` and even `Instagram`.  Once the video was played for a few seconds, an infinite loop would begin and the phone itself would become slower and slower, until eventually a hard freeze would occur.  The only way to resolve this issue was with a hard reset by holding the `power` and `home` buttons simultaneously.  Thankfully this issue caused no permanent harm, as affected devices were able to function normally following a hard reset.

Both the `corrupt .mp4` bug and the more recent `iOS Shake-to-Undo` bug prove is that properly `crowdtesting` software, even after release, is an extremely valuable tool that can often catch defects that are never even considered when performing standard in-house testing procedures.  While neither of these bugs present any permanent damage to the device, it's all too easy to imagine a loss of temporary data, such as filling out a web form or writing an email, when a hard freeze occurs and forces a reset of the device.

[`Reddit`]: https://www.reddit.com/r/jailbreak/comments/5e5y9r/discussion_warning_this_video_kills_your_iphone/

---

__SOURCES__

- https://www.reddit.com/r/jailbreak/comments/5e5y9r/discussion_warning_this_video_kills_your_iphone/?st=IVSKMNC4&sh=45a49cc1
- https://www.reddit.com/r/apple/comments/5e6jo7/warningpsa_newly_released_video_crashed_ios_10/
