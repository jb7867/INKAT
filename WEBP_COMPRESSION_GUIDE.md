# Squoosh Image Compression Guide for Naloxone Game

## Current Project Size: 259MB → Target: 5-8MB (97% reduction needed)

## PNG vs WebP Decision Matrix:
- **WebP**: All backgrounds, character images (97%+ reduction)  
- **PNG**: Keep only if transparency is critical AND file <500KB
- **Squoosh Control**: Quality slider (0-100), Effort slider (0-6)

### Critical Large Files (Priority 1 - Compress First)
These files are causing the biggest size issues:

1. **scene_1.png** (48.3 MB) → **400-500 KB WebP** (99% reduction)
   - **Decision**: MUST convert to WebP (no choice at this size)
   - **Squoosh Settings**: WebP Quality 55-65, Effort 6
   - **Target Size**: 400-500 KB maximum

2. **main bg.png** (30+ MB estimated) → **300-400 KB WebP** (99% reduction)
   - **Decision**: MUST convert to WebP (background image)
   - **Squoosh Settings**: WebP Quality 50-60, Effort 6
   - **Target Size**: 300-400 KB maximum

3. **grass bg.png** (20+ MB estimated) → **250-350 KB WebP** (98% reduction)
   - **Decision**: MUST convert to WebP (texture can handle heavy compression)
   - **Squoosh Settings**: WebP Quality 45-55, Effort 6
   - **Target Size**: 250-350 KB maximum

### Character Backgrounds (Priority 2)
4. **jules body bg.png** (15+ MB estimated) → **300-400 KB WebP** (97% reduction)
   - **Decision**: Convert to WebP (character detail important but compressible)
   - **Squoosh Settings**: WebP Quality 60-70, Effort 6
   - **Target Size**: 300-400 KB maximum

5. **Jules thigh bg.png** (15+ MB estimated) → **300-400 KB WebP** (97% reduction)
   - **Decision**: Convert to WebP 
   - **Squoosh Settings**: WebP Quality 60-70, Effort 6
   - **Target Size**: 300-400 KB maximum

6. **Jules arm bg.png** (15+ MB estimated) → **300-400 KB WebP** (97% reduction)
   - **Decision**: Convert to WebP
   - **Squoosh Settings**: WebP Quality 60-70, Effort 6
   - **Target Size**: 300-400 KB maximum

7. **Nate 1 bg.png** (12+ MB estimated) → **250-350 KB WebP** (97% reduction)
   - **Decision**: Convert to WebP
   - **Squoosh Settings**: WebP Quality 60-70, Effort 6
   - **Target Size**: 250-350 KB maximum

8. **Nate 2 bg.png** (12+ MB estimated) → **250-350 KB WebP** (97% reduction)
   - **Decision**: Convert to WebP
   - **Squoosh Settings**: WebP Quality 60-70, Effort 6
   - **Target Size**: 250-350 KB maximum

9. **nate check up bg.png** (10+ MB estimated) → **200-300 KB WebP** (97% reduction)
   - **Decision**: Convert to WebP
   - **Squoosh Settings**: WebP Quality 60-70, Effort 6
   - **Target Size**: 200-300 KB maximum

10. **nate reuse bg.png** (10+ MB estimated) → **200-300 KB WebP** (97% reduction)
    - **Decision**: Convert to WebP
    - **Squoosh Settings**: WebP Quality 60-70, Effort 6
    - **Target Size**: 200-300 KB maximum

### UI and Scene Images (Priority 3)
11. **intro bg.png** (8+ MB estimated) → **150-250 KB WebP** (97% reduction)
    - **Decision**: Convert to WebP (background image)
    - **Squoosh Settings**: WebP Quality 55-65, Effort 6
    - **Target Size**: 150-250 KB maximum

12. **scenario bg.png** (6+ MB estimated) → **120-200 KB WebP** (97% reduction)
    - **Decision**: Convert to WebP (background image)
    - **Squoosh Settings**: WebP Quality 55-65, Effort 6
    - **Target Size**: 120-200 KB maximum

13. **main bg2.png** (5+ MB estimated) → **120-200 KB WebP** (97% reduction)
    - **Decision**: Convert to WebP (background image)
    - **Squoosh Settings**: WebP Quality 55-65, Effort 6
    - **Target Size**: 120-200 KB maximum

### Equipment Images (Priority 4 - Higher Quality Needed)
14. **naloxone 1.png** (3+ MB estimated) → **80-120 KB WebP** (96% reduction)
    - **Decision**: Convert to WebP (important but compressible)
    - **Squoosh Settings**: WebP Quality 70-80, Effort 6
    - **Target Size**: 80-120 KB maximum
    - **Quality Check**: Must remain readable for gameplay

15. **naloxone 2.png** (3+ MB estimated) → **80-120 KB WebP** (96% reduction)
    - **Decision**: Convert to WebP (important but compressible)
    - **Squoosh Settings**: WebP Quality 70-80, Effort 6
    - **Target Size**: 80-120 KB maximum
    - **Quality Check**: Must remain readable for gameplay

16. **case 1.png** (2+ MB estimated) → **60-100 KB WebP** (96% reduction)
    - **Decision**: Convert to WebP (game object needs clarity)
    - **Squoosh Settings**: WebP Quality 70-80, Effort 6
    - **Target Size**: 60-100 KB maximum

17. **case 2.png** (2+ MB estimated) → **60-100 KB WebP** (96% reduction)
    - **Decision**: Convert to WebP (game object needs clarity)
    - **Squoosh Settings**: WebP Quality 70-80, Effort 6
    - **Target Size**: 60-100 KB maximum

### Small Equipment Images (Priority 5 - Quality Critical)
18. **needle 1.png** (1+ MB estimated) → **Option A: 30-50 KB WebP OR Option B: 200-300 KB PNG**
    - **Decision**: TRY WebP first (WebP Quality 75-85, Effort 6)
    - **Fallback**: Keep PNG if WebP loses critical detail
    - **Target Size**: 30-50 KB WebP OR 200-300 KB PNG
    - **Quality Check**: CRITICAL - must be sharp for gameplay

19. **needle 2.png** (1+ MB estimated) → **Option A: 30-50 KB WebP OR Option B: 200-300 KB PNG**
    - **Decision**: TRY WebP first (WebP Quality 75-85, Effort 6)
    - **Fallback**: Keep PNG if WebP loses critical detail
    - **Target Size**: 30-50 KB WebP OR 200-300 KB PNG

20. **needle 3.png** (1+ MB estimated) → **Option A: 30-50 KB WebP OR Option B: 200-300 KB PNG**
    - **Decision**: TRY WebP first (WebP Quality 75-85, Effort 6)
    - **Fallback**: Keep PNG if WebP loses critical detail
    - **Target Size**: 30-50 KB WebP OR 200-300 KB PNG

21. **sachet 1.png** (1+ MB estimated) → **25-40 KB WebP** (96% reduction)
    - **Decision**: Convert to WebP (less detail-critical than needles)
    - **Squoosh Settings**: WebP Quality 75-85, Effort 6
    - **Target Size**: 25-40 KB maximum

22. **sachet 2.png** (1+ MB estimated) → **25-40 KB WebP** (96% reduction)
    - **Decision**: Convert to WebP (less detail-critical than needles)
    - **Squoosh Settings**: WebP Quality 75-85, Effort 6
    - **Target Size**: 25-40 KB maximum

23. **tip 1.png** (500 KB estimated) → **20-35 KB WebP** (94% reduction)
    - **Decision**: Convert to WebP (very small object)
    - **Squoosh Settings**: WebP Quality 80-90, Effort 6
    - **Target Size**: 20-35 KB maximum

### Logo/Branding (Priority 6 - Text Readability Critical)
24. **Azaredo Training Co..png** (2+ MB estimated) → **Option A: 40-60 KB WebP OR Option B: 300-500 KB PNG**
    - **Decision**: TRY WebP first (WebP Quality 80-90, Effort 6)
    - **Fallback**: Keep PNG if text becomes unreadable
    - **Target Size**: 40-60 KB WebP OR 300-500 KB PNG
    - **Quality Check**: CRITICAL - text must be perfectly readable

## Squoosh.app Step-by-Step Process:

### How to Use Squoosh:
1. **Open**: Go to https://squoosh.app
2. **Upload**: Drag and drop your PNG file
3. **Choose Format**: Select "WebP" in the right panel
4. **Adjust Quality**: Use the slider (see settings below)
5. **Adjust Effort**: Set to 6 (maximum compression)
6. **Preview**: Check the before/after comparison
7. **Download**: Click download when satisfied

### Squoosh Settings by Category:

#### **Backgrounds & Large Images** (scene_1, main bg, grass bg, character bgs):
- **WebP Quality**: 50-70
- **Effort**: 6 (maximum)
- **Goal**: Sacrifice some quality for massive size reduction
- **Target**: 200-500 KB per file

#### **Equipment & UI** (naloxone, cases):
- **WebP Quality**: 70-80
- **Effort**: 6
- **Goal**: Balance size reduction with readability
- **Target**: 60-120 KB per file

#### **Small Critical Objects** (needles, logo):
- **WebP Quality**: 75-85 (try first)
- **Effort**: 6
- **Goal**: Maximum quality retention
- **Target**: 30-60 KB per file
- **Fallback**: If WebP looks bad, try PNG compression instead

#### **PNG Compression Alternative** (for critical small images):
- **Format**: OptiPNG or PNG
- **Quality**: Maximum (no quality loss)
- **Target**: 200-500 KB per file
- **Use When**: WebP makes text/details unreadable

## Quality Check Guidelines:

### ✅ ACCEPTABLE compression artifacts:
- Slight softness in background textures
- Minor color banding in gradients
- Reduced sharpness in non-critical areas

### ❌ UNACCEPTABLE compression artifacts:
- Unreadable text (logo, UI elements)
- Needle tips that look blurry (gameplay critical)
- Severe blockiness in character faces
- Color distortion that changes game meaning

## File Size Targets Summary:
- **Total Project**: 5-8 MB (from 259 MB)
- **Largest Files** (scene_1, main bg): 300-500 KB each
- **Character Backgrounds**: 200-400 KB each  
- **Equipment Images**: 60-120 KB each
- **Small Objects**: 20-60 KB each
- **Emergency PNG Fallbacks**: 200-500 KB each (only if WebP fails quality check)

## Expected Results:
- **Before**: 259 MB total
- **After**: ~5.5-7 MB total (97%+ reduction)
- **Web Load Time**: From 30+ seconds → 2-3 seconds on average connection
- **Quality**: Backgrounds slightly softer, UI/equipment still sharp

## Files That May Stay PNG (if WebP quality is poor):
- **needle 1.png, needle 2.png, needle 3.png** (if tip detail is lost)
- **Azaredo Training Co..png** (if text becomes unreadable)
- **Any file where gameplay suffers from WebP artifacts**

## Compression Order (Start Here):
1. **scene_1.png** → Biggest impact (48MB → 400KB)
2. **main bg.png** → Major impact (30MB → 350KB)  
3. **grass bg.png** → Major impact (20MB → 300KB)
4. **Jules body bg.png** → High impact (15MB → 350KB)
5. **Continue with character backgrounds** (Nate files)
6. **Then equipment** (naloxone, cases)
7. **Small objects last** (needles, sachets)

## File Extension Updates Needed After Compression:
After compressing to WebP, update `index.html` file paths from:
```javascript
// OLD:
'Assets/scene_1.png'
'Assets/main bg.png'

// NEW:  
'Assets/scene_1.webp'
'Assets/main bg.webp'
```

I'll help you update all the file paths once compression is complete!
