Day 39 — PDF Splitter & Merger

Project

PDF Splitter & Merger is a browser-based PDF utility with two main workflows:

PDF Splitter

PDF Merger

Task Checklist

Read the provided resources.

Review the solution workflow.

Open Claude.

Set Claude effort level to Low.

Start a new conversation.

Paste the PDF Splitter & Merger prompt.

Answer the Claude interview question — Automatically design the application / proceed with automatic feature selection.

Generate the complete HTML application.

Save the generated HTML file.

Open/review the application interface locally.

Test the PDF Splitter interface and controls.

Test the PDF Merger interface and controls.

Review the preview/download workflow in the generated application.

Take screenshots.

Create the Day39 submission folder.

Create this day39.md file.

Prepare the generated HTML file for upload.

Upload screenshots, generated HTML file, and processed PDFs to GitHub.

Commit and push the changes.

Submit the GitHub commit URL.

Features Implemented

PDF Splitter

PDF file upload with drag-and-drop.

Automatic page-count detection.

Page thumbnail preview.

Page selection.

Select all / clear selection.

Custom page ranges.

Split after specific page numbers.

Split every N pages.

Extract selected pages.

Multiple split ranges in one operation.

Input validation for invalid ranges.

Output structure preview.

Processing progress indicator.

Individual PDF downloads.

PDF Merger

Multiple PDF upload.

Drag-and-drop upload.

File list with page counts and sizes.

Drag-and-drop document reordering.

Remove individual files.

Total file and page counts.

Output-size estimate.

Merge and download workflow.

Progress indicator.

UI / UX

Premium dark interface.

Glass-style cards.

Responsive layout.

Hover and transition effects.

Drag-and-drop interactions.

Modal PDF preview.

Keyboard shortcut support (Ctrl/Cmd + O, Esc).

Clear validation and toast feedback.

Screenshots

1. PDF Splitter Interface



2. PDF Merger Interface



Key Learnings

Client-side processing can improve privacy because documents can be processed in the browser rather than being sent to a backend.

Good PDF utilities need clear validation so users know exactly which pages or files will be processed.

Visual previews reduce mistakes when users are selecting pages or arranging documents.

Drag-and-drop improves workflow speed, especially for merging multiple documents.

Progress feedback matters because PDF operations can take noticeable time with larger documents.

Reusable JavaScript components make it easier to maintain upload, preview, selection, validation, and download functionality.

Responsive design is important because document utilities may be used on both desktop and smaller screens.

Important Note

The generated application currently loads the PDF processing engines dynamically from CDN resources. Therefore, the PDF processing portion requires internet access on the first load and does not yet satisfy a strict fully-offline/no-external-resource requirement. The UI and application structure are self-contained in the HTML file.

Files

PDF_Splitter_and_Merger.html — generated application.

01_splitter_interface.png — splitter screenshot.

02_merger_interface.png — merger screenshot.

day39.md — project documentation.

Git Commands

git add Day39/
git commit -m "Add Day39 PDF Splitter and Merger"
git push origin main

After pushing, copy the commit URL from GitHub and submit it.