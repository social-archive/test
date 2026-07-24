# 스킬 오버드라이브 이미지 에셋

## 사용 에셋

| 파일 | 용도 |
|---|---|
| `arena-cosmic-v1.png` | 게임 전투 화면의 16:9 우주 유적 배경 |
| `arena-infinite-tile-v2.png` | 전 방향 무한 스크롤에 사용하는 정사각형 우주 전장 타일 |
| `nova-player-v1.png` | 투명 배경이 적용된 주인공 노바 |
| `nova-chroma-v1.png` | 배경 제거 전 원본 캐릭터 이미지 |
| `rift-hound-v1.png` | 투명 배경이 적용된 일반 적 리프트 하운드 |
| `rift-hound-chroma-v1.png` | 배경 제거 전 리프트 하운드 원본 |
| `astral-devourer-v1.png` | 투명 배경이 적용된 보스 아스트랄 디바우러 |
| `astral-devourer-chroma-v1.png` | 배경 제거 전 보스 원본 |
| `bolt-player-v1.png` | 투명 배경이 적용된 플레이 캐릭터 볼트 |
| `bolt-chroma-v1.png` | 배경 제거 전 볼트 원본 |
| `eclipse-player-v1.png` | 투명 배경이 적용된 플레이 캐릭터 이클립스 |
| `eclipse-chroma-v1.png` | 배경 제거 전 이클립스 원본 |
| `rift-spear-v1.png` | 투명 배경이 적용된 돌진 적 리프트 스피어 |
| `rift-spear-chroma-v1.png` | 배경 제거 전 리프트 스피어 원본 |
| `xp-shard-v1.png` | 투명 배경이 적용된 경험치 결정 |
| `xp-shard-chroma-v1.png` | 배경 제거 전 경험치 결정 원본 |
| `skill-card-atlas-v1.png` | 기본 스킬 6종의 3×2 카드 일러스트 아틀라스 |
| `utility-card-atlas-v1.png` | 유틸리티 모듈 6종의 3×2 카드 일러스트 아틀라스 |
| `ultimate-cut-in-v1.png` | 궁극 진화 선택 화면의 16:9 컷인 |

## 플레이 전용 경량 에셋

`optimized/` 폴더에는 Canvas에서 실제로 그리는 크기에 맞춘 경량 PNG가 들어 있다. 원본은 선택 화면과 추후 재가공을 위해 그대로 보존한다.

| 파일 | 렌더 크기 |
|---|---:|
| `optimized/arena-infinite-tile-v2.png` | 768×768 |
| `optimized/arena-cosmic-v1.png` | 1280×720 |
| `optimized/nova-player-v1.png` | 256×256 |
| `optimized/nova-title-v1.png` | 512×512 |
| `optimized/bolt-player-v1.png` | 256×256 |
| `optimized/eclipse-player-v1.png` | 256×256 |
| `optimized/rift-hound-v1.png` | 192×192 |
| `optimized/rift-spear-v1.png` | 192×192 |
| `optimized/xp-shard-v1.png` | 64×64 |
| `optimized/astral-devourer-v1.png` | 384×384 |
| `optimized/skill-card-atlas-v1.png` | 768×512 |
| `optimized/utility-card-atlas-v1.png` | 768×512 |
| `optimized/ultimate-cut-in-v1.png` | 960×540 |

## 배경 적용 지침

- 게임 화면 전체를 채우도록 `cover` 방식으로 배치한다.
- 배경 위에 약한 남색 오버레이를 적용해 적과 투사체의 가독성을 유지한다.
- 중앙 영역은 캐릭터와 적이 이동하는 공간으로 사용한다.
- 수정과 우주 균열이 있는 외곽 영역은 위험 지역 또는 보스 등장 연출에 활용한다.

## 캐릭터 적용 지침

- 실제 플레이에서는 `nova-player-v1.png`를 사용한다.
- 캐릭터의 전체 실루엣이 보이도록 비율을 유지한다.
- 피격 판정은 이미지 전체가 아니라 몸통 중심의 작은 원으로 설정한다.
- 레벨 상승 시 캐릭터 주변에 별도의 오라와 스킬 효과를 겹쳐 표시한다.
- 카드 선택 및 결과 화면에서는 같은 이미지를 크게 확대해 대표 일러스트로 활용한다.

## 생성 방식

두 이미지는 기본 내장 이미지 생성 도구로 제작했다. 캐릭터는 단색 크로마키 배경으로 생성한 뒤 로컬 배경 제거 도구를 사용해 투명 PNG로 변환했다.

리프트 하운드와 아스트랄 디바우러도 같은 내장 이미지 생성 도구와 크로마키 제거 방식으로 추가 제작했다.

볼트, 이클립스, 리프트 스피어, 경험치 결정, 스킬 카드 아틀라스와 궁극 진화 컷인도 기본 내장 이미지 생성 도구로 제작했다. 투명 에셋 4종은 단색 크로마키 원본에서 배경을 제거한 뒤 알파 채널과 가장자리를 검수했다.

## 최종 생성 프롬프트

### 우주 전투 배경

```text
Use case: stylized-concept
Asset type: game combat arena background for a browser roguelike survival game
Primary request: a premium high-detail top-down cosmic arena where neon magic skills and hundreds of enemies will be layered during gameplay
Scene/backdrop: vast circular astral ruin floating in deep space, fractured obsidian floor, luminous cyan and violet energy rivers, crystalline ruins and distant nebula clouds around the outer edges
Subject: environment only, no characters, no enemies
Style/medium: polished 2D game key art, hand-painted sci-fantasy, high-end action roguelike visual quality, crisp and richly textured
Composition/framing: true top-down gameplay view, wide 16:9 landscape; keep the central 55 percent comparatively dark, open, and low-detail for gameplay readability; concentrate spectacular crystals, cosmic storms, glowing runes, particles, and depth along the outer edges; no horizon line
Lighting/mood: dramatic ultraviolet, electric cyan, hot magenta and subtle gold rim light; energetic and magical but readable
Color palette: deep navy and near-black base with saturated cyan, violet, magenta, and small gold accents
Constraints: seamless-feeling playable arena composition; no UI, no text, no logo, no watermark, no characters, no enemies; do not place a bright focal object in the exact center; avoid simple geometric placeholder shapes
```

### 무한 스크롤 우주 전장 타일

```text
Use case: stylized-concept
Asset type: seamless tileable game environment texture for an infinite-scrolling top-down browser action roguelike
Primary request: a premium high-detail cosmic battlefield floor tile that can repeat in every direction while neon combat effects and hundreds of enemies remain readable
Scene/backdrop: ancient fractured obsidian astral platform floating in deep space, subtle cyan and violet energy veins, embedded crystal dust, faint circular rune fragments and distant nebula depth
Subject: environment only, no characters, enemies, pickups, weapons, UI, or focal landmark
Style/medium: polished 2D hand-painted cartoon sci-fantasy game art, rich surface detail, high-end action roguelike quality
Composition/framing: exact top-down orthographic square tile; evenly distributed detail; comparatively dark low-contrast center and overall floor; all four edges must connect seamlessly with no border, frame, seam, hard lighting cutoff, unique central object, or obvious repeating landmark
Lighting/mood: deep navy and near-black base with subtle ultraviolet ambient light, controlled cyan and magenta glints, tiny restrained gold sparks; dramatic but gameplay-readable
Color palette: deep navy, obsidian, violet, electric cyan, sparse hot magenta and gold
Constraints: seamless tileable texture in both X and Y directions; matching color, cracks, veins, and texture density across opposite edges; no perspective horizon; no directional shadows; no text, logo, watermark, UI, characters, creatures, pickups, large central portal, or isolated centerpiece
Avoid: visible square border, bright center, large simple geometric shapes, repeated icon pattern, empty flat background, photorealism
```

### 주인공 노바

```text
Use case: stylized-concept
Asset type: playable game character asset for a top-down browser action roguelike
Primary request: Nova, an original cosmic skill-weaver hero whose stacked magic evolves into spectacular neon attacks
Subject: one single full-body young adult hero, androgynous appearance, short swept-back silver-white hair with clean chunky shapes, determined expression, sleek deep-navy combat coat and fitted armor, luminous cyan and violet crystal plates, small gold details, two solid crystalline energy blades orbiting close behind the shoulders; no other characters
Style/medium: premium polished 2D game character render, crisp hand-painted cartoon sci-fantasy, strong readable silhouette, high-end action game asset, hard clean edges
Composition/framing: full body visible from head to boots, centered, top-down three-quarter gameplay camera angle, dynamic ready stance, generous empty padding on all sides
Lighting/mood: vivid cyan and violet rim lighting on the character, energetic heroic mood, keep internal forms readable at small size
Color palette: deep navy, silver-white, electric cyan, violet, small gold accents; absolutely no green in the subject
Scene/backdrop: perfectly flat solid #00ff00 chroma-key background for background removal
Constraints: the background must be one uniform #00ff00 color with no shadows, gradients, texture, reflections, floor plane, glow spill, or lighting variation; keep all character parts fully separated from the background with crisp edges; no cast shadow, no contact shadow, no reflection; one character only; no UI, no text, no logo, no watermark; do not use #00ff00 anywhere in the character
Avoid: photorealism, thin wispy hair, smoke, translucent cape, semi-transparent aura, cropped feet, complex background, simple geometric placeholder character
```

### 일반 적 리프트 하운드

```text
Use case: stylized-concept
Asset type: playable enemy sprite for a top-down browser action roguelike
Primary request: one original astral void creature called a Rift Hound, designed to swarm the hero in large numbers
Subject: single compact quadruped cosmic beast, angular obsidian armor shell, bright hot-magenta core in the chest, cyan edge accents, sharp crystalline claws, aggressive forward-leaning running pose, strong compact silhouette, no other creatures
Style/medium: premium polished 2D game sprite render, crisp hand-painted cartoon sci-fantasy, hard clean edges, readable at 48 to 80 pixels
Composition/framing: full creature visible, centered, top-down three-quarter gameplay camera angle, generous padding on all sides
Lighting/mood: magenta internal glow with cyan rim light, dangerous and fast
Color palette: obsidian black, deep violet, hot magenta, electric cyan; absolutely no green
Scene/backdrop: perfectly flat solid #00ff00 chroma-key background for background removal
Constraints: uniform #00ff00 background with no shadows, gradient, floor, texture, reflection, glow spill, or lighting variation; no cast shadow; single opaque creature only; crisp separated silhouette; no smoke or transparent particles; no UI, no text, no logo, no watermark; do not use #00ff00 in the creature
Avoid: simple circles, abstract geometric placeholders, photorealism, multiple creatures, cropped limbs
```

### 보스 아스트랄 디바우러

```text
Use case: stylized-concept
Asset type: boss sprite for a top-down browser action roguelike
Primary request: one original cosmic raid boss called the Astral Devourer, visually imposing and much larger than the normal enemies
Subject: single colossal floating armored cosmic entity, crown-like obsidian horns, broad symmetrical silhouette, six heavy crystalline arms folded around a blazing violet star core, cyan cracks and gold ancient armor trims, fierce mask-like face, no other creatures
Style/medium: premium polished 2D game boss render, crisp hand-painted cartoon sci-fantasy, spectacular high-end action game asset, hard clean edges, readable silhouette
Composition/framing: full boss visible and centered, top-down three-quarter gameplay camera angle, symmetrical hovering pose, generous padding on all sides
Lighting/mood: overwhelming ultraviolet core glow, cyan rim lighting, small gold highlights, apocalyptic and majestic
Color palette: obsidian black, deep navy, violet, magenta, electric cyan, antique gold; absolutely no green
Scene/backdrop: perfectly flat solid #00ff00 chroma-key background for background removal
Constraints: uniform #00ff00 background with no shadows, gradient, floor, texture, reflection, glow spill, or lighting variation; no cast shadow; single opaque boss only; crisp separated silhouette; no smoke or transparent particles; no UI, no text, no logo, no watermark; do not use #00ff00 in the boss
Avoid: simple circles, abstract geometric placeholders, photorealism, multiple characters, cropped limbs
```

### 추가 플레이 캐릭터 볼트

```text
Premium polished 2D cartoon sci-fantasy playable character asset: one full-body young adult male lightning runner named Bolt, top-down three-quarter gameplay view, dynamic sprint-ready pose, swept electric-blue hair, deep navy and cobalt combat suit, luminous yellow lightning circuits, cyan crystal greaves, compact shoulder armor, confident expression, strong readable silhouette at small size. Centered with generous padding on a perfectly uniform flat #00ff00 chroma-key background. No green in the character, no shadow, floor, text, logo, watermark, smoke, transparency, crop, extra characters, or placeholder geometry.
```

### 추가 플레이 캐릭터 이클립스

```text
Premium polished 2D cartoon sci-fantasy playable character asset: one full-body young adult female void mage named Eclipse, top-down three-quarter gameplay view, elegant battle-ready pose, black and violet layered armor dress, hot-magenta energy seams, antique-gold trim, crescent void blades and a compact dark orb, strong readable silhouette at small size. Centered with generous padding on a perfectly uniform flat #00ff00 chroma-key background. No green in the character, no shadow, floor, text, logo, watermark, smoke, transparency, crop, extra characters, or placeholder geometry.
```

### 돌진 적 리프트 스피어

```text
Premium polished 2D cartoon sci-fantasy enemy sprite: one fast six-legged astral spear predator called Rift Spear, crimson-black angular armor, blazing orange core, long forward horn, cyan blade tips, aggressive low charging pose, top-down three-quarter gameplay view, crisp readable silhouette at 48–90 pixels. Centered with generous padding on a perfectly uniform flat #00ff00 chroma-key background. No green in the creature, no shadow, floor, text, logo, watermark, smoke, crop, multiple creatures, or placeholder geometry.
```

### 경험치 결정

```text
Premium polished 2D game pickup asset: one single faceted cosmic experience crystal shard, elongated diamond silhouette, luminous cyan upper facets, violet lower facets and small gold crown detail, strong white internal gleam, crisp readable outline at 16–28 pixels. Centered with generous padding on a perfectly uniform flat #00ff00 chroma-key background. No green in the pickup, no shadow, floor, text, logo, watermark, extra objects, crop, or placeholder geometry.
```

### 스킬 카드 아틀라스

```text
Premium polished 2D sci-fantasy skill icon atlas, exact 3 columns by 2 rows on six equal dark-navy square tiles with clear gutters. Top row: cyan prism blades, violet chain lightning, orange comet shower. Bottom row: magenta void pulse, mint star drones, pink cosmic bloom orb. Each tile has one centered high-detail icon, consistent camera and lighting, vivid neon glow, crisp edges, readable at card size. No text, letters, numbers, logos, watermark, characters, or ambiguous extra panels.
```

### 유틸리티 카드 아틀라스

```text
Use case: stylized-concept
Asset type: premium 2D game UI icon atlas for utility upgrade cards in a neon cosmic browser action roguelike
Primary request: exactly six distinct utility upgrade illustrations arranged as a precise 3-column by 2-row atlas
Subject and order: top-left a cyan triple-projectile crystal magazine with three outward energy bolts; top-center a violet chrono accelerator turbine surrounded by fast clock arcs for attack speed; top-right gold-and-cyan winged boots with a forward motion trail for movement speed; bottom-left a mint gravity collector core pulling several tiny blue experience crystals inward; bottom-center a hot-magenta critical-focus prism targeting a bright weak point with a clean crosshair; bottom-right a blue-and-gold aegis shield wrapped around a glowing heart-shaped core for defense and health
Style/medium: polished hand-painted cartoon sci-fantasy game icons, crisp hard edges, premium collectible card art, consistent with vivid neon cosmic skill icons
Composition/framing: exact 3x2 grid of six equal square dark-navy tiles, clear uniform gutters, one centered large icon per tile, generous internal padding, no object crossing tile boundaries
Lighting/mood: intense cyan, violet, magenta, mint and gold magical glow, bright focal highlights, dark readable backgrounds
Constraints: every requested concept appears exactly once and in the specified position; six tiles only; no text, letters, numbers, labels, characters, hands, logos, watermark, extra panels, or merged icons; each icon must remain clearly readable when cropped to a small card thumbnail
Avoid: emoji style, flat placeholder shapes, ambiguous repeated symbols, photorealism, uneven tile sizes, decorative border text
```

### 궁극 진화 컷인

```text
Wide 16:9 premium 2D cartoon sci-fantasy ultimate-evolution cut-in, split cosmic battle energy composition: left side a cyan-and-gold crystalline blade and lightning storm; right side a hot-magenta black hole and supernova bloom; deep navy center with converging energy, spectacular particles and high contrast while keeping the center readable for overlay UI. No characters, text, letters, numbers, logo, watermark, frame, or placeholder geometry.
```
