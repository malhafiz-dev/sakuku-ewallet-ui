# Install Guide

## 1. Initialize Project

```bash
npm init -y
```

---

## 2. Install Development Dependencies

```bash
npm install -D tailwindcss @tailwindcss/cli @iconify/tailwind4 @iconify/json browser-sync concurrently prettier prettier-plugin-tailwindcss
```

---

## 3. Setup Tailwind CSS

Buat file:

```
src/input.css
```

Kemudian tambahkan:

```css
@import "tailwindcss";

@plugin "@iconify/tailwind4";
```

> **Catatan:** Jika VS Code menampilkan warning `Unknown at rule @plugin`, buka **Settings (JSON)** lalu tambahkan:

```json
{
  "css.lint.unknownAtRules": "ignore"
}
```

Warning tersebut hanya berasal dari CSS Language Service VS Code dan tidak memengaruhi proses build.

---

## 4. Setup Working Directory

```
project
│
├── dist
│   ├── assets
│   │   ├── css
│   │   ├── img
│   │   └── js
│   └── index.html
│
├── src
│   └── input.css
│
├── package.json
├── .prettierrc
└── Install.md
```

---

## 5. Setup Prettier

Buat file:

```
.prettierrc
```

Isi dengan:

```json
{
  "tabWidth": 2,
  "singleQuote": true,
  "plugins": ["prettier-plugin-tailwindcss"]
}
```

---

## 6. Setup NPM Scripts

Tambahkan pada `package.json`:

```json
"scripts": {
  "dev": "concurrently \"browser-sync start --server dist --files dist --port 3000\" \"npx @tailwindcss/cli -i ./src/input.css -o ./dist/assets/css/main.css --watch\"",
  "build": "npx @tailwindcss/cli -i ./src/input.css -o ./dist/assets/css/main.css --minify"
}
```

---

## 7. Run Development Server

```bash
npm run dev
```

Aplikasi akan berjalan pada:

```
http://localhost:3000
```

---

## 8. Build Production

```bash
npm run build
```

File CSS hasil build akan berada di:

```
dist/assets/css/main.css
```

---

## 9. Using Iconify

Contoh penggunaan icon:

```html
<span class="icon-[lucide--wallet] text-3xl text-blue-600"></span>

<span class="icon-[mdi-light--home] text-2xl text-red-500"></span>

<span class="icon-[tabler--user] text-2xl"></span>
```

Cari koleksi icon di:

https://icon-sets.iconify.design/