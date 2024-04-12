Download tailwindcss.exe to tailwind folder or Install using npm
curl -o tailwindcss.exe -sL https://github.com/tailwindlabs/tailwindcss/releases/latest/download/tailwindcss-windows-x64.exe
npm install -D tailwindcss

# Create a tailwind.config.js file
tailwindcss.exe init
npx tailwindcss init

# Start a watcher
tailwindcss.exe -i ../wwwsys/Content/tailwind/input.css -o ../wwwsys/Content/tailwind/output.css --watch
npx tailwindcss -i ../wwwsys/Content/tailwind/input.css -o ../wwwsys/Content/tailwind/output.css --watch

# Compile and minify your CSS for production 
tailwindcss.exe -i ../wwwsys/Content/tailwind/input.css -o ../wwwsys/Content/tailwind/output.min.css --minify
npx tailwindcss -i ../wwwsys/Content/tailwind/input.css -o ../wwwsys/Content/tailwind/output.min.css --minify

//Update tailwind.config.js

/** @type {import('tailwindcss').Config} */
module.exports = {
    darkMode: 'class'
    content: ["../wwwsys/AppSites/**/*.html"],
    theme: {
        extend: {},
    },
    plugins: [
        require('@tailwindcss/forms'),
        require('@tailwindcss/typography'),
    ]
}
