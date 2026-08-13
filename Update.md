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
