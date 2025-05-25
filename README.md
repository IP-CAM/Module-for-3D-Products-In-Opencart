# Product 3D Control for OpenCart

This module integrates **Three.js** with OpenCart to add 3D model support on product pages. It provides both **admin-side configuration** and **front-end rendering**, allowing store owners to associate 3D models with products for an interactive viewing experience.

> ⚠️ This module is experimental and intended as a starting point for integrating Three.js into OpenCart. It's functional, but not yet polished — improvements are planned.

---

## 📦 Module File

`product3dcontrol.ocmod.zip`

Install via the built-in OpenCart Extension Installer.

---

## 🛠 Features

- Adds a custom 3D viewer to product pages using [Three.js](https://threejs.org/).
- Admin interface to configure and upload 3D models per product.
- Dual-language support: **English** and **Greek**.
- Lightweight and designed to be easily extended or customized.
- Includes geometry subtraction tools for basic shape manipulation.

---

## 🧩 Compatibility

- ✅ Tested on **OpenCart 3.0.3.3**
- 🚧 Should work on most **3.x versions** prior to OpenCart 4
- ❌ Not compatible with OpenCart 4.x (yet)

---

## 🌐 Languages

- English (en-gb)
- Greek (el-gr)

---

## 📂 Installation

1. Log in to your OpenCart admin panel.
2. Go to **Extensions → Extension Installer**.
3. Upload `product3dcontrol.ocmod.zip`.
4. Refresh the modifications (Extensions → Modifications → Refresh).
5. Navigate to **Extensions → Modules**, locate **Product 3D Control**, and install it.
6. Configure the module from the admin panel.

---

## 🧾 Instructions

### Test Product

After installation, a test product will be added automatically:
- **Name**: `TEST PRODUCT`
- **SKU**: `TEST3DPRODUCT`

Visit the product in the front end:
- A **3D View** tab appears next to the description.
- You can **rotate** the model with your mouse and **zoom in/out**.

> ⚠️ If the 3D model doesn’t load:
>
> Move the file manually from:
> ```
> /image/catalog/extension/module/product3dcontrol/products/test/test_model.glb
> ```
> To:
> ```
> /image/catalog/extension/module/product3dcontrol/products/{TEST_PRODUCT_ID}/test_model.glb
> ```

---

### Admin Panel Usage

Go to: **Catalog → Product 3D Create**

1. Search for the product you want to create a 3D model for.
2. Click the **edit** icon.
3. On the edit page:
   - You'll see product info (title, description, images).
   - Below that, the **Three.js Editor** is embedded.

#### Reference Images

- You can select up to **4 product images**.
- Click **"Add To Project"** to use them in the editor as reference material.

---

### Saving Models

When you use:

File → Export GLB
- The model is saved automatically to:/image/catalog/extension/module/product3dcontrol/products/{PRODUCT_ID}/{RANDOM_NAME}.glb
- The filename is randomized to prevent scraping based on predictable product IDs.

---

### Subtracting Geometry (Custom Feature)

This module supports a basic geometry subtraction operation:

**Example: Make a sphere with a square hole**
1. Add a **sphere** and a **cube**.
2. Position the cube to intersect the sphere.
3. Select the **target shape** (e.g., the sphere).
4. Then select the **cutting shape** (e.g., the cube).
5. Press `Ctrl + P` to subtract the cube from the sphere.

---

### Front-End Buttons

Above the product name in the front end:
- **ADMIN**: Opens the product's admin edit page.
- **FRONT**: Returns to the product's front-end view.

---

## 📈 Roadmap / TODO

- Improve UI/UX for 3D controls.
- Add support for more model formats.
- Implement more robust error handling.
- Improve mobile responsiveness.
- Add a way to load any previously made or saved 3D model to the editor.
- Save old versions of 3D models and select which one the user sees, or allow multiple 3D models for products with multiple parts.
---

## 📄 License

This module is open-sourced under the [MIT License](LICENSE).

---

## 🤝 Contributions

Feel free to fork, submit pull requests, or open issues.

---

## 📧 Contact

For questions or suggestions, open an issue here on GitHub.
