SpinShelf website update: "Improved Concept & 3D Model" section

Copy these into the everyday-reach repo root, replacing the existing files:
  index.html            (adds the #model3d section after Prototyping and a "3D Model" nav link)
  styles.css            (adds .model-frame and .sketch-grid--wide rules at the end)
  assets/wk12/          (new folder: spinshelf-3d.html, concept views, storyboard)

Then commit and push to main. Vercel redeploys automatically.

These files are based on commit 505356e of main. If index.html or styles.css changed
after that, apply 0001-*.patch with `git am` instead of overwriting.
