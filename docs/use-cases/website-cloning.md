# Website Cloning

Ravian AI can **clone entire websites** — downloading structure, content, styling, and assets into your local workspace for analysis, archiving, or repurposing.

Instead of manual screen scraping or complex crawlers, you give Ravian the URL and what you want to capture.

---

## What this capability does

Ravian's website cloning:

- Crawls entire sites or specific sections recursively.
- Downloads HTML, CSS, JS, images, and other assets.
- Preserves folder structure and relative links.
- Extracts content into structured formats (Markdown, JSON) for analysis.
- Handles authentication, pagination, and dynamic content when needed.

!!! note
    Use this for competitive analysis, archiving, or creating offline copies. Respect robots.txt and terms of service.

---

## Typical workflows

Common cloning use cases:

- Competitor site analysis and benchmarking.
- Archiving sites before redesign or shutdown.
- Content migration to CMS or static generators.
- Creating offline references for design teams.

---

## Example: Clone Lovable.dev

Watch Ravian clone the entire [Lovable.dev](https://lovable.dev) website in this demo:

<div style="position: relative; padding-bottom: 56.25%; height: 0; overflow: hidden; max-width: 100%; height: auto;">
  <iframe src="https://www.youtube.com/embed/iG-NDXmf8FQ?si=2Eb-4ivz9a4LboJZ" 
          title="Ravian AI clones Lovable.dev website" 
          frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" 
          referrerpolicy="strict-origin-when-cross-origin" 
          allowfullscreen 
          style="position: absolute; top: 0; left: 0; width: 100%; height: 100%;">
  </iframe>
</div>


**What happens in the demo**

1. **Start the task**  
   You tell Ravian:  
   > *"Clone the Lovable.dev website completely."*

2. **Ravian plans**  
   Ravian shows a step-by-step plan:
   - Analyze homepage  
   - Discover internal pages  
   - Download assets  
   - Preserve structure  

3. **Execution**  
   Ravian browses Lovable.dev, maps the site structure, downloads HTML, CSS, and images, and recreates the folder hierarchy locally.

4. **Result**  
   You receive a complete offline copy with all styling intact — ready for analysis or modification.

---

## How to clone any website

### 1. Open Task Mode and describe your goal

    
    Clone https://example.com completely, including all pages, styles, and images.
    Save everything to my analysis folder.

---

### 2. Review the plan

Ravian will show:

* The discovered sitemap
* Pages it will crawl
* Assets it will download
* Folder structure it will create

Approve the plan when it looks correct.

---

### 3. Execute the task

Ravian crawls the site and saves everything locally.

Example output:

    
    example.com/
    ├── index.html
    ├── css/
    ├── images/
    ├── about/
    └── blog/
        └── 2024/
    

---

### 4. Analyze or extend

You can now ask Ravian:

* *"Analyze this cloned site for design patterns"*
* *"Convert this into static HTML"*
* *"Extract only blog content into Markdown files"*

---

## Pro tips

* **Scope control**
  Add:

  > *"Only pages under /pricing and /features"*
  > to limit crawling.

* **Asset optimization**
  Ask:

  > *"Minify CSS and JS"*
  > *"Optimize images for web"*

* **Content extraction**
  Request:

  > *"Save all content as Markdown files for CMS migration"*

* **Updates**
  Re-run the same task to sync changes from the live site.

---

**Website cloning made simple, reliable, and fully autonomous.**

