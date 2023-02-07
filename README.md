# tailwind-playground

## Installation and Setup

### 1. install tailwind and create configuration file

```shell
npm install tailwindcss@latest --save-dev
npx tailwindcss init
```

### 2. Configure path for any source files that contain Tailwind class names (including html templates, JavaScript components)

```JavaScript
// in tailwind.config.js
module.exports = {
    content: [
        './index.html'
    ]
}
```

### 3. Create a css file and add the Tailwind directives

```css
/* in input.css */
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### 4. Add a script to scan all source files that use Tailwind to build CSS

```JSON
// in package.json
{
    "scripts": {
        "build-css": "npx tailwindcss -i ./css/input.css -o ./css/output.css --watch"
    }
}
```

_now can use tailwind within source files_
