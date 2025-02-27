---
type: Blog Post
date: 2024-12-24
tags:
  - coding
title: 24-12-2024 Blog Infrastructure
---
# Blog Infrastructure: Streamlining Content Publishing with Obsidian and GitHub Actions
This idea of a blog started when I stumbled upon [Network Chuck's video](https://www.youtube.com/watch?v=dnE7c0ELEH8&ab_channel=NetworkChuck). It was a start to finish on how he set up a blog site using **obsidian**, **HUGO**, and **HOSTINGER**. 

Inspired by this, I tried setting up my own. 

## What Sets My Setup Apart?
Unlike many **"setting up Obsidian blog tutorials"**, including Network Chuck's, I didn’t start from scratch. My blog needed to integrate seamlessly with an already deployed website, requiring custom solutions rather than plug-and-play APIs or plugins. This additional complexity presented both challenges and opportunities.

Could this be the foundation for a SaaS product? Possibly :3 
## Key Features 
- **Integration with an Existing Website**  
    My blog merges directly into my portfolio website rather than operating as a standalone site.
- **Customizable Themes and Aesthetics**  
    Fonts, headings, padding, and overall design are fully customizable to align with the site's branding.
- **Rich Content Support**  
    The blog accommodates images, drawings, and other media types seamlessly.
- **Minimum User Input**
	I want the workflow of writing to deploying to be as frictionless as possible. Ofcourse I can 

## Infrastructure: Automation at Its Core
Here’s how the infrastructure is set up:

1. **Obsidian** is connected to a GitHub repository called **portfolio-blog**.
2. After finishing a blog post in Obsidian, I commit, sync, and push the changes to the repository.
3. This triggers a **GitHub Action**, which sends a POST request webhook to my **portfolio-website** repository.
4. The portfolio repository processes the webhook, verifies the changes, and deploys the updated blog to the production website.

With this setup, most of the workflow is automated, requiring minimal user intervention. GitHub Actions handle the heavy lifting, ensuring the process is smooth and efficient.

![[Pasted image 20250104113300.png]]
## Workflow: Writing and Publishing Made Simple
Thanks to this infrastructure, writing and publishing blog posts is a seamless process. Here’s how it works:
1. **Create a New File**  
    Start a new markdown file in Obsidian under the designated blog directory.
2. **Add Metadata**  
    Include the title, date, and tags for the blog post.
3. **Write the Content**  
    Draft the blog post with text, images, and drawings as needed.
4. **Push the Changes**  
    Commit, sync, and push the updates to GitHub via Obsidian.

The automated pipeline takes over from here, deploying the blog to the live website.
