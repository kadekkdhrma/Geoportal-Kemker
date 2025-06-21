# SIPUTIH

## Setup
```
npm install --legacy-peer-deps
```

## Development
```
npm run dev
```

## Deployment
Create /dist directory, contains files and /dist/assets contains bundled src files (index.html, js, css).
```
npm run build
```
Create .htaccess at root (ensures react refresh page)
```
RewriteEngine On
RewriteBase /

# Skip the rewrite rule if the file exists (to prevent breaking static files like JSON)
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d

# Redirect everything else to index.html
RewriteRule ^(.*)$ /index.html [QSA,L]
```