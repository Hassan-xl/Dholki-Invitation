# Abdul Wassay & Warisha · Dholki Invitation

A static website. No build step, no dependencies. Hosted the same way as the other invitations (GitHub + Vercel).

| File | What it is |
|---|---|
| `index.html` | The whole invitation: bunting, umbrellas, marigolds, the dancers, the curtains, the mehndi hand, the rickshaw |
| `assets/dholki-loop.mp3` | A seamless 94-second loop cut from your dhol & shehnai track (1.1 MB instead of 7.4 MB) |
| `assets/d-*.webp`, `assets/d-*.png` | The paper dancers cut out of your images (PNG is the fallback for older phones) |
| `assets/fonts/` | The typefaces, including Urdu Nastaliq, stored with the site so they load fast |
| `dholki.ics` | Calendar file iPhones open from the "Add to Calendar" button |
| `vercel.json` | Tells Vercel to send `dholki.ics` as a calendar file |
| `og.jpg` | The preview picture WhatsApp shows when the link is shared |
| `favicon.png`, `apple-touch-icon.png` | Browser tab and home-screen icons |

## Put it online (GitHub + Vercel)

1. Create a new GitHub repository and upload **everything in this folder** (keep the `assets` folder as it is).
2. In Vercel choose **Add New → Project** and import that repository.
3. Set **Framework Preset** to **Other**, leave the build command empty and the output directory as the root.
4. Press **Deploy**.

## Before sending to guests

**1. Your live address.** The preview tags in `index.html` point to `https://dholki-wassay-warisha.vercel.app`.
If Vercel gives you a different address, search `index.html` for `dholki-wassay-warisha.vercel.app` and replace all of them.

**2. The map pin.** "Open in Maps" searches for *Askari 5 Sector F, Malir Cantonment, Karachi*. For an exact pin,
open the building in Google Maps → **Share → Copy link**, and paste it as the value of `MAP_URL` in `index.html`.

## Personal links for each guest

- `https://your-address/?to=Ahmed Family`
- `https://your-address/#Ahmed-Family`

The cover then says "Specially for Ahmed Family".

## How the experience flows

1. **Tap the dhol.** The music starts, confetti flies, and the paper dancers jump in and dance to the beat.
2. **Pull the tassel.** The phulkari curtains open on the invitation from Muhammad Sulieman & Mansha Sulieman.
3. **Mehndi lagao!** Guests draw on a paper hand with a finger. A henna design appears (with the couple's initials
   hidden in the palm, like the tradition of hiding the groom's name), and then the date tiles and a live countdown light up.
4. **Tashreef laiye.** The address in a truck-art frame, with a rickshaw that drives in and honks when tapped,
   plus Open in Maps and Add to Calendar.
5. **The dance floor.** Everyone dances. Tapping a dancer makes them spin and cheer.

The little dholak at the bottom always tells guests what to do next, and its spoon taps along with the beat.
The yellow arrow moves on (and does the step for them if they skip it). Swiping also turns the pages.

## About the music and the movement

- The whole song is analysed once and its real beats are written into the page, so the bunting, umbrellas,
  marigold strings, lights and dancers all move on the actual dhol beats, not on a guessed tempo.
- The loop is decoded once and played gaplessly, so there is no hiccup when it repeats.
- The music is downloaded while the guest looks at the loading flower, so it starts instantly on the first tap.
- On iPhones running iOS 16.4 or later the music plays even when the phone is on silent, because the guest
  chose to start it. The round yellow button at the top right pauses it.
- The dancers bob gently even before the music starts or when it is paused, so the page always feels alive.
- On slower phones the page draws less confetti automatically. It also respects the "Reduce motion" setting.
- All dates and times live in the `CFG` block at the top of the script (UTC: 7:00 pm in Pakistan is 14:00 UTC).
  If the time changes, also update `dholki.ics`.
