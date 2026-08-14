# 7b2f1ff

- Music now runs on SoundCloud only, the source picker is gone
- Custom playlists no longer have a colored icon, only Liked Songs does

# 918990a

Updated Akura Music UI to be a bit nicer

# 0867230

- You can now turn on notifications for a whole room, not just DMs and mentions
- Tap the bell in a room's header to get notified for every new message in it
- Private rooms notify without showing the message text, since it stays encrypted

# ed3b66a

- Closed a hole where right-clicking the password screen could skip the password entirely
- Chat no longer lets the message box slide off the bottom once a conversation gets long; the messages scroll instead
- Cleaned up chat on phones so the message box has room and messages use the full width
- The music player now follows your theme and accent colour instead of always being dark

# 23db7d8

- Music has a source picker now: switch between Akura Music and SoundCloud right in the sidebar
- SoundCloud gets you its own search, trending and full-length playback
- New download button on the player saves the song you're listening to, from either source

# 9a74c0f

- Music actually loads and plays again: it now tries a whole list of sources instead of the one that was down, and plays full songs, not 30 second clips
- Seeking works anywhere in a track, and a dead source no longer freezes playback
- Client code now carries an extra scrambling layer on top of the existing obfuscation

# bc03bf4

- Music now talks to its source directly instead of everything going through Akura's server, so songs start quicker and no longer share one relay with everyone else
- If your network blocks it outright, it quietly falls back to the old way

# 86d36bd

- Akura Music plays whole songs now instead of cutting off after a 30 second preview
- Songs, charts and cover art come from Monochrome instead of Deezer, and seeking works anywhere in a track
- Playlists saved before this update will need their songs added again, the old ones cannot be looked up

# 3c31d83

- New Akura Music: search real songs, browse the charts, actually listen, and build local playlists
- Clicking Music now opens the new app instead of a list of outside sites

# f2ec738

- Added online, idle, do not disturb and invisible status, and profile banners
- Added notifications for DMs and pings, opt in from your profile

# d4d678c

- Chat error messages now say what actually went wrong instead of a generic failure, this is what made a stale account bug hard to track down

# c73152c

- Fixed genuine, correctly signed messages in private rooms and every DM always showing as unverified

# 34a2d12

- Fixed the close button on the room and profile popups sitting way off from the actual card
- Fixed a huge gap opening up between your messages and theirs in a wide chat window
- Room, DM and friend lists in the sidebar could go permanently blank if anything hiccuped loading them, now they only ever update once the new list is actually ready
- Gifs now show a star on hover to favorite them
- Fixed DMs failing to start for accounts that were signed in from a saved session created before DMs existed

# b7f44ba

- Akura Chat is a full rebuild now: a persistent sidebar with Friends, Direct Messages and Rooms, next to the actual conversation, instead of separate full page screens
- Added friends, send and accept requests, remove a friend, see who is pending
- Added real direct messages, end to end encrypted with an actual key exchange between the two people, not just a room password
- Added bios to profiles
- Type a colon and a word like fire to get emoji suggestions, click one or just send it and it turns into the real emoji
- Added a gif picker with a favorites tab next to the message box

# e3db3c4

- Changing your profile picture now updates it live everywhere it shows up, not just after a reload
- Chat got a real visual pass: glowing avatars, room icons, hover lift on room rows, and shadowed gradient message bubbles instead of flat plain ones

# 0675835

- Fixed the right click menu on your own rooms getting covered by the general Akura menu, rename and delete were there, just hidden underneath it

# 217e6ec

- The changelog now loads through Akura's own server instead of going straight to GitHub, so it still works on networks that block GitHub itself

# 26993b5

- Fixed images and gifs in chat sitting way off to one side instead of next to your avatar
- The empty chat screen now shows fresh AI generated example prompts instead of the same four every time
- If you own a room, you can open it again without retyping the password, and you can rename it, change its password, or delete it from a right click menu or the room settings button
- Nearly the entire games library was missing its thumbnail, found and fixed the real cause, most games should show a real picture now instead of a plain tile

# f244131

- The assistant now knows your actual local date and time, resolved from your IP, not just a server clock

# 10b1296

- The assistant now always knows the real current date, instead of leaning on its own training data or guessing
- Search and page results are stamped with when they were actually fetched, so recency is not a guess either
- Sharper image reading, attachments keep more detail before being sent, and it now reads exact text and counts instead of estimating
- It will say when part of an image is too small or blurry to be sure about instead of guessing

# 63fe716

- Fixed a real bypass: reaching Settings during the split second before load finished and hitting back to Akura skipped the password entirely
- The footer no longer flashes visible for a frame before the password gate is checked
- Chat has real toggle switches now instead of a checkbox, and more breathing room throughout
- New save account option when creating a chat account, skip the password next time on this device
- Chat now supports image and gif attachments, still end to end encrypted in password protected rooms
- Sent messages appear instantly instead of waiting on a round trip, then quietly sync in the background with no flash
- Added read receipts and profile pictures to chat
- New My rooms tab in chat, alongside Public rooms
- The assistant no longer pastes raw scraped page text back at you, it answers in its own words
- Image generation leads with the better model again, the other one is only a fallback now
- Image prompts are steered toward original art direction, less likely to get filtered
- Small speed tweaks to how fast the assistant starts responding, and a stronger model now leads for reading images

# 33dd55b

- Chat no longer says it is local only in the header and setup screen, it syncs across devices through Supabase now

# 7bf891e

- Akura Chat now actually syncs across devices, accounts, rooms and messages live in the cloud instead of only on this device
- Messages in a room now arrive live for everyone in it, no refresh needed
- Password protected rooms are still end to end encrypted, the server only ever sees the locked content

# 4b604ca

- New Akura Chat, a place to talk with other users, separate from the assistant
- Create an account with a username and password, everything is tied to a real cryptographic identity
- Chat in public rooms, or make a password protected room that is end to end encrypted, only people with the password can read it
- For now this only lives on this device, a shared version is coming later

# 80d712a

- Fixed generated images sometimes coming back as a solid black square for known characters, that was a content filter on the old model, switched to one that does not have that problem

# b6b8606

- At your request, the assistant can now change your Wisp relay server and AI model too, and can test the connection for you
- Clear all data and Reset Akura still have no tool and never will, those stay behind their own confirmation in Settings
- Fixed a case where a slow-resolving result, like a Wisp test, could finish after the reply was already done and silently fail to show up

# ab868a1

- The assistant can now open a website for you through the proxy just by asking
- It can also change settings for you: mode, theme, ad blocking, remote favicons, saving history, hiding the top bar, the animated background
- It will never change your Wisp relay server itself, that always has to be entered by you, it will just open Proxy settings so you can

# 3cc87ee

- Generated and found images no longer flash in half-loaded, the "Generating..." status now holds until the picture has actually finished loading, then hands off cleanly

# 1de2467

- Fixed image search sometimes showing fake broken links pointing at your own machine
- The assistant no longer explains that images will appear, it just answers

# bc16a6a

- Fixed the assistant sometimes not using its tools at all, one slow model could quietly kill the whole attempt, it now tries the others properly
- Llama 3.3 70B is currently slow and unreliable, it is no longer picked automatically, only if you choose it yourself in Settings
- Added optional reverse image search for identifying anime, manga and game characters, needs your own free saucenao.com key to turn on

# 0696442

- The assistant can now find real images and show them right in the chat
- It can also generate brand new images from a description
- Both show up as soon as they are ready, not just after the assistant finishes typing
- Generated images are saved so they are still there if you come back to that chat later

# 41e5e26

- The assistant can now actually search the web and read pages, it will no longer tell you it cannot browse
- It can look at images you attach, and can open parts of Akura for you when you ask
- A small router model picks which main model answers on Auto, instead of always trying the same order
- Real math rendering, write $x^2$ or $$\frac{a}{b}$$ and it renders properly
- Streaming feels lighter on slower devices, especially noticeable on Chromebooks
- Chat bubbles reworked to read more like a typical chat app
- Chats can be renamed from the sidebar
- The model name is no longer shown in the AI header
- New site-wide right click menu, proxied pages keep their own

# 2abed57

- Only the travelling light on the search bar glows now, instead of the whole field lighting up
- Tightened the lit arc so it reads as one light moving around the rim

# 18a1ab2

- The light circles the search bar at all times and brightens when you focus the field
- Performance mode keeps the rim but holds it still

# 0515e7e

- The search field is a pill with a light travelling around its rim
- Quick apps answer to the number keys, press 1 to 9, or hold Alt to see which is which
- Section headings carry a small accent tick
- New "Clear all data" in Settings, Data. It wipes local storage, cookies, databases, caches and
  the service worker for Akura and for every site opened through it. It confirms twice and cannot
  be undone
- Databases still held open when the wipe runs are finished on the next load, before anything can
  reopen them

# 0c6a701

- Removed the splash line under the wordmark

# ada3a28

- Fixed dropdowns being cut off when opened inside a settings panel
- Dropdowns flip above the button when there is no room below them
- Model names are never truncated, the menu grows to fit them instead

# 7718507

- Default theme is Akura lavender again, the way it was before
- The emerald palette lives on as its own theme, Verdant, so nothing was lost
- A slow accent haze drifts behind the starfield
- A hand drawn swash sits under the wordmarks
- Quick app icons sit on rounded plates that light up on hover
- Every panel catches light along its top edge
- The footer shows whether a proxy relay is actually connected
- Every dropdown is custom now, with keyboard control and no native select anywhere
- Site icons are on by default, fall back across providers, and drop to a lettered tile if a
  provider stalls instead of leaving an empty square

# 1ae584c

- Rebuilt the interface around a script wordmark, a centred search field and a Quick apps grid
- Home search goes straight to the built in browser
- New command palette on Ctrl+K across apps, sites, games and settings
- Settings is a full page now instead of a cramped modal
- Added Light, Dark and System modes
- Eight colour themes to pick from
- New games page with search, category filter, favourites and lazy loaded covers
- Quick apps are editable, and the starfield can be switched off on slower devices
- Browsing history and bookmarks, both stored only on this device
- The assistant falls back automatically when a model is busy or unreachable
- Pick a specific model in Settings, or leave it on Auto
- Answers stream in token by token instead of rebuilding the whole message each time
- Added a Stop button, Regenerate, and per message Copy
- Conversations are saved, so a refresh no longer wipes the chat, and you can keep several going
- Reasoning models get a collapsible thinking panel, and every reply shows animated dots while it
  waits
- Markdown is rendered by a built in parser that escapes HTML before it parses, closing a hole
  where model output was written straight into the page
- Formatting still works on locked down networks
- Failures now appear as an inline error instead of hanging on a typing indicator
- Ad blocking actually works now. The setting was read in a place it could never be read from, so
  the toggle had never done anything
- Each browser tab tracks its own retry state, so one tab's error no longer cancels another's check
- Reloading a proxied site no longer inherits a stale timer that hid the loading screen early
- Site icons are drawn locally by default, with no third party lookup on every card
- Removed two settings toggles that were stored but never actually used
