# Naloxone Game Optimization Guide

## Current Issues
- Total project size: ~259 MB (should be under 10-20 MB for web deployment)
- Individual background images are 40-50 MB each
- This will cause very slow loading times for users

## Image Optimization Strategy

### 1. Compress Background Images
**Target sizes for backgrounds:**
- scene_1.png: 48.3 MB → ~500 KB (99% reduction needed)
- jules body bg.png: 43.5 MB → ~400 KB
- grass test.png: 39.1 MB → ~300 KB
- All other backgrounds: aim for 200-500 KB each

### 2. Recommended Tools
- **Online**: TinyPNG, Squoosh.app, or Compressor.io
- **Software**: GIMP, Photoshop, or ImageOptim

### 3. Compression Settings
- **Format**: Use WebP or optimized PNG/JPEG
- **Quality**: 75-85% for backgrounds (they're often not the focus)
- **Resolution**: Check if 1920x1080 is needed - consider 1280x720 for some backgrounds
- **Color depth**: Reduce to 256 colors if possible for illustrations

### 4. Specific Recommendations
```
Current → Target Size:
scene_1.png: 48.3 MB → 500 KB
jules body bg.png: 43.5 MB → 400 KB  
grass test.png: 39.1 MB → 300 KB
nate check up bg.png: 18.4 MB → 200 KB
nate reuse bg.png: 17.1 MB → 200 KB
grass bg.png: 14.1 MB → 150 KB
Nate 2 bg.png: 13.6 MB → 150 KB
Nate 1 bg.png: 11.8 MB → 150 KB
```

### 5. Expected Results
- **Total project size**: 259 MB → 5-8 MB (97% reduction)
- **Loading time**: From 30+ seconds → 2-3 seconds on average internet
- **Better user experience**: Game starts immediately

## Code Optimization (Optional)

### 1. Split into Multiple Files
Consider separating into:
- index.html (structure)
- game.js (game logic)
- styles.css (styling)

### 2. Image Preloading
Add loading screen while images load:
```javascript
let imagesLoaded = 0;
const totalImages = Object.keys(gameImages).length;

function onImageLoad() {
    imagesLoaded++;
    updateLoadingScreen(imagesLoaded / totalImages);
    if (imagesLoaded === totalImages) {
        startGame();
    }
}
```

## Priority Actions
1. **CRITICAL**: Compress all background images (will solve 95% of the size issue)
2. **IMPORTANT**: Test game still looks good after compression
3. **NICE TO HAVE**: Add loading screen and split code files
