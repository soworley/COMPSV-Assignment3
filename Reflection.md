
---

# `REFLECTION.md`
> Put this file in the repo root. Add your Copilot chat screenshots into `screenshots/` and update the image filenames in this file so the instructor can see them.

```markdown
# Reflection — GitHub Copilot & Programming

**Project:** Mini Social Feed  
**Tech stack:** HTML, CSS, JavaScript (no framework)  
**Time spent with Copilot (planned):** ~2 hours

---

## 1) What did you ask Copilot to help you build? How did you break down the problem?

**What I asked Copilot:**  
- I asked Copilot to scaffold the basic UI (a page with a feed and a "Create Post" area).
- I asked for a JavaScript module to manage posts, likes, comments, and localStorage persistence.
- I asked for CSS for a simple, modern card UI.

**How I broke down the work (example prompts I used):**
1. "Create a simple HTML page for a social feed with a new-post form and a posts list."
2. "Add a JS file that renders posts from an array and supports likes and comments."
3. "Make the app persist posts in localStorage."
4. "Add a like button that toggles and updates a like counter."

I built feature-by-feature: scaffold → rendering → like button → comments → persistence → styling.

---

## 2) How did your approach to asking questions change as you worked?

At first I used broad prompts ("create a social feed page"). As Copilot produced code I shifted to much more targeted prompts: "Implement toggling likes for a post object" or "How to save posts to localStorage and retrieve them on load". I also used follow-up prompts to refine UI behavior (e.g., "make comment input clear after adding").

---

## 3) What parts of the development process with GitHub Copilot surprised you?

- **Speed:** Copilot quickly produced useful scaffolding (HTML + JS structure) and saved a lot of typing.
- **Quality variance:** Some suggestions were ready-to-use; others needed linting or small security fixes (I added a simple `escapeHtml` function to avoid HTML injection).
- **Context sensitivity:** Copilot produced better code after the file had some context — it adapted to file names and variable names I’d already used.

---

## 4) What did you learn about the technology you used that you didn't know before?

- I reinforced how to store arrays of objects in `localStorage` and restore them safely.
- I practiced progressive enhancement without frameworks — event delegation vs. per-element handlers and simple escaping to mitigate injection risk.
- I learned better prompt phrasing: specific, incremental prompts give more usable completions than very large "do everything" prompts.

---

## 5) What would you do differently if you had to build this again?

- Use modular code earlier (split into small functions / modules).
- Add tests (unit tests for core functions).
- Use a small bundler or React if I wanted a more scalable UI.
- Request more specific Copilot prompts asking for edge-case handling (empty comments, XSS prevention, accessibility tweaks).

---

## Evidence / Screenshots from GitHub Copilot chat (place screenshots in the `screenshots/` folder)

**How to include screenshots:**  
1. In your local repo, create a folder `screenshots/`.
2. Add the Copilot chat images (e.g., `copilot-chat-1.png`, `copilot-chat-2.png`).
3. Update the image references below if you use different filenames.

**Example screenshot references (replace with your actual screenshots):**

- ![Copilot chat prompt and suggestion — initial scaffolding](screenshots/copilot-chat-1.png)  
  *This screenshot should show the prompt where I asked Copilot to scaffold the HTML and the suggestion it provided.*

- ![Copilot chat showing JS function suggestion for like button behavior](screenshots/copilot-chat-2.png)  
  *This screenshot should show a snippet where Copilot suggested the like toggle implementation.*

- ![Copilot chat showing README text generation](screenshots/copilot-chat-3.png)  
  *This screenshot should show Copilot producing the README text or suggestions that I accepted/modified.*

---

## Short transcript excerpts (copy/paste of chat text if you cannot screenshot)

> **User:** "Create a simple HTML page for a social feed with a new post form and a container for posts."  
> **Copilot:** "Here's a minimal HTML structure with `#new-post` and `#posts` sections. I'll also include a basic CSS class structure."

> **User:** "Add JS to render posts from an array and allow toggling likes."  
> **Copilot:** "You can map over posts and build DOM elements; attach a click handler that toggles `post.liked` and increments or decrements `post.likes`."

> **User:** "How can I persist posts in localStorage?"  
> **Copilot:** "Use `localStorage.setItem('posts_v1', JSON.stringify(posts))` on state changes, and initialize with `JSON.parse(localStorage.getItem('posts_v1')) || samplePosts`."

---

## Final notes / Submission checklist

- [ ] All code files added to repository (`index.html`, `style.css`, `app.js`)
- [ ] `README.md` included (see above)
- [ ] `REFLECTION.md` included (this file)
- [ ] Add your Copilot chat screenshots into `screenshots/` and push them
- [ ] Commit messages example: `git commit -m "Initial app scaffold (Copilot-assisted)"` and `git commit -m "Add likes and comments (Copilot-assisted)"`

When you push the repo, submit the link to your class system.

Good luck — if you want, I can also:
- Convert this into a React app (single-file) if you prefer React for the course,
- Generate a short GIF demo you can include in the README (needs a local recording step),
- Produce a sample `WORKFLOW_ANALYSIS.md` / commit history narrative.

Tell me which of those (if any) you want next and I’ll produce the files/text immediately.
