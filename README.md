# Infinite Poster Generator

A creative coding web application that generates endless mid-century modern graphic design posters inspired by the golden age of graphic design (1950s-1990s).

## Overview

This application creates continuously evolving abstract posters that resemble the work of legendary designers like Paul Rand, Josef Müller-Brockmann, Reid Miles, and the Swiss Modernist movement. Forms appear slowly as if hand-drawn, persist as part of the composition, and eventually fade away to make room for new elements.

## Features

- **Intelligent Composition Engine**: Forms are placed using grid-based design principles with visual weight balancing to avoid random "slop"
- **Stroke-by-Stroke Animation**: Elements appear as if being drawn in real-time using various media (pencil, watercolor, marker, acrylic)
- **Style DSL**: JSON-based style definition system for creating and transitioning between different design eras
- **User Controls**:
  - Pause/Resume generation
  - Adjust speed (Slow, Normal, Fast, Very Fast)
  - Skip to next style
  - Export current poster as PNG
- **Responsive**: Adapts to window size while maintaining design integrity
- **No Server Required**: Runs as a single HTML file

## Usage

### Running Locally

Simply open `index.html` in a modern web browser. No build process or server required.

### Running on GitHub Pages

1. Push to GitHub
2. Enable GitHub Pages in repository settings
3. Access via: `https://<username>.github.io/infiniteposter/`

### Controls

- **Hover** over the canvas to reveal controls
- **Pause/Resume**: Toggle animation
- **Speed Dropdown**: Adjust generation speed
- **Next Style**: Skip to the next design style
- **Export**: Save current poster as PNG image

## Current Styles

### Swiss Modernist (1950s)
Grid-based compositions with limited color palettes, geometric forms, and high negative space. Inspired by Josef Müller-Brockmann and the International Typographic Style.

### Jazz Cool (1960s)
Asymmetric, dynamic compositions with bold colors and organic shapes. Inspired by Blue Note Records album covers and Reid Miles' work.

## Technical Architecture

### Core Technologies
- **P5.js**: Creative coding framework for canvas rendering
- **p5.brush**: Natural media simulation (watercolor, pencil, marker, spray, acrylic)

### Key Systems

#### Grid System
12-column grid providing underlying structure for form placement with configurable rigidity.

#### Composition Engine
- Spatial awareness preventing overcrowding
- Visual weight balancing (left/right, top/bottom)
- Color usage tracking for balanced palettes
- Negative space protection
- Form density management

#### Form Lifecycle
1. **Appearing** (0-5s): Stroke-by-stroke drawing animation
2. **Persisting** (5-120s): Static element in composition
3. **Removing** (120-125s): Fade out transition

#### Style DSL
Styles are defined in JSON format with properties for:
- Composition rules (grid rigidity, symmetry, negative space)
- Color palettes (limited, bold, vibrant)
- Form types and density
- Media types and textures
- Animation timing

## Development Roadmap

### Phase 1: Foundation ✅
- [x] P5.js + p5.brush integration
- [x] Grid system
- [x] Basic geometric forms
- [x] Composition engine
- [x] Two initial styles (Swiss Modernist, Jazz Cool)
- [x] User controls
- [x] Export functionality

### Phase 2: Enhanced Media (Next)
- [ ] Improved brush stroke animations
- [ ] Stencil effects
- [ ] Texture layering
- [ ] Media-specific characteristics

### Phase 3: Additional Styles
- [ ] 1980s Memphis Design
- [ ] 1990s Rave/Club aesthetics
- [ ] Psychedelic (late 1960s)
- [ ] Bauhaus influence

### Phase 4: Advanced Features
- [ ] Typography integration
- [ ] 4K resolution optimization
- [ ] Style blending/transitions
- [ ] Configuration UI
- [ ] Custom style creation

## Design Philosophy

### Anti-Slop Mechanisms
The application prevents chaotic "random art" through:
- Maximum form limits per layer
- Minimum distance requirements between forms
- Color harmony validation
- Visual weight distribution analysis
- Composition scoring system

### Design Intelligence
Forms "know" about:
- Existing elements in the composition
- Grid structure and alignment points
- Visual balance requirements
- Color relationships
- Negative space preservation

## Browser Compatibility

Tested on:
- Chrome/Edge 90+
- Firefox 88+
- Safari 14+

Requires:
- JavaScript ES6+
- HTML5 Canvas
- WebGL support (recommended for performance)

## License

MIT License - See LICENSE file for details

## Inspiration

This project draws inspiration from:
- Swiss International Style (Müller-Brockmann, Hofmann)
- American Modernism (Paul Rand, Saul Bass)
- Blue Note Records album art (Reid Miles)
- Fortune Magazine covers (1950s-60s)
- Push Pin Studios (Milton Glaser)

## Credits

Created by Damon Seeley (2026)

Built with:
- [P5.js](https://p5js.org/) by Processing Foundation
- [p5.brush](https://github.com/acamposuribe/p5.brush) by acamposuribe
