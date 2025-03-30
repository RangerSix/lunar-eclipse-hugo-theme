Welcome.
You probably are saying why do it this way? I can use a ready made theme or even use AI to make a theme.
This is true, but if you use a ready made theme, it want be yours and you will probably have to sacrifice something you want in your theme.
Using AI, I find is never right. Spent more time with errors than blogging. 
This way you get to build the house the way you want it, I'm just giving you the foundation.
And perhaps we both can learn something. lol..


---

# Hugo Blog Website Guide for Windows 11

This guide shows you how to build a customized Hugo blog/website from the ground up. Rather than using a pre-made theme, you’ll learn how to set up your project and integrate your own design touches—a process that not only creates a unique site but also helps you learn more.

> _Remember: The process may be challenging at times, but it’s an excellent opportunity to understand the inner workings of your website._

---

## 1. Prerequisites

Before getting started, make sure your Windows 11 system has the following tools installed:

- **Windows PowerShell**
- **Visual Studio Code (VS Code)** – readily available via the [Windows Store](https://www.microsoft.com/store/apps) or from the official website.
- **Git for Windows** – available at [gitforwindows.org](https://gitforwindows.org) for a robust version.
- **Go Programming Language** – download and install from [go.dev](https://go.dev/doc/install).
- **Hugo** – download the extended version from the [Hugo GitHub releases page](https://github.com/gohugoio/hugo/releases/tag/v0.145.0). Look for:
  - `hugo_extended_0.145.0_windows-amd64.zip`

*Note: Detailed installation instructions aren’t provided here; ensure each tool is installed and added to your system’s PATH.*

---

## 2. Verifying Your Environment

Open PowerShell and check that each tool is working properly by running:

```powershell
git version
go version
hugo version
```

Each command should return version details with no errors. If they do, you're ready to build your site.

---

## 3. Creating Your New Hugo Site

1. **Choose Your Location**  
   Open PowerShell and navigate (`cd`) to the folder where you want your website. (Tip: Avoid creating your site inside a OneDrive folder to prevent syncing issues.)

2. **Create a Directory for Your Site**  
   For example, create a folder named `myhugosite` and navigate into it:
   ```powershell
   mkdir myhugosite
   cd myhugosite
   ```

3. **Generate the Site**  
   Run the following command—replace `yoursitename` with your desired site name:
   ```powershell
   hugo new site yoursitename
   ```
   This creates a new folder named after your site. Navigate into the folder:
   ```powershell
   cd yoursitename
   ```

---

## 4. Installing the Theme

You have two options to install your theme, **lunar-eclipse** in this example:

### Option 1: Manual Installation

1. **Download the Theme**  
   Click the green “Code” button on the theme’s GitHub repository and download the ZIP file.

2. **Extract and Rename**  
   - Extract the ZIP file.
   - Locate the folder (e.g., `lunar-eclipse-hugo-theme-main`), then rename the inner folder to `lunar-eclipse`.
   - Confirm the folder now contains the necessary files: `theme.toml`, `config.toml`, `README.md` and directories `static` and `layouts`.

3. **Move the Theme into Your Site**  
   Copy or move the folder `lunar-eclipse` into the `themes` directory of your Hugo site.

### Option 2: Using Git Submodule

1. **Add the Submodule**  
   In your site’s root directory, run:
   ```powershell
   git submodule add https://github.com/RangerSix/lunar-eclipse-hugo-theme.git themes/lunar-eclipse
   ```

Either method will install the theme into your site’s `themes` folder.

---

## 5. Testing the Basic Theme Setup

1. **Run the Local Server**  
   In the root of your Hugo site, execute:
   ```powershell
   hugo server -t lunar-eclipse
   ```
   The `-t` flag tells Hugo to use the `lunar-eclipse` theme.

2. **View Your Site**  
   Open your browser and type:
   ```
   localhost:1313
   ```
   You should see the site rendered with the basic lunar-eclipse theme.

3. **Stop the Server**  
   Press `Ctrl + C` in PowerShell when you’re finished viewing.

---

## 6. Creating and Publishing a Post

1. **Create a New Post**  
   In PowerShell (ensure you’re in the root of your site), type:
   ```powershell
   hugo new posts/postname.md
   ```
   Replace `postname` with your chosen title. A file appears at `content/posts/postname.md`.

2. **Edit the Post**  
   Open the new file in VS Code. In the front matter at the top:
   - Change:  
     `draft: true` → `draft: false`
   - Update the `title` field as desired.
   - Write your post content below the front matter.
   - Save the file.

3. **Update Site Configuration**  
   Open `hugo.toml` (located in your site’s root) in VS Code. Add or update the following entries:
   ```toml
   title = "Your Site Title"
   theme = "lunar-eclipse"
   ```
   Save your changes.

4. **Build the Site and Test Your Post**  
   In PowerShell:
   ```powershell
   hugo            # Build the site, including the new post
   hugo server     # Launch the local server
   ```
   Browse to `localhost:1313` to ensure your post appears. Stop the server with `Ctrl + C` when done.

---

## 7. Customizing Your Theme

To truly make the theme your own:

1. **Locate the Stylesheet**  
   Navigate to:
   ```
   themes/lunar-eclipse/static/css/styles.css
   ```
2. **Edit the CSS**  
   Open `styles.css` in VS Code and adjust colors, fonts, and layouts to fit your style.
3. **Review Changes**  
   Save your changes and run:
   ```powershell
   hugo server
   ```
   Refresh your browser to see your modifications in real time.

---

## Final Thoughts and Next Steps

By following these steps, you've built the foundation for a fully customized Hugo website. The process not only results in a site uniquely tailored to your tastes but also deepens your understanding of web development practices.

**Additional Enhancements to Explore:**

- **Continuous Deployment:** Automate updates using tools like GitHub Actions for deploying to hosting platforms such as Netlify or Vercel.
- **Feature Expansion:** Integrate features powered by AI or additional Hugo components, such as taxonomies, menus, and shortcodes.
- **SEO and Performance:** Look into Hugo’s built-in SEO practices and performance tweaks to optimize your site.

Happy Coding!

--- 



 
