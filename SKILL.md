---
name: FileDeepAnalyzer
description: Advanced file reader that deeply analyzes uploaded documents/images/data. Extracts text/tables/images, summarizes insights, identifies patterns, answers questions with evidence. Supports PDF, DOCX, TXT, CSV, images, code files.
keywords: file analysis, document understanding, data extraction, summarization, OCR
icon: 📄🔍
---

# FileDeepAnalyzer Skill

## Capabilities
- **Multi-format reading**: PDF (text/tables/images), DOCX, TXT, Markdown, CSV/Excel, images (OCR + description), code files (syntax analysis).
- **Deep understanding**: Chunking for large files, semantic search, entity extraction, sentiment/theme analysis.
- **Structured outputs**: Summary, key facts table, Q&A with quotes, visualizations (charts from data).
- **Context retention**: Remembers file contents across conversation turns.

## Usage Instructions
1. **Upload file first** in Manus chat (drag/drop or + icon).
2. Activate: `/FileDeepAnalyzer`
3. Commands (natural language OK):
   - "Summarize this file in 200 words."
   - "Extract all tables/names/dates from [filename]."
   - "Analyze code structure and suggest improvements."
   - "Rate content quality (1-10) on clarity, depth; explain."
   - "Answer: What are the main arguments?" (quotes evidence).
   - "Generate CSV of key data points."
   - "Visualize trends from CSV/image chart."

## Tools & Workflow
1. **Read file**: Use `read_file(filename)` or multimodal for images/PDF.
2. **Parse**:
   - Text/PDF: Extract full text, chunk >5k tokens.
   - Tables: Parse to Markdown/CSV.
   - Images: OCR + describe objects/context.
3. **Analyze**:
   - Embed chunks for RAG.
   - Extract: NER (names/orgs), keywords, sentiment.
   - Structure: Headings, sections, length/stats.
4. **Output**: Table of insights + ask for refinements.

## Example Outputs
| Section | Key Insight | Quote/Evidence |
|---------|-------------|---------------|
| Summary | Core topic: AI ethics | "AI must prioritize..." |
| Entities | John Doe (author) | Page 2 |

**Confirm before actions like editing/exporting.**

## Files
- Uses Manus built-in: browser/read for files, code_execution for processing.
