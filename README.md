# Blue Archive Coordinate Tool

## Table of Contents

1. [What This Tool Does](#what-this-tool-does)
2. [Why This Tool Exists](#why-this-tool-exists)
3. [How to Get Started](#how-to-get-started)
4. [Using the Tool](#using-the-tool)
5. [Blue Archive Integration](#blue-archive-integration)
---

## What This Tool Does

The Blue Archive Coordinate Tool is a browser bookmarklet that transforms any (youtube) video page into an interactive coordinate mapping workspace. Think of it as placing a transparent overlay on top of a video where you can drop markers and measure exact positions.

When you activate this tool on a video, it creates a layer that lets you click and place numbered markers at specific locations. Each marker automatically calculates both pixel coordinates and percentage-based ratios, which are exactly what emulators like BlueStacks need to know where to tap on the screen.

The tool essentially bridges the gap between watching a Blue Archive guide video and perfecting your skill locations. Instead of guessing where buttons are located or manually measuring screen positions, you can precisely mark every important tap location.

---

## Why This Tool Exists

Raid score chasers can sometimes face a common challenge. For some raids, the game requires precise timing and positioning for optimal results. However, creating coordinates traditionally requires tedious trial-and-error positioning.

This tool solves several specific problems that Blue Archive players encounter. First, it eliminates the guesswork when watching guide videos. You can pause at any moment, mark exactly where the player tapped, and instantly get the coordinates needed. Second, it handles the complex math automatically. Emulators require coordinates as percentages of screen size, which changes based on your device resolution and zoom level. The tool calculates these ratios instantly and adjusts them when your screen changes.

Third, it provides a visual confirmation system. Instead of hoping your automation script will tap in the right place, you can see exactly where each marker is positioned and test different configurations before committing to them.

Finally, this tool was taken in inspiration from: https://arca.live/b/bluearchive/130030062

---

## How to Get Started

### Step 1: Understanding Bookmarklets

A bookmarklet is essentially a small program disguised as a bookmark. Instead of taking you to a website, it runs JavaScript code on whatever page you are currently viewing. This approach means the coordinate tool does not require any software installation, server setup, or browser extensions. It works entirely within your existing browser using standard web technologies.

To install the bookmarklet, you need to save it to your browser's bookmarks bar. This process varies slightly between browsers, but the core concept remains the same. You are creating a special bookmark that contains executable code rather than a website address.

### Step 2: "Installing" the Bookmarklet

Open the Blue Archive Coordinate Tool webpage (the HTML file in this project). You will see comprehensive instructions and a prominent link labeled "Blue Archive Coordinates Bookmarklet". This link contains the entire coordinate tool program encoded as a special URL.

The easiest installation method is dragging the link directly to your bookmarks bar. Most modern browsers display the bookmarks bar below the address bar, though you may need to enable it through your browser settings if it is not visible. Simply click and drag the bookmarklet link from the webpage to your bookmarks bar, then release it. Your browser will create a new bookmark containing the coordinate tool.

Alternatively, you can right-click the bookmarklet link, select "Bookmark this link" or "Add to bookmarks", and manually place it in your bookmarks bar folder. The key requirement is having quick access to activate the tool when needed.

### Step 3: Testing the Installation

Navigate to any video webpage, preferably YouTube with a Blue Archive video. Click the bookmarklet you just installed. If everything works correctly, you should see several new elements appear on the page. A zoom indicator will show in the top-left corner, a resolution panel will appear above the video, and a control panel will be positioned on the right side of the video.

If nothing happens when you click the bookmarklet, check your browser's developer console for error messages. The most common issue is browser security settings blocking JavaScript execution from bookmarks, which can usually be resolved through browser preferences.

---

## Using the Tool

### Basic Marker Placement

The fundamental operation of the coordinate tool revolves around placing markers at specific locations on the video. However, the interaction method might feel unusual at first. Instead of simply clicking where you want a marker, you must hold the Shift key while clicking. This design prevents accidental marker placement and allows the underlying video controls to remain functional.

When you hold Shift and click anywhere on the video, the tool creates a numbered marker at that exact position. Each marker consists of several visual elements: a colored ring that makes it easy to spot, a small dot at the precise center point, and a text label showing the marker number. These visual elements help you understand exactly where each coordinate point is located.

The marker system automatically calculates multiple coordinate formats for each placement. The tool measures the pixel position relative to the video's current size, calculates the percentage-based ratios that automation tools require, and updates all values instantly when you resize the video or zoom your browser.

### Understanding the Control Panel

The control panel appears on the right side of the video and serves as the command center for all coordinate operations. The panel contains several distinct sections, each handling different aspects of marker management.

The top section provides basic marker operations. The "Add" button creates a new marker at the center of the video, which is useful when you need a starting point for fine-tuning. The marker list below shows detailed information for each marker you have placed, including both pixel coordinates and percentage ratios.

The customization section lets you adjust marker appearance to suit your preferences or improve visibility on different video types. You can change the ring size to make markers more prominent on large screens or smaller for detailed work. The ring and dot colors can be adjusted to contrast better with specific video content, ensuring markers remain visible regardless of the background.

### Working with Coordinates

Each marker generates four coordinate values that serve different purposes in automation setup. The X and Y pixel values show the exact position in screen pixels, which is useful for understanding absolute positioning. The Ratio X and Ratio Y values express the same position as percentages of the total video size, which is what you would enter in the emulator.

Understanding why both formats matter helps clarify when to use each one. Pixel coordinates are absolute measurements that change when the video size changes. If you resize your browser window or switch to fullscreen mode, the pixel coordinates of the same visual element will be different. Ratio coordinates, however, remain constant regardless of screen size because they express position as a percentage of the total area.

This dual system means you can set up coordinates on a small browser window and use them on a fullscreen BlueStacks instance without any conversion calculations. The tool handles all the mathematical relationships automatically.

### Marker Management

Markers can be edited, moved, and customized after creation to ensure precise positioning. Clicking and dragging any marker allows you to fine-tune its position while watching the coordinate values update in real-time. This interactive adjustment system means you never have to recreate a marker from scratch if it is slightly off-target.

Each marker in the control panel includes input fields for direct coordinate editing. You can type specific values if you know exactly where a marker should be positioned, or you can make small incremental adjustments by changing the numbers manually. The tool immediately updates the visual marker position when you modify any coordinate value.

The labeling system allows you to assign meaningful names to each marker beyond the automatic numbering. For example, you might label markers as "TYuuka first EX", "DHina EX", or "SHanako EX" to make your coordinate sets more understandable when sharing with others or returning to them later.

---

## Blue Archive Integration

### BlueStacks Compatibility

BlueStacks is an available emulator for Blue Archive, and this coordinate tool is specifically designed to integrate seamlessly with BlueStacks control schemes. When you export coordinates from the tool, you can choose between two formats that serve different purposes in the BlueStacks ecosystem.

The CFG format creates a complete BlueStacks control scheme file that you can import directly into your BlueStacks installation. This format includes all the metadata and structure that BlueStacks expects, making the import process completely seamless. The tool automatically generates appropriate control names, timestamps, and configuration data that BlueStacks uses for internal management.

The JSON format provides a simplified data structure that is easier to read and modify manually. This format is useful when you want to extract coordinate data for use in custom automation scripts or when you need to merge coordinate sets from different sources.

### Coordinate Precision and Scaling

Torment and Lunatic raids (or even other modes!) sometimes requires extremely precise coordinate targeting because the game's interface elements are often small and densely packed. A few pixels difference can mean missing an optimal area entirely. The coordinate tool addresses this precision requirement through several technical approaches.

The zoom compensation system automatically adjusts all coordinate calculations when you change your browser zoom level. This feature is crucial because many players need to zoom in on videos to see fine details, but traditional coordinate tools become inaccurate when the display scale changes. The tool continuously monitors the zoom level and recalculates all marker positions to maintain accuracy.

The resolution locking feature prevents accidental coordinate drift when the video player changes size. You can lock the tool to specific dimensions, ensuring that all coordinate calculations remain consistent even if the video player interface changes size due to fullscreen transitions or browser window adjustments.

### Sharing and Collaboration

The coordinate tool facilitates sharing automation setups between Blue Archive players through standardized export formats. When you create a set of coordinates for a particular farming route or battle strategy, you can export the data and share it with others who can import it directly into their own setup.

This sharing capability creates opportunities for community collaboration on strategies. Experienced players can create and distribute coordinate sets for new content, helping less technical players access coordinates without needing to understand the underlying mathematics.
