# Capital Caps - Baseball Cap Store

A modern, full-stack e-commerce application for a baseball cap store built with Next.js 15 and Cloudinary. This project demonstrates media literacy best practices for developers, showcasing how to effectively manage and transform images using Cloudinary's powerful API.

> This application supports the "Cloud to Crowd" Media IQ course on Cloudinary Academy, free for all and designed for the Cloudinary Creators Program. Learn more at https://community.cloudinary.com and take the course at https://training.cloudinary.com/learn/course/devrel-c2c-next

## 🚀 Features

- **Product Catalog**: Browse available baseball caps with detailed product pages
- **Cloudinary Integration**: Dynamic image optimization, transformations, and overlays
- **Responsive Design**: Beautiful, mobile-first UI built with Tailwind CSS
- **Admin Panel**: Access admin features and utilities
- **Image Transformations**: Automatic cropping, watermarking, and discount badges
- **Server-Side Rendering**: Fast, SEO-friendly pages with Next.js App Router

## 🛠️ Tech Stack

- **Framework**: Next.js 16+ (App Router)
- **Language**: TypeScript 5
- **Styling**: Tailwind CSS 4
- **Image Management**: Cloudinary & next-cloudinary
- **Deployment**: Netlify
- **Runtime**: React 19+

## 📋 Prerequisites

- Node.js 20+ 
- npm or yarn
- Cloudinary account (free tier works)
- Netlify account (for deployment)
- CodeSandbox account (if you want to try a sandbox rather than a local build)

## 🔧 Local installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd start
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Set up environment variables**

   To run the final version of this app, create a `.env.local` file in the `final` directory with the following variables:

   ```env
   NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME=your_cloud_name
   NEXT_PUBLIC_CLOUDINARY_API_KEY=your_api_key
   CLOUDINARY_API_SECRET=your_api_secret
   NEXT_PUBLIC_CLOUDINARY_UPLOAD_PRESET=baseball-cap-store
   NEXT_PUBLIC_CLOUDINARY_FOLDER_NAME=baseball-cap-store
   ```
   Then, follow step 2 above.

## 🏃 Running the Project

### Development Mode

```bash
npm run dev
```

The application will be available at `http://localhost:3000`

### Production Build

```bash
npm run build
npm start
```

### Linting

```bash
npm run lint
```

## 📁 Project Structure

```
final/
├── app/                    # Next.js App Router pages
│   ├── admin/             # Admin panel pages
│   ├── products/          # Product detail pages
│   └── page.tsx           # Home page
├── components/            # React components
│   ├── ProductCard.tsx    # Product card component
│   └── ProductImage.tsx   # Cloudinary image component
├── lib/                   # Utility libraries
│   ├── cloudinary.ts      # Cloudinary configuration
│   └── data/              # Data files (if needed)
├── products/              # Product data
│   └── products.json      # Product catalog
├── scripts/               # Utility scripts
│   └── add-logo.ts        # Logo upload script
├── types/                 # TypeScript type definitions
└── logo/                  # Logo assets
```

## 🌐 Deployment

### Netlify

This project is configured for Netlify deployment with a `netlify.toml` file in the root directory.

1. **Connect your repository** to Netlify
2. **Set environment variables** in Netlify dashboard:
   - Go to Site settings → Environment variables
   - Add all the variables from your `.env.local` file
3. **Deploy**: Netlify will automatically detect the configuration and deploy from the `final` directory

The `netlify.toml` configuration:
- Base directory: `final`
- Build command: `npm run build`
- Next.js plugin: Automatically enabled

### Environment Variables on Netlify

Make sure to add all environment variables in the Netlify dashboard:
- `NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME`
- `NEXT_PUBLIC_CLOUDINARY_API_KEY`
- `CLOUDINARY_API_SECRET`
- `NEXT_PUBLIC_CLOUDINARY_UPLOAD_PRESET`
- `NEXT_PUBLIC_CLOUDINARY_FOLDER_NAME`

## 🎨 Cloudinary Features

This project demonstrates several Cloudinary capabilities:

- **Automatic Image Optimization**: Format and quality optimization
- **Smart Cropping**: Automatic gravity-based cropping (`g_auto`)
- **Overlays**: Logo watermarking on product images
- **Dynamic Transformations**: Discount badges and text overlays
- **Responsive Images**: Automatic sizing and format selection

## 📝 Available Scripts

- `npm run dev` - Start development server with Turbopack
- `npm run build` - Build for production with Turbopack
- `npm run start` - Start production server
- `npm run lint` - Run ESLint

## 🔍 Key Files

- `app/page.tsx` - Home page with product listing
- `app/products/[id]/page.tsx` - Individual product detail page
- `components/ProductImage.tsx` - Cloudinary image component with transformations
- `lib/cloudinary.ts` - Cloudinary SDK configuration
- `next.config.ts` - Next.js configuration with file tracing for products.json
- `netlify.toml` - Netlify deployment configuration

## 🐛 Troubleshooting

### Product pages show server error on Netlify

The `products.json` file is configured to be included in the build via `next.config.ts`. If you still encounter issues:

1. Verify the file path in `next.config.ts` matches your file structure
2. Check that `outputFileTracingIncludes` is correctly configured
3. Ensure the `products` directory is committed to your repository

### Cloudinary images not loading

1. Verify all environment variables are set correctly
2. Check that the upload preset exists in your Cloudinary dashboard
3. Ensure product images are uploaded to the correct folder in Cloudinary
4. Run `npm run init` to upload the logo if it's missing

### Build fails on Netlify

1. Check that all environment variables are set in Netlify dashboard
2. Verify the base directory in `netlify.toml` is correct (`final`)
3. Ensure Node.js version is 20+ in Netlify build settings

## 📚 Learn More

- [Next.js Documentation](https://nextjs.org/docs)
- [Cloudinary Documentation](https://cloudinary.com/documentation)
- [next-cloudinary Documentation](https://next-cloudinary.dev/)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)

## 📄 License

This project is part of our 'Cloud to Crowd' course on media literacy for developers.

---

Built with ❤️ using Next.js by the Cloudinary Developer Relations Team

