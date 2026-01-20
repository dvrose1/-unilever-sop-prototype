# Unilever S&OP PowerPoint Extension Prototype

## Overview

This is a fully functional prototype of the redesigned PowerPoint extension for Unilever's S&OP Monthly Performance Reviews. It demonstrates the streamlined user flow focused on brand slide generation.

## Features

### Core Flow
1. **Workspace Selection** - Select the Unilever S&OP workspace
2. **Template Type** - Choose "Brand Performance Slides"
3. **Brand Selection** - Pick a brand (Dove, TRESemmé, Vaseline, etc.)
4. **Channel Selection** - Select channel (National, Social, Paid Search, MikMak)
5. **Preview & Generate** - Review slides to be created with confidence scores
6. **Generation Progress** - Real-time progress indicators
7. **Success & Insights** - View generated slides and add additional insights

### Supporting Features
- **Quick Query Bar** - Always-visible bottom bar for asking questions
- **Breadcrumb Navigation** - Easy navigation back to any step
- **Confidence Scores** - 95%, 92%, 88% confidence indicators on insights
- **Checkbox Selection** - Choose which slides to generate
- **Add to Slide** - One-click insertion of additional insights

## How to Run

### Option 1: Open Directly in Browser
1. Navigate to the prototype folder:
   ```
   cd "/Users/doug/Documents/Dev/PPT Extension/prototype"
   ```

2. Open `index.html` in your browser:
   - **Mac**: `open index.html`
   - Or drag `index.html` into your browser
   - Or double-click `index.html`

### Option 2: Run with Local Server (Recommended)
For the best experience, run with a local web server:

```bash
# Using Python 3
cd "/Users/doug/Documents/Dev/PPT Extension/prototype"
python3 -m http.server 8000

# Then open: http://localhost:8000
```

## Prototype Flow

### 1. Workspace Selection
- Click on "Unilever S&OP" workspace card

### 2. Template Selection
- Click on "Brand Performance Slides" (the only enabled option)
- Other templates show "Coming Soon" badges (disabled)

### 3. Brand Selection
- Choose from: Dove, TRESemmé, Vaseline, Nexxus, Shea Moisture
- Breadcrumb navigation available to go back

### 4. Channel Selection
- Choose from: National, Social, Paid Search, MikMak
- "Add Multiple Channels" button available (not yet functional in prototype)

### 5. Preview Slides
- See 3 slides that will be generated:
  - Brand Performance Overview (95% confidence)
  - Key Insights & Recommendations (92% confidence)
  - Look Ahead Recommendations (88% confidence)
- Checkboxes to include/exclude slides
- Summary shows count and estimated time
- Click "Generate 3 Slides"

### 6. Generation Progress
- Watch real-time progress through 5 steps:
  - Analyzing data sources
  - Computing performance metrics
  - Generating visualizations
  - Creating slide layouts
  - Inserting into presentation
- Animated spinners and status updates

### 7. Success Screen
- Confirmation that slides were added
- Additional insights available to add:
  - Performance Alerts
  - Optimization Opportunities
  - Risk Indicators
- Each insight has "Add to Slide" button
- Options to create more slides or finish

## Quick Query Bar

The query bar is always visible at the bottom of the screen:

### How to Use
1. **Type a question** in the input field
2. **Press Enter** or click the send button (→)
3. **View the response** in the expanded panel
4. **Click suggestions** for quick queries:
   - "What drove Dove's performance?"
   - "Compare ROI across channels"

### Response Features
- AI avatar and "Strategy Assistant" label
- Confidence score badge
- "Add to Slide" button
- "Continue in Teams →" button for deeper analysis

## Key Design Decisions

### What Changed from Original
1. **Removed tabs** - Single linear flow instead of 5 competing tabs
2. **Progressive disclosure** - Only show next step when ready
3. **Clear hierarchy** - Template → Brand → Channel decision tree
4. **Integrated progress** - No separate "Progress" tab
5. **Contextual insights** - Shown after generation, not in separate tab
6. **Bottom query bar** - Always accessible without competing for attention

### Design Principles Applied
- **One primary action at a time** - No cognitive overload
- **Clear cause and effect** - Users know what happens when they click
- **Workflow-native** - Feels like part of PowerPoint, not a separate tool
- **Confidence transparency** - All AI outputs show confidence scores
- **Reversible actions** - Breadcrumb navigation to go back anytime

## Technical Details

- **Pure HTML/CSS/JavaScript** - No frameworks, easy to modify
- **Responsive design** - Works at different widths
- **Smooth animations** - Professional transitions and loading states
- **Realistic interactions** - Feels like a real PowerPoint add-in
- **PowerPoint-inspired styling** - Colors, fonts, and spacing match Office design language

## Customization

### Colors
Main colors defined in `styles.css`:
- Primary: `#1e3a5f` (dark blue)
- Accent: `#0078d4` (Microsoft blue)
- Success: `#107c10` (green)

### Brands/Channels
Edit in `index.html`:
- Brand list: Lines 100-124
- Channel list: Lines 150-169

### Slide Templates
Edit preview items in `index.html`: Lines 200-280

## Next Steps for Production

1. **Backend Integration**
   - Connect to Assemble Knowledge Room API
   - Real data fetching and confidence scoring
   - Actual slide generation via PowerPoint API

2. **Additional Templates**
   - Enable "BU Executive Summary"
   - Enable "SoS/SoM Update"
   - Enable "Post-Meeting Actions"

3. **Multi-channel Selection**
   - Implement bulk channel selection
   - Show all selected combinations in preview

4. **Office Add-in Manifest**
   - Package as real Office Add-in
   - Deploy to Unilever's AppSource or sideload

5. **Teams Integration**
   - Deep-link "Continue in Teams" button
   - Bi-directional sync with Teams bot

## Files Structure

```
prototype/
├── index.html          # Main HTML structure
├── styles.css          # All styling
├── script.js           # Interactive functionality
└── README.md          # This file
```

## Browser Compatibility

Tested and works in:
- Chrome 90+
- Safari 14+
- Firefox 88+
- Edge 90+

## Demo Tips

When showing this prototype:

1. **Start with workspace selection** - Shows familiar entry point
2. **Emphasize the linear flow** - "No more tab confusion"
3. **Highlight confidence scores** - "Transparency on every insight"
4. **Demo the query bar** - "Quick questions without leaving the flow"
5. **Show the generation progress** - "See exactly what's happening"
6. **End with insights screen** - "Contextual help when you need it"

## Questions or Issues?

This prototype demonstrates the core UX improvements. For production implementation or modifications, the code is clean and well-commented for easy updates.
