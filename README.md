Secure Time-Limited File Sharer

A secure, ephemeral file sharing application built with HTML, JavaScript, and Supabase. Upload files, generate shareable links, and rest easy knowing your data automatically expires or "self-destructs" after a set time or download limit.

🚀 Features

⏱️ Time-Based Expiration: Links automatically become invalid after a user-selected duration (e.g., 1 hour, 24 hours).

🔢 Download Limits: Set a maximum number of downloads (e.g., "Burn after 1 read").

🔒 Secure Storage: Files are stored securely in Supabase Storage with signed URLs.

🔑 Password Protection: (Optional) Add an extra layer of security with password-protected links.

📱 Responsive Design: Works seamlessly on mobile and desktop devices.

🛠️ Tech Stack

Frontend: HTML5, CSS3, JavaScript (ES6+)

Styling: Tailwind CSS (via CDN)

Backend: Supabase (PostgreSQL Database)

Storage: Supabase Storage

💻 Getting Started

Since this is a standalone HTML application, you don't need to install any Node modules. You can run it directly in your browser.

Prerequisites

A modern web browser (Chrome, Firefox, Edge, etc.)

A Supabase account

Installation & Setup

Clone or Download the Repository

git clone 
cd secure-file-share


Configure Supabase Keys

Because this is a client-side app without a build process, you need to add your keys directly to the code.

Open index.html in your text editor (VS Code).

Scroll down to the script section (around line 140).

Find the configuration block and paste your keys:

// --- CONFIGURATION ---
// REPLACE THESE WITH YOUR ACTUAL SUPABASE KEYS

const supabaseUrl = "[https://your-project-id.supabase.co](https://your-project-id.supabase.co)";
const supabaseKey = "your-public-anon-key";

// --- CONSTANTS ---
const BUCKET_NAME = "uploads"; 
const TABLE_NAME = "files";


Run the App

Simply double-click index.html to open it in your browser.

Note: For the best experience (and to avoid CORS issues with some features), it is better to serve it using a local server extension (like "Live Server" in VS Code) rather than opening the file directly.

🗄️ Supabase Setup

To make the app work, you need to configure your Supabase project:

Create a Storage Bucket:

Go to Storage and create a new public bucket named uploads.

Create a Database Table:
Run the required SQL in your Supabase SQL Editor to create the files table:

Set up Row Level Security (RLS):

Enable RLS on the files table.

Add a policy to allow INSERT for everyone (Anon).

Add a policy to allow SELECT for everyone (Anon).

🤝 Contributing

Contributions are welcome!

Fork the project

Create your Feature Branch

Commit your Changes

Push to the Branch

Open a Pull Request

📄 License

This project is licensed under the MIT License.
