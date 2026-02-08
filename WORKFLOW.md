# 🛠️ Asset Processing Workflow

This document outlines the professional standards and technical steps followed to prepare every asset in this repository. Our goal is to provide high-quality visuals with the smallest possible footprint for a fast, modern web experience.

## 1. Selection & Verification

* **Platform Sourcing**: Assets are selected from trusted open-license platforms (Pexels, Pixabay, NASA).
* **License Check**: We verify that each asset is free for commercial and personal use before it enters our pipeline.
* **Aesthetic Alignment**: Images are chosen based on their relevance to the blog's content categories, such as Physics or Mathematics.

## 2. Technical Processing

We use a "Performance-First" approach to image processing.

* **Format Conversion**: Standard formats (JPEG/PNG) are converted to **AVIF**. This next-gen format provides superior compression compared to WebP and traditional formats, ensuring faster page loads.
* **Optimization Tooling**: We primarily use **Squoosh.app** for its advanced codecs and manual control.
* **Compression Settings**:
* **AVIF**: We target a quality setting between 30-50, which often reduces file size by 50-80% without noticeable visual loss.
* **Resizing**: Images are scaled to a maximum width of 1920px (for heroes) or 1200px (for post content) to avoid serving unnecessary pixels.


* **Metadata Management**: All non-essential EXIF data is stripped to minimize file size.

## 3. Naming Conventions (SEO)

To ensure the repository is easy to navigate and assets are SEO-friendly, we follow a strict naming convention:

* **Format**: `[post-slug]-[description].[extension]`
* **Rules**:
* Lowercase only.
* No spaces (use hyphens instead).
* Descriptive but concise (e.g., `quantum-mechanics-cat.avif`).



## 4. Deployment via CDN

* **Versioning**: Assets are tagged and pushed to GitHub.
* **Delivery**: We utilize **jsDelivr** as our global Content Delivery Network (CDN). This allows our blog to fetch images from the nearest global edge server, significantly reducing latency.
