# 🎵 Audio Player Integration Guide

## What Was Uploaded

✅ **audio-player.html** - Standalone audio player (live at `/audio-player.html`)  
✅ Full Cloudflare R2 integration ready  
✅ Playlist support (Mixes, Productions, Sessions)  

---

## 🚀 NEXT STEPS

### Step 1: Create Cloudflare R2 Bucket (2 minutes)

```
1. Go to https://dash.cloudflare.com
2. Left sidebar → "R2 Object Storage"
3. Click "Create Bucket"
4. Name: derrickfiles-audio
5. Create bucket
```

### Step 2: Get Public Bucket URL

In the R2 dashboard:
- Click your bucket
- Find "Public URL" section
- Copy URL like: `https://derrickfiles-audio.XXXXX.r2.dev`

### Step 3: Configure Player

1. Visit: `https://derrickfiles.com/audio-player.html`
2. Paste your bucket URL in the setup form
3. Upload MP3 files to:
   - `/mixes/` folder
   - `/productions/` folder
   - `/sessions/` folder

### Step 4: Test It!

1. Configure bucket URL
2. Select a track from any playlist
3. Click play
4. Enjoy streaming! 🎧

---

## 📁 Upload MP3 File Structure

```
Your R2 Bucket
├── mixes/
│   ├── summer-techno.mp3
│   ├── deep-house-vibes.mp3
│   └── club-bangers.mp3
├── productions/
│   ├── original-track-1.mp3
│   ├── remix-edit.mp3
│   └── unreleased-demo.mp3
└── sessions/
    ├── studio-session-1.mp3
    ├── live-jam.mp3
    └── beat-production.mp3
```

---

## 🔗 Add Audio Player to Main Site

If you want to add the player to your main index.html, add this section:

```html
<!-- Add this AFTER the productions section, BEFORE the hr divider -->
<div class="hr"></div>

<!-- ══ AUDIO STREAMING SECTION ══ -->
<section id="audio-streaming" class="sec">
  <span class="sec-label">Premium Audio Library</span>
  <h2 class="sec-title">AUDIO <span style="color:var(--gold);">STREAMING</span></h2>
  
  <div style="background:var(--card);border:1px solid var(--border2);border-radius:8px;padding:32px;">
    <iframe 
      src="/audio-player.html" 
      style="width:100%;height:700px;border:none;border-radius:8px;background:var(--dark);"
      title="Audio Player">
    </iframe>
  </div>
</section>
```

---

## 🎛️ Player Features

✅ Play/Pause/Next/Previous controls  
✅ Volume control slider  
✅ Progress bar with seek functionality  
✅ Three playlists (Mixes, Productions, Sessions)  
✅ Track duration display  
✅ Now playing info  
✅ Visual feedback (pulsing cover art)  
✅ Responsive design (mobile-friendly)  
✅ Stores bucket URL in localStorage  
✅ Direct MP3 streaming from Cloudflare R2  

---

## ⚠️ Important Notes

1. **Make bucket PUBLIC** - Set R2 bucket to public read access
2. **MP3 Format** - Use standard MP3 files (no DRM)
3. **CORS Headers** - Cloudflare R2 handles this automatically
4. **Browser Support** - Works on all modern browsers

---

## 🧪 Testing Checklist

- [ ] Created R2 bucket
- [ ] Set bucket to PUBLIC
- [ ] Got public bucket URL
- [ ] Uploaded test MP3 files
- [ ] Configured player with bucket URL
- [ ] Clicked "Connect Bucket"
- [ ] Selected and played a track
- [ ] Tested play/pause
- [ ] Tested next/previous
- [ ] Tested volume slider
- [ ] Tested progress seek

---

## 📞 Support

If the player doesn't load tracks:
1. Check bucket is set to **PUBLIC**
2. Verify URL format: `https://bucket-name.XXXXX.r2.dev`
3. Confirm MP3 files are in correct folders
4. Check browser console for errors (F12)

---

**Repository:** https://github.com/djderrickfiles/derrickfiles-main  
**Player File:** `/audio-player.html`  
**Live URL:** `https://derrickfiles.com/audio-player.html`
