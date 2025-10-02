## 📁 Cấu trúc Project - Student Management App

1. Tạo Project React
   bash# Tạo project mới với Vite (nhanh hơn Create React App)
   npm create vite@latest student-management -- --template react
   cd student-management

# Hoặc dùng Create React App

npx create-react-app student-management
cd student-management 2. Cài đặt Dependencies
bash# Cài Tailwind CSS
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p

# Cài Lucide React (icons)

npm install lucide-react 3. Cấu trúc thư mục
student-management/
├── public/
├── src/
│ ├── App.jsx # Component chính (paste code từ artifact)
│ ├── App.css # CSS tùy chỉnh (nếu cần)
│ ├── index.css # Tailwind imports
│ └── main.jsx # Entry point
├── tailwind.config.js # Cấu hình Tailwind
├── package.json
└── vite.config.js (hoặc react config) 4. File cần tạo/sửa
tailwind.config.js
javascript/** @type {import('tailwindcss').Config} \*/
export default {
content: [
"./index.html",
"./src/**/\*.{js,ts,jsx,tsx}",
],
theme: {
extend: {},
},
plugins: [],
}
src/index.css
css@tailwind base;
@tailwind components;
@tailwind utilities;

/_ Custom styles nếu cần _/
body {
margin: 0;
font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen',
'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue',
sans-serif;
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale;
}

-   {
    box-sizing: border-box;
    }
    src/main.jsx (Vite)
    javascriptimport React from 'react'
    import ReactDOM from 'react-dom/client'
    import App from './App.jsx'
    import './index.css'

ReactDOM.createRoot(document.getElementById('root')).render(
<React.StrictMode>
<App />
</React.StrictMode>,
)
src/index.js (Create React App)
javascriptimport React from 'react';
import ReactDOM from 'react-dom/client';
import './index.css';
import App from './App';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
<React.StrictMode>
<App />
</React.StrictMode>
);
src/App.jsx
Copy toàn bộ code từ artifact "Ứng Dụng Quản Lý Học Sinh" 5. Chạy Project
bash# Development
npm run dev # Vite

# hoặc

npm start # Create React App

# Build production

npm run build 6. Mở trình duyệt

Vite: http://localhost:5173
Create React App: http://localhost:3000

7. Deploy (Optional)
   Vercel (Khuyên dùng - Miễn phí)
   bashnpm install -g vercel
   vercel
   Netlify
   bashnpm run build

# Kéo thả folder dist (Vite) hoặc build (CRA) vào netlify.com

📝 Lưu ý

Tailwind CSS cung cấp tất cả styles (không cần CSS riêng)
Lucide React cung cấp icons đẹp
Google Apps Script URL đã được config sẵn trong code
Mở Console (F12) để xem log debug

🎨 Tùy chỉnh màu sắc (Optional)
Nếu muốn đổi màu chủ đạo, sửa trong tailwind.config.js:
javascripttheme: {
extend: {
colors: {
primary: '#4f46e5', // Indigo
secondary: '#06b6d4', // Cyan
}
},
}
Rồi thay các class bg-indigo-600 → bg-primary trong code.

## Commit lên github

1. D:\Git\cmd\git.exe status -- Xem các file đã chỉnh sửa
2. D:\Git\cmd\git.exe add . -- Thêm tất cả các file đã chỉnh sửa / mới tạo vào staging area
3. D:\Git\cmd\git.exe commit -m "noi dung" -- commit lên local
4. D:\Git\cmd\git.exe push origin main -- Push lên GitHub
