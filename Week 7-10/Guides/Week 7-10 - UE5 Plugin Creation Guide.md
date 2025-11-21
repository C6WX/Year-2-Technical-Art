# Week 7–10 – UE5 Plugin Creation Guide




## 1. Creating a New Plugin in UE5 (5.6.1)

1. Open your project in **Unreal Engine**.  
2. Go to **`Edit > Plugins`**.  
3. Click **`New Plugin`** (usually at the bottom-right of the Plugins window).  
4. Choose a template:
   - **Recommended:** `Content Only`  *(no C++ required)*.
5. Fill in the details:
   - **Name:** `[TA_YourProjectName_Pack]`  
   - **Category:** `[Technical Art / VFX / Tools]`  
   - **Description:** `[1–2 sentence summary of what the plugin provides]`
6. Click **Create Plugin** and restart the editor if prompted.

Your plugin will now live under a `Plugins/` folder in your project. You will move/duplicate your assets into the plugin's Content folder next.

---

## 3. Organising Content Inside the Plugin

Create a **clean, professional folder structure** inside your plugin. Use this as a starting point and adapt to your project.

Suggested structure:

- `Content/[YourPluginName]/Maps`
- `Content/[YourPluginName]/Blueprints`
- `Content/[YourPluginName]/VFX` or `Niagara`
- `Content/[YourPluginName]/Materials`
- `Content/[YourPluginName]/Meshes`
- `Content/[YourPluginName]/Textures`


1. In the **Content Browser**, navigate to your plugin's Content.  
2. Create folders matching the structure you need.  
3. **Move or duplicate** your finished assets into the plugin folders:
   - Materials / material instances  
   - Niagara systems / emitters  
   - Blueprints / tools  
   - Meshes / textures  
   - Demo maps
4. Right-click the plugin root folder and choose **`Fix Up Redirectors in Folder`**.

---

## 4. Creating a Demonstration Map

Your plugin should ideally contain **a demo map** that shows how to use your assets.

The demo map should:

- Show each **major asset/system** in a simple scene.  
- Use clear layout and basic geometry (focus on the technical art).  
- Include **signposting** (e.g. text renders, simple UI, on-screen instructions).  
- Demonstrate **typical client use** (e.g. ability ability triggers, hit impacts, environment effects).

---

## 5. Preparing the Plugin for Export

Before you export:

- [ ] Check your assets work **inside the plugin**, not from your original `/Game` folders.  
- [ ] Open your demo map from the plugin and test everything.  
- [ ] Remove temporary/testing assets you do not want to ship.

---

## 6. Packaging the Plugin (Exporting for the Client)

1. Open your project with the plugin enabled.  
2. Go to **`Edit > Plugins`**.  
3. Find your plugin in the list (likely under **Project** or **Installed**).
4. In your plugin's panel, click **`Package`** / **`Package Plugin`**.  
5. Choose an **output folder** outside of your project, e.g.:  
   - `.../Builds/Plugins/[YourPluginName]_v1_0_0`  
6. Select target platform(s) (usually `Windows` or `All`).  


When complete, you will have a **packaged plugin folder** ready to send.

---

## 7. Testing the Packaged Plugin in a Fresh Project

To make sure your client can use the plugin easily:

1. Create a **new empty UE5 project** using the same or newer minor version (e.g. 5.6.1).  
2. Close the editor.  
3. Copy your **packaged plugin folder** into the new project's `Plugins/` directory.  
4. Open the new project.  
5. In **`Edit > Plugins`**, check that your plugin appears and is enabled.  
6. Open your demo map from the plugin content and test:
   - Effects, Blueprints, tools, etc.  
   - Any custom UI / interactions.

If anything is missing or broken, fix your original project/plugin and re-package.

---

## 8. Final Export Package for the Client

Your final delivery to the client should include:

- [ ] A **zipped folder** containing the packaged plugin:  
  - File name: `[TA_YourProjectName_Pack_v1_0_0.zip]`  
- [ ] A completed **Handover Document** (see separate template).  
- [ ] Any additional reference images/videos links, if agreed with the client.



