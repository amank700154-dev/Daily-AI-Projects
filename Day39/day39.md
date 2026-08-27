# Day 39 — PDF Splitter & Merger

## Project
**PDF Splitter & Merger** is a browser-based PDF utility with two main workflows:
- PDF Splitter
- PDF Merger

## Task Checklist

- [x] Read the provided resources.
- [x] Review the solution workflow.
- [x] Open Claude.
- [x] Set Claude effort level to Low.
- [x] Start a new conversation.
- [x] Paste the PDF Splitter & Merger prompt.
- [x] Answer the Claude interview question — Automatically design the application / proceed with automatic feature selection.
- [x] Generate the complete HTML application.
- [x] Save the generated HTML file.
- [x] Open/review the application interface locally.
- [x] Test the PDF Splitter interface and controls.
- [x] Test the PDF Merger interface and controls.
- [x] Review the preview/download workflow in the generated application.
- [x] Take screenshots.
- [x] Create the Day39 submission folder.
- [x] Create this day39.md file.
- [x] Prepare the generated HTML file for upload.
- [ ] Upload screenshots, generated HTML file, and processed PDFs to GitHub.
- [ ] Commit and push the changes.
- [ ] Submit the GitHub commit URL.

## Features Implemented

### PDF Splitter
- PDF upload with drag-and-drop.
- Automatic page-count detection.
- Page thumbnail preview.
- Page selection.
- Select all / clear selection.
- Custom page ranges.
- Split after specific page numbers.
- Split every N pages.
- Extract selected pages.
- Multiple split ranges.
- Input validation.
- Output structure preview.
- Processing progress indicator.
- Individual PDF downloads.

### PDF Merger
- Multiple PDF upload.
- Drag-and-drop upload.
- File list with page counts and sizes.
- Drag-and-drop document reordering.
- Remove individual files.
- Total file and page counts.
- Output-size estimate.
- Merge and download workflow.
- Progress indicator.

### UI / UX
- Premium dark interface.
- Glass-style cards.
- Responsive layout.
- Hover and transition effects.
- Drag-and-drop interactions.
- Modal PDF preview.
- Keyboard shortcut support.
- Validation and toast feedback.

## Screenshots

- `01_splitter_interface.png` — PDF Splitter interface.
- `02_merger_interface.png` — PDF Merger interface.

## Key Learnings

1. Client-side processing can improve document privacy because files can be processed in the browser.
2. PDF utilities need clear validation so users understand which pages and files will be processed.
3. Visual previews reduce selection and ordering mistakes.
4. Drag-and-drop makes multi-document workflows faster.
5. Progress feedback improves the experience during larger PDF operations.
6. Reusable JavaScript logic makes upload, preview, selection, validation, and download features easier to maintain.
7. Responsive design is important for document tools used across devices.

## Important Note

The generated application currently loads the PDF processing engines dynamically from CDN resources. Therefore, PDF processing requires internet access on first load and does not yet satisfy a strict fully-offline/no-external-resource requirement.

## Git Commands

```bash
git add Day39/
git commit -m "Add Day39 PDF Splitter and Merger"
git push origin main
```
