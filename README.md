# Anime Studio AI — Mock Prototype

A no-cost, browser-only mock web app for turning the supplied *Short Film.docx* screenplay into a seven-scene realistic-anime storyboard.

## Run it

1. Extract the ZIP file.
2. Open `index.html` in a modern browser (Chrome, Edge, Firefox or Safari).
3. Select any of the seven scenes in the left sidebar.
4. Edit the visual/motion prompt, camera direction or target duration and choose **Save edits**.
5. Choose **Simulate scene generation** for a single scene, or **Simulate all 7 scenes** to test the mock job flow.
6. Choose **Export storyboard JSON** to download the scene and character data.

No npm, Python, server, account, API key, GPU or paid API is required for this mock version.

## Important limitations

- The preview is a CSS illustration placeholder, not AI-generated footage.
- “Simulate generation” changes only local UI state. It does not contact a model or generate a video.
- Edits live in the current page session; export JSON to keep them.
- Character descriptions avoid inventing fixed physical traits that are not established in the screenplay. Visual prompts are editable adaptation notes.
- The source screenplay's seven scenes and core dialogue beats are represented in `index.html` and the exported JSON.

## Suggested next implementation milestone

Move scene/character data into a JSON file, create a FastAPI backend with SQLite persistence, and implement a `VideoProvider` interface. Keep a mock provider as the default; connect a real image-to-video provider only after the workflow is tested.
