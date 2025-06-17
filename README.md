# Blue Archive Coordinate Tool

A browser bookmarklet for mapping precise tap positions from Blue Archive guide videos.

## What This Does

When you're watching a torment/lunatic raid clear or JFD guide, this tool lets you mark exactly where someone taps their screen. You get precise coordinates that help you replicate their positioning on your own device.

Think of it like placing digital pins on a video. Each pin captures both the visual position and the exact coordinates needed to execute the same strategy yourself.

## Why You Need This

High-difficulty Blue Archive content (torment/lunatic difficulty, final restriction stages) sometimes requires pixel-perfect positioning. The difference between clearing and failing can come down to exact student placement that you can't judge by eye alone... amongst other things like crit and all.

## Quick Start

**Install the Bookmarklet:**
1. Open the HTML file in your browser
2. Drag the blue bookmarklet link to your bookmarks bar
3. You now have the tool installed

**Use on Any (Youtube) Video:**
1. Go to a Blue Archive guide video
2. Click your bookmarklet to activate the tool
3. Hold Shift and click anywhere on the video to place markers
4. Each marker shows both pixel coordinates and percentage ratios

**Get Your Data:**
- Click "Export" to save coordinates as files
- Choose CFG format for BlueStacks or JSON for general use
- Import coordinates from other players' exports

## Understanding the Interface

**Zoom Indicator (top-left):** Shows your browser zoom level. The tool automatically adjusts coordinates when you zoom in to see details.

**Resolution Panel (above video):** Displays video dimensions. You can lock this to prevent changes when the video resizes.

**Control Panel (right side):** Manage markers, customize appearance, and export data. Each marker shows four coordinate values:
- X/Y pixels: Exact screen position
- Ratio X/Y: Position as percentage of screen size (This is what you enter for your emulator!)

## Platform Compatibility

The ratio coordinates work across different platforms automatically. Mark positions while watching on your computer. The relative positioning stays accurate regardless of screen size.

While this is made with BlueStacks in mind, it can also work with MumU player albeit you have to dig into your files and find the CFG for yout keybind layout. This is untested with other emulators.

## Best Practices

**For Analysis:**
- Pause videos at critical positioning moments
- Label markers with meaningful names (like "DPS Safe Spot" or "TYuuka EX 2nd use")
- Export your coordinate sets to save your analysis work or directly enter them in your emulator

**For Execution:**
- Practice the positioning sequences until they become muscle memory (or wing it)
- Use the visual feedback to understand spacing requirements between students, the screen can move! Especially in moving raids such as Chesed or raids where the targeted student matters (Shirokuro)

**For Sharing:**
- Include team composition info when sharing coordinates
- Document why specific positions matter, not just where they are


## Troubleshooting

**Tool doesn't activate:** Make sure you're on a page with a video and that your browser allows JavaScript in bookmarks.

**Markers hard to see:** Use the control panel to adjust marker colors and sizes for better visibility on different video types.

**Coordinates seem wrong:** Check the zoom indicator and try refreshing the page. Browser zoom can sometimes cause accuracy issues if the compensation system gets confused.

**Export not working:** Try a different file format or check that your browser isn't blocking file downloads.

## Technical Notes

The tool works by creating an overlay on top of the video that captures your clicks without interfering with video controls. All coordinate calculations happen in real-time and automatically adjust for zoom level changes.

Coordinate data uses percentage ratios specifically because Blue Archive players use many different devices and screen configurations. This approach ensures that positioning analysis translates accurately across platforms.

The bookmarklet is completely self-contained and doesn't require any external servers or accounts. Everything runs locally in your browser for maximum compatibility and privacy.

---
## Special Thanks!

**Remember:** This tool helps you understand expert positioning, but mastering high-difficulty content still requires practice and strategic understanding. Use coordinate mapping as a foundation for developing your own precision gameplay skills.

**This tool was inspired by https://arca.live/b/bluearchive/130030062** Full credits to the idea to its creator, 야드파운드인치갤런!

Thank you Soomshigi for helping me create this post as it was directly inspired from someone else on Arca: https://arca.live/b/bluearchive/139131901

Thank you Mapleless for providing a keymap file for MumuPlayer as I wasn't using that emulator at the time!
