# 🚀 GitHub Pages Deployment System

A simple and elegant web interface for deploying and managing websites on GitHub Pages. Create new websites or edit existing ones with just a few clicks!

![GitHub Pages Deployer](https://img.shields.io/badge/Status-Active-success)
![License](https://img.shields.io/badge/License-MIT-blue)

## ✨ Features

- **One-Click Deployment**: Deploy websites to GitHub Pages instantly
- **Easy Editing**: Update existing websites with round-based versioning
- **Clean Interface**: Simple, user-friendly design with minimal input required
- **Real-time Feedback**: Visual loading states and success/error notifications
- **Smart Nonce Management**: Automatic nonce generation and persistence across rounds

## 🎯 Use Cases

- Quickly prototype and deploy web applications
- Create portfolios, landing pages, or project showcases
- Build to-do lists, calculators, or interactive tools
- Iterate on existing projects with easy updates

## 🖥️ Interface

The deployment system features a modern, gradient-themed interface with three simple input fields:

1. **Task Name**: Unique identifier for your project (e.g., `TO_do_list`, `Portfolio_Website`)
2. **Round**: Version control - use `1` for new websites, `2+` for editing existing ones
3. **Brief Description**: Describe what you want to create or modify

## 🚀 Getting Started

### Prerequisites

- A modern web browser (Chrome, Firefox, Safari, or Edge)
- Internet connection

### Usage

1. **Open the Application**: Load the `index.html` file in your browser or visit the hosted URL

2. **Create a New Website** (Round 1):
   - Enter a unique task name (e.g., `My_Portfolio`)
   - Set round to `1`
   - Describe what you want to create
   - Click "🚀 Deploy Website"

3. **Edit an Existing Website** (Round 2+):
   - Enter the same task name as before
   - Set round to `2` or higher
   - Describe the changes you want to make
   - Click "✏️ Update Website"

4. **View Your Website**: After successful deployment, click the "🔗 View Your Website" button

## 📝 Example Requests

### Creating a To-Do List App
```
Task Name: TO_do_list
Round: 1
Brief: Create a beautiful to-do list app with modern UI, dark theme, and task completion animations
```

### Editing the Background Color
```
Task Name: TO_do_list
Round: 2
Brief: Modify this app to make background in red color
```

### Building a Portfolio
```
Task Name: Portfolio_Website
Round: 1
Brief: Build a personal portfolio website with sections for About, Projects, and Contact with smooth scrolling
```

## 🔧 How It Works

The system communicates with a backend API that:

1. Receives your deployment request
2. Generates the website code based on your description
3. Creates/updates a GitHub repository
4. Deploys the site to GitHub Pages
5. Returns the live URL

### API Integration

The frontend sends POST requests to:
```
https://aryan1411-code-generator-api.hf.space/api-endpoint
```

**Request Structure:**
```json
{
  "email": "student2@example.com",
  "secret": "aryan",
  "task": "User's task name",
  "round": 1,
  "nonce": "auto-generated",
  "brief": "User's description",
  "checks": ["Quality checks"],
  "evaluation_url": "https://127.0.0.1:8000/",
  "attachments": []
}
```

## 🎨 Features Breakdown

### Round Management
- **Round 1**: Creates a brand new website with a randomly generated nonce
- **Round 2+**: Edits the existing website using the same nonce from Round 1

### Visual Feedback
- Color-coded badges: Green for "New Website", Orange for "Edit Existing"
- Dynamic button text based on the selected round
- Loading spinner during deployment
- Success messages with direct links to deployed sites
- Clear error messages if deployment fails

### Smart Defaults
Hidden fields are automatically configured:
- Email and authentication credentials
- Quality checks (MIT license, README, display requirements)
- Evaluation URL
- Unique nonce generation

## 🛠️ Technology Stack

- **HTML5**: Structure and semantic markup
- **CSS3**: Modern styling with gradients and animations
- **Vanilla JavaScript**: API communication and DOM manipulation
- **Fetch API**: Asynchronous HTTP requests

## 📱 Responsive Design

The interface is fully responsive and works seamlessly on:
- Desktop computers
- Tablets
- Mobile devices

## 🔒 Security

- All sensitive credentials are handled server-side
- The frontend only exposes necessary user inputs
- HTTPS communication with the backend API

## 🐛 Troubleshooting

**Deployment Failed?**
- Check your internet connection
- Ensure the task name is unique for new projects
- Verify you're using the correct round number
- Make sure your brief description is clear and detailed

**Website Not Loading?**
- GitHub Pages may take a few minutes to propagate
- Try clearing your browser cache
- Verify the URL is correct

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## 👨‍💻 Author

Built with ❤️ by the development team

## 🙏 Acknowledgments

- Backend API powered by Hugging Face Spaces
- Deployed on GitHub Pages
- Inspired by modern deployment platforms

## 📞 Support

If you encounter any issues or have questions:
- Open an issue on GitHub
- Contact the development team
- Check the API documentation

---

**Happy Deploying! 🎉**