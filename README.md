# Mermaid Diagram Exporter

A lightweight web-based tool for creating, editing, and exporting Mermaid diagrams with advanced features. Perfect for database design documentation, flowcharts, and entity relationship diagrams.

## Overview

The Mermaid Diagram Exporter is a versatile HTML and JavaScript application that allows you to:

- Create and edit diagrams using the Mermaid syntax
- Render diagrams in real-time
- Export diagrams as high-quality PNG or SVG files
- Copy diagrams directly to clipboard
- Choose from multiple visual themes
- Extract diagrams from markdown files
- Use pre-built database design diagrams

## Features

### Core Functionality
- **Real-time rendering** of Mermaid diagrams
- **Export to PNG** with customizable quality settings
- **Export to SVG** for lossless scaling and editing
- **Copy to clipboard** for quick insertion into other applications
- **Theme selection** with four options (Default, Dark, Forest, Neutral)
- **Custom diagram titles** that appear in the rendered output
- **File-based loading** to extract diagrams from markdown files

### Pre-built Diagram Libraries
The exporter comes with three comprehensive sets of pre-built diagrams:

1. **Package Delivery Database**
   - Entity-Relationship Diagram
   - Database Schema
   - Package Tracking Flow

2. **Hospital Database**
   - Entity-Relationship Diagram
   - Patient-Doctor Relationship
   - Medical Log Flow

3. **Database Normalization**
   - Original Schema
   - Normalized Schema (4NF)
   - Normalization Process

## How to Use

### Getting Started
1. Open `MermaidExporter.html` in any modern web browser
2. Start creating your diagram in the editor or use one of the pre-built templates
3. Click "Render Diagram" to see your diagram

### Creating a Diagram
1. Enter your Mermaid syntax into the code editor
2. Add an optional title in the "Diagram Title" field
3. Click "Render Diagram" to preview your creation
4. Use the theme selector to change the visual style

### Exporting Diagrams
- Click "Export as PNG" for a high-quality bitmap image
- Click "Export as SVG" for a scalable vector graphic
- Click "Copy to Clipboard" to copy the SVG code for pasting elsewhere

### Loading from Files
1. Click the "Load From File" tab
2. Select a markdown file containing Mermaid code blocks (````mermaid`)
3. Click "Load Diagrams" to extract and list available diagrams
4. Click "Load This Diagram" to open any extracted diagram in the editor

### Using Pre-built Diagrams
1. Click one of the preset tabs (Package Delivery, Hospital, or Normalization)
2. Select the specific diagram you want to use
3. The diagram will load into the editor where you can modify it or export it directly

## Mermaid Syntax Examples

### Entity Relationship Diagram
```
erDiagram
    CUSTOMER ||--o{ ORDER : places
    ORDER ||--|{ LINE_ITEM : contains
    
    CUSTOMER {
        string name
        string email
    }
    ORDER {
        int orderNumber
        date orderDate
    }
    LINE_ITEM {
        string product
        int quantity
    }
```

### Class Diagram
```
classDiagram
    class Animal {
        +String name
        +move() void
        +eat() void
    }
    class Dog {
        +bark() void
    }
    Animal <|-- Dog
```

### Flowchart
```
flowchart TD
    A[Start] --> B{Decision}
    B -->|Yes| C[Do Something]
    B -->|No| D[Do Something Else]
    C --> E[End]
    D --> E
```

## Technical Details

### Dependencies
- [Mermaid.js](https://mermaid.js.org/) (v10.6.0) - For diagram rendering
- [FileSaver.js](https://github.com/eligrey/FileSaver.js) (v2.0.5) - For file downloads
- [html2canvas](https://html2canvas.hertzen.com/) - For PNG export functionality

### Browser Compatibility
Works with all modern browsers including:
- Chrome
- Firefox
- Safari
- Edge

### Hosting
This is a client-side application that can be run locally without any server requirements. Simply open the HTML file in your browser to use.

## Future Enhancements
- Batch export of multiple diagrams
- Custom sizing and scaling options
- Local storage of diagrams
- More diagram templates and examples

## License
This tool is provided as-is for educational and practical purposes.

## Acknowledgements
Built using Mermaid.js, the open source diagramming and charting tool.
