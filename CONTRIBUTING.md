# Contributing to ESPHome CYD BVG Departure Display

First off, thank you for considering contributing to this project! 🎉

## How Can I Contribute?

### 🐛 Reporting Bugs

Before creating bug reports, please check the existing issues to avoid duplicates.

**When submitting a bug report, include:**
- A clear and descriptive title
- Steps to reproduce the behavior
- Expected behavior vs actual behavior
- Screenshots (especially of the display)
- ESPHome version and Home Assistant version
- Your hardware model (confirm it's ESP32-3248S035C)
- Relevant log output

### 💡 Suggesting Enhancements

Enhancement suggestions are welcome! Please provide:
- A clear description of the enhancement
- Why this would be useful
- Potential implementation approach (if you have ideas)

### 🔧 Pull Requests

1. **Fork the repository** and create your branch from `main`
2. **Make your changes** following the code style
3. **Test thoroughly** on actual hardware if possible
4. **Update documentation** (README, comments, etc.)
5. **Commit with clear messages** following [Conventional Commits](https://www.conventionalcommits.org/)

Example commit messages:
```
feat: add auto-dim based on time of day
fix: correct LED color mapping for RGB
docs: update installation instructions
refactor: simplify departure time calculation
```

## Code Style

### YAML Files
- Use 2 spaces for indentation
- Add comments for complex logic
- Keep line length reasonable (<120 chars)
- Use descriptive names for IDs

### Python/Lambda Code
- Follow PEP 8 style guide
- Add inline comments for complex calculations
- Use meaningful variable names

## Project Structure

Please maintain the existing structure:
```
esphome-cyd-bvg-departure-display/
├── cyd-bvg.yaml           # Main config - keep customizable via substitutions
├── includes/              # Modular includes - keep generic
├── home-assistant/        # HA templates - document filter logic
└── images/                # Screenshots - optimize for web
```

## Testing Checklist

Before submitting a PR, verify:

- [ ] Configuration validates with `esphome config cyd-bvg.yaml`
- [ ] Changes tested on actual CYD hardware
- [ ] All 5 departure lines display correctly
- [ ] LED delay warning works (if touched)
- [ ] Documentation updated (README, comments)
- [ ] No hardcoded values (use substitutions)
- [ ] German umlauts display correctly (ä, ö, ü, ß)

## Areas Needing Help

We'd love contributions in these areas:

### 🎨 UI/Display
- Different layouts (vertical, compact, etc.)
- Support for more than 5 departures
- Icons for transport types (S-Bahn, Tram, Bus)
- Night mode / color themes

### 🔧 Features
- Touch screen support (change station, refresh)
- Multiple station support
- Integration with other transport systems
- Accessibility features

### 📚 Documentation
- Video setup guide
- More troubleshooting scenarios
- Translation to other languages
- Better screenshots

### 🧪 Testing
- Different hardware variations
- Other BVG/VBB stations
- Edge cases (no departures, all cancelled, etc.)

## Credits

When contributing, you'll be added to the contributors list automatically by GitHub.

For significant contributions, we'll also mention you in the README credits section.

## Questions?

Feel free to open an issue with the `question` label if you need help contributing!

## Code of Conduct

Be respectful, inclusive, and constructive. This is a community project - let's keep it friendly! 🤝

---

Thank you for contributing! 🚇
