# 📋 Setup Guide - English Adventure App

This guide will help you set up and run the English Adventure app on your local machine and deploy it to GitHub.

## 🎯 Prerequisites

Before you begin, make sure you have:
- **Node.js** (version 14 or higher) - [Download here](https://nodejs.org/)
- **Git** - [Download here](https://git-scm.com/)
- **GitHub Account** - [Sign up here](https://github.com/)
- A code editor like **VS Code** - [Download here](https://code.visualstudio.com/)

## 📥 Local Setup

### Step 1: Download the Project

If you received this as a file, extract it to your desired location.

### Step 2: Open Terminal/Command Prompt

Navigate to the project folder:
```bash
cd path/to/english-adventure-app
```

### Step 3: Install Dependencies

Run this command to install all required packages:
```bash
npm install
```

This will install React and other dependencies. It may take a few minutes.

### Step 4: Start the Development Server

Run:
```bash
npm start
```

The app will automatically open in your browser at `http://localhost:3000`

If it doesn't open automatically, manually navigate to that URL.

### Step 5: Test the App

- Enter your name on the welcome screen
- Try completing activities in Unit 1
- Check if certificates download correctly
- Test all features

## 🚀 Deploying to GitHub

### Step 1: Create a GitHub Repository

1. Go to [GitHub](https://github.com/)
2. Click the **+** icon in the top right
3. Select **"New repository"**
4. Name it: `english-adventure-app`
5. Add description: "Interactive English vocabulary learning app"
6. Choose **Public** or **Private**
7. **DO NOT** initialize with README (we already have one)
8. Click **"Create repository"**

### Step 2: Initialize Git (if not already done)

In your project folder terminal:
```bash
git init
```

### Step 3: Add All Files

```bash
git add .
```

### Step 4: Make Your First Commit

```bash
git commit -m "Initial commit: English Adventure App"
```

### Step 5: Connect to GitHub

Replace `yourusername` with your GitHub username:
```bash
git remote add origin https://github.com/yourusername/english-adventure-app.git
```

### Step 6: Push to GitHub

```bash
git branch -M main
git push -u origin main
```

You'll be prompted for your GitHub username and password (or personal access token).

### Step 7: Verify Upload

Go to your GitHub repository URL:
`https://github.com/yourusername/english-adventure-app`

You should see all your files!

## 🌐 Deploy to GitHub Pages (Optional)

To make your app accessible online:

### Step 1: Install GitHub Pages package

```bash
npm install --save-dev gh-pages
```

### Step 2: Update package.json

Add this line at the top level of your `package.json`:
```json
"homepage": "https://yourusername.github.io/english-adventure-app",
```

Add these to the "scripts" section:
```json
"predeploy": "npm run build",
"deploy": "gh-pages -d build"
```

### Step 3: Deploy

```bash
npm run deploy
```

### Step 4: Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings**
3. Scroll to **Pages** section
4. Under "Source", select **gh-pages** branch
5. Click **Save**

Your app will be live at: `https://yourusername.github.io/english-adventure-app`

## 🔧 Troubleshooting

### "Command not found: npm"
- Install Node.js from https://nodejs.org/

### "Permission denied" errors
- On Mac/Linux, try: `sudo npm install`
- On Windows, run terminal as Administrator

### Port 3000 already in use
- Change port: `PORT=3001 npm start`
- Or kill process using port 3000

### Build errors
- Delete `node_modules` and `package-lock.json`
- Run `npm install` again
- Try `npm start` again

### Certificate download not working
- Check browser settings allow downloads
- Try different browser (Chrome recommended)

## 📱 Mobile Testing

To test on mobile devices on same network:

1. Find your computer's IP address:
   - Windows: `ipconfig`
   - Mac/Linux: `ifconfig`

2. Start the app: `npm start`

3. On mobile browser, go to:
   `http://YOUR_IP_ADDRESS:3000`

## 🎨 Customization

### Change Colors
Edit the color values in `src/App.jsx`:
- Look for `#667eea` and `#764ba2` (main gradient)
- Replace with your preferred colors

### Add More Words
Edit the `courseData` object in `src/App.jsx`:
- Add more vocabulary items to each unit
- Add new units following the same structure

### Change Unit Themes
Modify the `units` array in `courseData`:
- Change `title`, `emoji`, `color`
- Update `vocabulary` arrays

## 📚 Project Structure

```
english-adventure-app/
├── public/              # Static files
│   └── index.html      # HTML template
├── src/                # Source code
│   ├── App.jsx        # Main app component
│   ├── index.js       # Entry point
│   └── index.css      # Global styles
├── package.json       # Dependencies
├── README.md         # Documentation
└── .gitignore        # Git ignore rules
```

## 🤝 Getting Help

If you encounter issues:
1. Check the troubleshooting section above
2. Search for the error message online
3. Open an issue on GitHub
4. Contact: your-email@example.com

## 🎉 Next Steps

Once everything is working:
1. ✅ Test all features thoroughly
2. ✅ Customize colors/content if desired
3. ✅ Share with students
4. ✅ Gather feedback
5. ✅ Make improvements

---

**Happy Teaching! 🎓**
