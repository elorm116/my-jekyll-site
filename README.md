# my-jekyll-site
Jekyll GitHub Pages Site with Admin Access
This is a simple Jekyll application configured to work with GitHub Pages and includes admin access control features.

Setup Instructions
1. Create a New Repository
Go to GitHub and create a new repository
Name it something like my-jekyll-site
Make sure it's public (required for free GitHub Pages)
Initialize with a README

2. Add Files to Repository
Copy all the files from the artifacts into your repository:

_config.yml - Site configuration
Gemfile - Ruby dependencies
index.html - Main page
admin.html - Admin dashboard
_posts/2024-01-01-welcome.md - Sample post
.github/workflows/pages.yml - GitHub Actions workflow

3. Configure Your Site
Edit _config.yml:
Change url to https://yourusername.github.io
Change baseurl to /your-repo-name
Update admin_users with GitHub usernames who should have admin access
Create the _posts directory and add your first post

4. Enable GitHub Pages
Go to your repository settings
Navigate to "Pages" in the left sidebar
Under "Source", select "GitHub Actions"
The workflow will automatically deploy your site

5. Add Admin Users
To add people with admin access:

Repository Collaborators: Go to Settings > Collaborators and add users
Admin Users: Edit _config.yml and add their GitHub usernames to admin_users
Admin Features
Admin users can:

Access the admin dashboard at /admin
Create new posts directly from GitHub
Edit site configuration
Manage repository collaborators
View site statistics
File Structure
your-repo/
├── _config.yml
├── Gemfile
├── index.html
├── admin.html
├── _posts/
│   └── 2024-01-01-welcome.md
├── .github/
│   └── workflows/
│       └── pages.yml
└── README.md
Adding New Posts
Go to your repository on GitHub
Navigate to _posts directory
Click "Add file" > "Create new file"
Name it: YYYY-MM-DD-title.md
Add front matter and content
Commit the changes
Managing Access
Repository Level Access:
Admin: Full control over repository and site
Write: Can push changes and manage issues/PRs
Read: Can view repository and clone
Site Admin Access:
Controlled by the admin_users list in _config.yml
Users must be in this list to access /admin page
Can be different from repository collaborators
Customization
Edit _config.yml for site settings
Modify index.html and admin.html for layout changes
Add new pages by creating HTML/Markdown files
Customize styling in individual pages or create a _sass directory
Deployment
The site automatically deploys when you push to the main branch using GitHub Actions. Check the "Actions" tab in your repository to see deployment status.

Troubleshooting
Site not loading: Check GitHub Actions for build errors
Admin features not working: Verify usernames in admin_users match exactly
404 errors: Check baseurl in _config.yml matches your repository name
Local Development
To run locally:

bash
bundle install
bundle exec jekyll serve
Visit http://localhost:4000 to see your site.

