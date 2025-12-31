# JSON Key Comparison Tool

A powerful web-based tool for comparing two JSON files and identifying key differences including additions, deletions, position changes, and value modifications.

## Features

### 🔍 Comprehensive Comparison
- **Added Keys**: Identifies new keys present in the new version
- **Removed Keys**: Detects keys that were deleted from the old version
- **Position Changes**: Tracks when keys move to different positions
- **Value Changes**: Highlights when key values are modified
- **Unchanged Keys**: Shows keys that remain identical

### 📤 Easy File Upload
- **Drag & Drop**: Simply drag JSON files onto the upload zones
- **Click to Browse**: Click the upload area to select files
- **Upload Status**: Visual feedback showing:
  - Success indicator with checkmark
  - File size information
  - Number of keys in the uploaded JSON

### 🎯 Smart Filtering
Quick filter buttons to show only specific types of changes:
- **All** - Show all keys
- **+ Added** - Only newly added keys
- **- Removed** - Only deleted keys
- **↕ Moved** - Only keys that changed position
- **≠ Changed** - Only keys with value changes
- **= Unchanged** - Only keys that stayed the same

### 🧠 Deep Comparison Mode
Enable **"Deep compare JSON values"** option to intelligently compare nested JSON objects:
- Ignores key order in nested objects
- Treats `{"a": 1, "b": 2}` and `{"b": 2, "a": 1}` as identical
- Perfect for comparing translation files where only key order differs

### 📊 Visual Statistics
Real-time statistics dashboard showing:
- Total number of added keys
- Total number of removed keys
- Total number of position changes
- Total number of value changes
- Total number of unchanged keys

### 🎨 Color-Coded Results
Easy-to-read color coding:
- 🟢 **Green**: Added keys
- 🔴 **Red**: Removed keys
- 🟡 **Yellow**: Position changes
- 🔵 **Blue**: Value changes
- ⚪ **Gray**: Unchanged keys

### 💾 Full Value Display
- No truncation - see complete values
- Proper formatting for nested JSON
- Line wrapping for long text
- Preserves formatting and indentation

## Use Cases

### Translation File Comparison
Perfect for comparing localization files (like `zh/main.json`) to identify:
- Missing translations
- Modified translations
- Reordered keys that need realignment

### Configuration Management
Compare configuration files between versions to track:
- New settings added
- Deprecated settings removed
- Modified default values

### API Response Validation
Verify API schema changes by comparing:
- Old vs new response structures
- Added or removed fields
- Modified data types or values

### Code Refactoring
Track changes in JSON-based data structures during refactoring:
- Ensure no data loss
- Verify intentional changes
- Identify unintended modifications

## How to Use

1. **Open the Tool**
   ```bash
   open /Users/linmoumou/Documents/Github/json-diff-tool/index.html
   ```
   Or simply double-click `index.html` in Finder

2. **Upload Files**
   - Upload the **old version** JSON file on the left
   - Upload the **new version** JSON file on the right
   - You'll see upload success indicators with file stats

3. **Configure Options** (Optional)
   - Check **"Deep compare JSON values"** if you want to ignore key order in nested objects

4. **Start Comparison**
   - Click the **"Start Comparison"** button
   - Results will appear below with statistics and detailed comparison

5. **Filter Results** (Optional)
   - Use filter buttons to focus on specific types of changes
   - Statistics update dynamically based on the active filter

6. **Review Results**
   - Scroll through the comparison table
   - Each row shows:
     - Status symbol (+ - ↕ ≠ =)
     - Key name
     - Old and new positions
     - Old and new values (full content)

## Technical Details

- **Framework**: Pure HTML/CSS/JavaScript
- **Styling**: Tailwind CSS (CDN)
- **Browser Support**: Modern browsers (Chrome, Firefox, Safari, Edge)
- **File Size**: No limits (handled in-memory)
- **Dependencies**: None (runs offline after initial CDN load)

## Features Roadmap

- ✅ Basic key comparison
- ✅ Upload status indicators
- ✅ Filter functionality
- ✅ Deep comparison mode
- ✅ Full value display
- ⬜ Export comparison results to CSV/JSON
- ⬜ Syntax highlighting for JSON values
- ⬜ Diff view for changed values
- ⬜ Search/filter by key name
- ⬜ Compare more than 2 files
- ⬜ Dark mode support

## Examples

### Example 1: Translation File Reordering
If you have two Chinese translation files where keys were reordered:
- Enable **"Deep compare"** mode
- Keys with only position changes will show as **↕ Moved**
- Keys with actual translation changes will show as **≠ Changed**
- Filter to **"≠ Changed"** to focus only on real translation updates

### Example 2: Finding Missing Translations
Comparing old and new translation files:
- Filter to **"+ Added"** to see new strings that need translation
- Filter to **"- Removed"** to see deprecated strings
- Use statistics to track translation progress

### Example 3: API Schema Evolution
Comparing API response schemas:
- See which fields were added to the response
- Identify removed/deprecated fields
- Track renamed fields (will show as removed + added)

## License

This tool is provided as-is for personal and commercial use.

## Author

Created for comparing JSON files, particularly useful for translation file management and configuration tracking.
