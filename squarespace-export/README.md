# Squarespace Integration Guide for Apexia Learning

This guide explains step-by-step how to bring your clean, professional Apexia Learning design into your Squarespace website.

---

## 📁 Files Prepared in `squarespace-export/`

1. **`01-header-code-injection.html`**: Google Fonts & script initialization.
2. **`02-squarespace-custom-css.css`**: Complete brand design system (colors, typography, grid, cards, responsive layouts).
3. **`03-page-code-block.html`**: Clean HTML content for your Squarespace page.
4. **`04-footer-code-injection.html`**: Smooth interactions, mobile menu, and dynamic elements.

---

## 🚀 Step-by-Step Instructions

### Step 1: Add Custom CSS to Squarespace
1. Log into your **Squarespace Dashboard**.
2. Go to **Website** → scroll down to **Website Tools** → select **Custom CSS**.
3. Open `squarespace-export/02-squarespace-custom-css.css`, copy everything, paste it into the Custom CSS box, and click **Save**.

### Step 2: Add Header Code Injection
1. In **Website Tools**, click **Code Injection**.
2. In the **Header** section, copy and paste the contents of `squarespace-export/01-header-code-injection.html`.

### Step 3: Add Footer Code Injection
1. Still in **Code Injection**, scroll down to the **Footer** section.
2. Copy and paste the contents of `squarespace-export/04-footer-code-injection.html`.
3. Click **Save** in the top left.

### Step 4: Add the Content via a Code Block
1. Go to **Website** → select the Page you want to edit (e.g., Home or a new blank page).
2. Click **Edit** on the page.
3. Click **Add Section** → choose **Add a blank section**.
4. In that section, click **Add Block** and select **Code** (`</>`).
5. Open the block settings, make sure **HTML** is selected and **Display Source** is turned **OFF**.
6. Copy the entire contents of `squarespace-export/03-page-code-block.html` and paste it inside the Code Block.
7. Click **Done** → **Save**.

---

## ⚡ Handling Images and Assets

1. Upload the brand images from `assets/illustrations/` and `assets/brand/` to Squarespace:
   - In Squarespace, go to any page, click any image block or Link editor → **Files** → **Upload File**.
   - Copy the uploaded file URL (e.g. `https://static1.squarespace.com/static/.../elearning.svg`).
2. In `03-page-code-block.html`, simply replace the local paths `assets/...` with your Squarespace-hosted image URLs if they are not already hosted externally.

---

## 📦 What About the Heavy 1GB+ Articulate Course Demos?
Squarespace does not host multi-gigabyte zipped SCORM/HTML5 runtimes.
To show live interactive Articulate courses inside your Squarespace site:
1. Deploy the `demos/` directory to **Netlify** or **Vercel** (drag-and-drop the folder for free).
2. Add an **Embed Block** or `<iframe>` in Squarespace pointing to your demo URL:
   ```html
   <iframe src="https://your-demos-site.netlify.app/change-management/" style="width:100%; height:700px; border:none; border-radius:12px;"></iframe>
   ```
