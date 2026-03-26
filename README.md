🖼️ Logo Card Studio

Logo Card Studio is a privacy-first, browser-based utility designed to batch-convert inconsistent logos into uniform, high-quality 400x400 square cards. It automatically trims whitespace, centers the content with smart padding, and applies a modern rounded-corner aesthetic.

✨ Features

Auto-Trim Engine: Scans image pixels to find the true bounding box of your logo, eliminating messy whitespace or transparent margins.

Proportional Scaling: Ensures logos are never stretched. It calculates the optimal fit based on the largest dimension to maintain original aspect ratios.

Batch Processing: Drop dozens of logos at once and process them simultaneously.

Live Customization: Adjust internal padding and corner roundness with real-time previews.

Privacy-First: All processing happens locally in your browser using the HTML5 Canvas API. Your images are never uploaded to a server.

One-Click Export: Bundles all processed cards into a single .zip file for easy downloading.

🚀 How to Use

Open the App: Launch index.html in any modern web browser.

Configure: Use the sliders to set your preferred Internal Padding (breathing room) and Corner Radius.

Upload: Drag and drop your logo files (PNG, JPG, WebP, SVG) onto the drop zone or click to browse.

Preview: Instantly view the generated 400x400 cards in the grid.

Download: Click Download All (.zip) to save your new assets.

🛠️ Technical Details

Smart Trimming Algorithm

The app uses a custom getBoundingBox function that iterates through the image's pixel data (ImageData). it identifies the boundaries of the non-transparent and non-white pixels to create a tight crop around the actual logo content.

Canvas Processing

Source Scaling: Calculates a scale factor based on the safeArea (400px minus the user-defined padding).

Clipping Mask: Uses ctx.roundRect() and ctx.clip() to ensure the white background and logo content perfectly match the desired corner radius.

Centering: Mathematical offsets are applied to ensure the logo is perfectly centered regardless of its original aspect ratio.

📦 Local Development

Since this is a client-side application, there is no complex setup required.

Clone the repository:

git clone [https://github.com/yourusername/logo-card-studio.git](https://github.com/yourusername/logo-card-studio.git)


Open index.html in your browser.

📚 Dependencies

Tailwind CSS - For modern UI styling.

JSZip - For client-side ZIP generation.

Lucide Icons (SVG) - For UI iconography.

📄 License

This project is open source and available under the MIT License.