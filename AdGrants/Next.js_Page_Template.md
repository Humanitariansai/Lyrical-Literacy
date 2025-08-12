# Next.js Page Template

This repository contains a reusable page template for Next.js applications. The template provides a consistent structure for creating new pages with a hero section, content sections, and resources.

## 📋 Features

- **Hero Section** with embedded video
- **Structured Content Sections** with responsive layout
- **Resources Section** with links to external sites
- **Social Media Links** in a clean, organized footer
- **Responsive Design** that works on all device sizes
- **Dark Mode Compatible** with appropriate styling classes

## 🚀 Usage

1. Copy the template code below
2. Create a new file in your Next.js project's `pages` or `app` directory
3. Paste the template code
4. Customize the content, headings, and links to match your needs

## 📄 Template Code

```jsx
import type { Metadata } from "next";
import Link from "next/link";
import PrimaryButton from "@/components/ui/primary-button";
import SecondaryButton from "@/components/ui/secondary-button";

export const metadata: Metadata = {
  title: "Template Page",
  description: "A template for creating new pages",
};

export default function TemplatePage() {
  return (
    <div className="container px-4 md:px-6 mx-auto py-12">
      <div className="max-w-4xl mx-auto">
        {/* ===== HERO SECTION ===== */}
        <div className="mb-16">
          <h1 className="text-4xl md:text-5xl font-bold mb-6">Template Page Title</h1>
          <p className="text-xl text-muted-foreground mb-8">
            This is a template page that you can use as a starting point for creating new pages. It includes a hero section with a video, placeholder sections for content, and a resources section.
          </p>
          <div className="relative w-full aspect-video rounded-lg overflow-hidden mb-8">
            <iframe
              className="absolute top-0 left-0 w-full h-full"
              src="https://www.youtube.com/embed/videoseries?si=caS7A9UMCFewuuRB&amp;list=PLgOGgHS58rB-sBjm4oEfMfFXcYZf89IDo"
              title="YouTube video player"
              allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
              referrerPolicy="strict-origin-when-cross-origin"
              allowFullScreen
            />
          </div>
        </div>

        {/* ===== MAIN CONTENT ===== */}
        <div className="grid gap-12">
          {/* ===== PLACEHOLDER SECTION 1 ===== */}
          <section>
            <h2 className="text-3xl font-bold mb-6">Section 1 Title</h2>
            <div className="prose prose-lg dark:prose-invert max-w-none">
              <p>
                This is a placeholder for your first section. You can replace this with actual content when creating a new page. Include paragraphs, lists, images, or any other content you need.
              </p>
              
              <p>
                You can add multiple paragraphs to provide detailed information. This template ensures consistent styling and layout across different pages.
              </p>
              
              <ul>
                <li>List item one</li>
                <li>List item two</li>
                <li>List item three</li>
              </ul>
            </div>
          </section>

          {/* ===== PLACEHOLDER SECTION 2 ===== */}
          <section>
            <h2 className="text-3xl font-bold mb-6">Section 2 Title</h2>
            <div className="prose prose-lg dark:prose-invert max-w-none">
              <p>
                This is a placeholder for your second section. You can have as many sections as needed for your content. Each section is separated with appropriate spacing.
              </p>
              
              <p>
                Consider using different content formats in different sections to keep your page visually interesting. Options include:
              </p>
              
              <div className="grid md:grid-cols-2 gap-6 my-8">
                <div className="p-6 bg-muted/50 rounded-lg">
                  <h3 className="text-xl font-bold mb-4">Card Title 1</h3>
                  <p className="text-muted-foreground">
                    This is example card content. You can use cards to present information in a visually distinct way.
                  </p>
                </div>
                
                <div className="p-6 bg-muted/50 rounded-lg">
                  <h3 className="text-xl font-bold mb-4">Card Title 2</h3>
                  <p className="text-muted-foreground">
                    This is example card content. Cards work well for presenting related pieces of information side by side.
                  </p>
                </div>
              </div>
            </div>
          </section>

          {/* ===== RESOURCES SECTION ===== */}
          <section>
            <h2 className="text-3xl font-bold mb-6">Further Resources</h2>
            <div className="flex flex-col sm:flex-row gap-4 flex-wrap">
              <PrimaryButton href="https://github.com/Humanitariansai/">
                GitHub Repository
              </PrimaryButton>
              <SecondaryButton href="https://www.youtube.com/@humanitariansai">
                YouTube Channel
              </SecondaryButton>
              <SecondaryButton href="https://www.humanitarians.ai/">
                Official Website
              </SecondaryButton>
            </div>
            
            <div className="mt-8 text-center">
              <h3 className="text-lg font-semibold mb-2">Connect with Humanitarians AI</h3>
              <div className="flex flex-wrap justify-center gap-4 mt-4">
                <a 
                  href="https://www.linkedin.com/company/105696953/"
                  target="_blank"
                  rel="noopener noreferrer"
                  className="text-sm text-primary hover:underline"
                >
                  LinkedIn
                </a>
                <a 
                  href="https://www.youtube.com/@humanitariansai"
                  target="_blank"
                  rel="noopener noreferrer"
                  className="text-sm text-primary hover:underline"
                >
                  YouTube
                </a>
                <a 
                  href="https://www.humanitarians.ai/"
                  target="_blank"
                  rel="noopener noreferrer"
                  className="text-sm text-primary hover:underline"
                >
                  Website
                </a>
                <a 
                  href="https://github.com/Humanitariansai/"
                  target="_blank"
                  rel="noopener noreferrer"
                  className="text-sm text-primary hover:underline"
                >
                  GitHub
                </a>
                <a 
                  href="https://music.apple.com/us/artist/humanitarians-ai/1781414009"
                  target="_blank"
                  rel="noopener noreferrer"
                  className="text-sm text-primary hover:underline"
                >
                  Apple Music
                </a>
                <a 
                  href="https://open.spotify.com/artist/3cj3R4pDpYQHaWx0MM2vFV"
                  target="_blank"
                  rel="noopener noreferrer"
                  className="text-sm text-primary hover:underline"
                >
                  Spotify
                </a>
              </div>
            </div>
          </section>
        </div>
      </div>
    </div>
  );
}
```

## 🛠️ Requirements

This template requires:

1. A Next.js project (13.4+ recommended for app router support)
2. TailwindCSS setup in your project
3. Two custom components:
   - `PrimaryButton`
   - `SecondaryButton`

## 📦 Custom Component Implementation

If you don't already have the required button components, you can implement them as follows:

### PrimaryButton Component

Create a file at `components/ui/primary-button.tsx`:

```tsx
import Link from "next/link";
import { ButtonHTMLAttributes, ReactNode } from "react";

interface PrimaryButtonProps extends ButtonHTMLAttributes<HTMLButtonElement> {
  children: ReactNode;
  href?: string;
}

export default function PrimaryButton({ 
  children, 
  href, 
  className = "",
  ...props 
}: PrimaryButtonProps) {
  const buttonClasses = `inline-flex items-center justify-center px-6 py-3 rounded-md font-medium bg-primary text-primary-foreground hover:bg-primary/90 transition-colors ${className}`;
  
  if (href) {
    return (
      <Link href={href} className={buttonClasses}>
        {children}
      </Link>
    );
  }
  
  return (
    <button className={buttonClasses} {...props}>
      {children}
    </button>
  );
}
```

### SecondaryButton Component

Create a file at `components/ui/secondary-button.tsx`:

```tsx
import Link from "next/link";
import { ButtonHTMLAttributes, ReactNode } from "react";

interface SecondaryButtonProps extends ButtonHTMLAttributes<HTMLButtonElement> {
  children: ReactNode;
  href?: string;
}

export default function SecondaryButton({ 
  children, 
  href, 
  className = "",
  ...props 
}: SecondaryButtonProps) {
  const buttonClasses = `inline-flex items-center justify-center px-6 py-3 rounded-md font-medium bg-secondary text-secondary-foreground hover:bg-secondary/90 transition-colors ${className}`;
  
  if (href) {
    return (
      <Link href={href} className={buttonClasses}>
        {children}
      </Link>
    );
  }
  
  return (
    <button className={buttonClasses} {...props}>
      {children}
    </button>
  );
}
```

## 🔄 Customization Tips

1. **Page Metadata**: Update the `title` and `description` in the metadata object
2. **Hero Section**: Replace the YouTube embed with your own video or image
3. **Content Sections**: Add, remove, or modify sections as needed
4. **Resources**: Update the links to point to your relevant resources
5. **Social Links**: Modify the social media links to connect to your accounts

## 📱 Responsive Behavior

The template includes responsive design considerations:
- Stack buttons vertically on small screens, horizontally on larger screens
- Adjust text sizes for better readability on mobile
- Use a single column layout on mobile, dual column for cards on desktop

## 🎨 Styling Notes

This template uses TailwindCSS with:
- Container constraints for consistent layout
- Responsive padding and margin
- Dark mode compatibility with `dark:` variants
- Prose styling for rich text content

## 🤝 Contributing

Contributions to improve this template are welcome! Please feel free to submit pull requests with enhancements or fixes.

## 📄 License

This template is available under the MIT License. Feel free to use it in your personal or commercial projects.
