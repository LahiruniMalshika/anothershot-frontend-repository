# AnotherShot Frontend

A modern, responsive Progressive Web App (PWA) built with Next.js 14 for photographer booking and portfolio showcasing. AnotherShot provides an intuitive platform where clients can discover and book photographers while photographers can showcase their work and manage their business.

## 🚀 Features

### Core Functionality
- **Multi-Role Authentication**: Seamless login/signup for Clients, Photographers, and Admins
- **Photographer Discovery**: Advanced search and filtering to find photographers by category, location, and style
- **Portfolio Showcase**: Beautiful image galleries with like/save functionality
- **Booking System**: Complete booking workflow with calendar integration
- **Real-time Chat**: Instant messaging with file attachments and emoji support
- **Payment Processing**: Secure Stripe integration for seamless payments
- **Profile Management**: Comprehensive profile setup for both clients and photographers
- **Package Management**: Photographers can create and manage service packages
- **Review System**: Testimonials and rating system for photographers
- **Notification System**: Real-time notifications for bookings, messages, and updates

### Advanced Features
- **Progressive Web App**: Installable app with offline capabilities
- **Responsive Design**: Optimized for desktop, tablet, and mobile devices
- **Image Management**: Cloudinary integration for high-quality image handling
- **Calendar Integration**: FullCalendar for booking scheduling
- **File Upload**: Drag-and-drop file uploads with progress indicators
- **Search & Filtering**: Advanced search with multiple filter options
- **Social Features**: Like, save, and share photographer portfolios
- **Admin Dashboard**: Comprehensive admin panel for platform management
- **Email Templates**: Custom email notifications and confirmations
- **SEO Optimized**: Next.js SEO features for better discoverability

### Role-Based Features

#### For Clients
- **Photographer Discovery**: Browse and search photographer portfolios
- **Booking Management**: Complete booking workflow with calendar integration
- **Payment Processing**: Secure Stripe checkout for bookings and albums
- **Real-time Chat**: Direct messaging with photographers
- **Profile Management**: Personal profile with booking history
- **Gallery Access**: View and purchase photographer albums
- **Review System**: Rate and review photographers after bookings

#### For Photographers
- **Portfolio Management**: Comprehensive profile with hero section, featured photos, and contact info
- **Album Creation**: Advanced album management with image uploads and pricing
- **Package Management**: Create and manage service packages with pricing
- **Booking Management**: Handle booking requests with calendar integration
- **Earnings Tracking**: Detailed earnings analytics with fee calculations
- **Settings Management**: Bank details, categories, and profile settings
- **Testimonial Management**: Manage client reviews and testimonials
- **Feed Management**: Social media-like portfolio feed
- **Event Management**: Create and manage photography events
- **History Tracking**: Complete transaction and booking history

#### For Admins
- **Dashboard Analytics**: Comprehensive analytics with revenue, users, and booking metrics
- **User Management**: Complete user administration and moderation
- **Payment Handling**: Payment administration and dispute resolution
- **Report Management**: Handle system, profile, and image reports
- **Content Moderation**: Platform content management and moderation
- **System Reports**: Platform-wide reporting and analytics

## 🛠️ Tech Stack

### Frontend Framework
- **Next.js 14**: React framework with App Router
- **React 18**: Modern React with hooks and concurrent features
- **TypeScript**: Type-safe development
- **Tailwind CSS**: Utility-first CSS framework

### UI Components & Styling
- **Radix UI**: Accessible component primitives
- **Lucide React**: Beautiful icon library
- **Framer Motion**: Smooth animations and transitions
- **React Hook Form**: Form handling with validation
- **Zod**: Schema validation

### State Management & Data Fetching
- **TanStack Query**: Server state management
- **NextAuth.js**: Authentication and session management
- **Socket.io Client**: Real-time communication
- **Axios**: HTTP client for API requests

### Payment & File Handling
- **Stripe**: Payment processing with React components
- **Cloudinary**: Image and file management
- **Next PWA**: Progressive Web App capabilities

### Development Tools
- **ESLint**: Code linting
- **Prettier**: Code formatting
- **Husky**: Git hooks
- **Commitlint**: Commit message linting

## 📋 Prerequisites

- Node.js (v18 or higher)
- npm or yarn package manager
- AnotherShot Backend API running
- Stripe account (for payments)
- Cloudinary account (for image storage)

## 🚀 Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd anothershot-frontend
   ```

2. **Install dependencies**
   ```bash
   npm install
   # or
   yarn install
   ```

3. **Environment Setup**
   Create a `.env.local` file in the root directory:
   ```env
   NEXTAUTH_URL="http://localhost:3000"
   NEXTAUTH_SECRET="your-nextauth-secret"
   NEXTAUTH_GOOGLE_CLIENT_ID="your-google-client-id"
   NEXTAUTH_GOOGLE_CLIENT_SECRET="your-google-client-secret"
   NEXT_PUBLIC_API_URL="http://localhost:8000"
   NEXT_PUBLIC_STRIPE_PUBLISHABLE_KEY="your-stripe-publishable-key"
   NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME="your-cloudinary-cloud-name"
   NEXT_PUBLIC_CLOUDINARY_API_KEY="your-cloudinary-api-key"
   NEXT_PUBLIC_CLOUDINARY_UPLOAD_PRESET="your-upload-preset"
   ```

4. **Start the development server**
   ```bash
   npm run dev
   # or
   yarn dev
   ```

The application will be available at `http://localhost:3000`

## 📁 Project Structure

```
app/
├── (auth)/                # Authentication routes
├── about/                 # About page routes
├── api/                   # API routes
├── data/                  # Static data and constants
├── lib/                   # Utility functions and configurations
├── page.tsx               # Home page
├── search/                # Search functionality
├── suspended/             # Suspended user page
├── unauthorized/          # Unauthorized access page
└── user/                  # User dashboard routes
    └── (routes)/
        ├── admin/         # Admin dashboard
        │   └── [userId]/
        │       └── (routes)/
        │           ├── dashboard/        # Analytics dashboard
        │           ├── inbox/           # Admin inbox
        │           ├── payment-handling/ # Payment administration
        │           ├── report-handling/  # Report management
        │           └── user-management/  # User administration
        ├── client/        # Client dashboard
        │   └── [userId]/
        │       └── (routes)/
        │           ├── bookings/        # Booking management
        │           ├── inbox/          # Client inbox
        │           └── profile/        # Client profile
        └── photographer/  # Photographer dashboard
            └── [userId]/
                └── (routes)/
                    ├── albums/         # Album management
                    ├── bookings/       # Booking management
                    ├── feed/          # Portfolio feed
                    ├── inbox/         # Photographer inbox
                    └── profile/       # Photographer profile
                        ├── contactSection/    # Contact management
                        ├── featuredPhoto/     # Featured photos
                        ├── heroSection/       # Hero section
                        ├── history/          # Transaction history
                        ├── packagesSection/  # Package management
                        ├── settings/         # Settings management
                        └── testimonialSection/ # Testimonial management

components/
├── adminHeader.tsx        # Admin navigation
├── auth/                  # Authentication components
├── chat/                  # Chat and messaging components
├── checkout/              # Payment and checkout components
├── DateTimePickers/       # Date and time selection
├── feedImageComp.tsx      # Image feed component
├── Header.tsx             # Main navigation
├── icons/                 # Custom icons
├── loading.tsx            # Loading components
├── Navbar.tsx             # Navigation bar
├── notification/          # Notification components
├── offer/                 # Offer management components
├── pagination.tsx         # Pagination component
├── Report/                # Reporting components
├── skeletonHome.tsx       # Loading skeletons
├── systemReport.tsx       # System reporting
├── ui/                    # Reusable UI components (33 components)
└── ...                    # Other feature components

context/
├── socketContext.tsx      # Socket.io context

hooks/
├── photographer/          # Photographer-specific hooks
└── use-testHook.tsx       # Custom hooks

providers/
├── AuthProvider.tsx       # Authentication provider
├── QueryProvider.tsx      # TanStack Query provider
└── toast-provider.tsx     # Toast notification provider

services/
├── auth/                  # Authentication services
├── chat/                  # Chat services
├── home/                  # Home page services
├── photographer/          # Photographer services
└── user/                  # User services

utils/
├── get-stripejs.ts        # Stripe utilities
└── mongodb.ts             # MongoDB utilities
```

## 🔧 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run start` - Start production server
- `npm run lint` - Run ESLint
- `npm run release` - Create a new release

## 🎨 UI/UX Features

### Design System
- **Modern Interface**: Clean, professional design with intuitive navigation
- **Responsive Layout**: Mobile-first design that works on all devices
- **Dark/Light Mode**: Theme switching capability
- **Accessibility**: WCAG compliant components with keyboard navigation
- **Loading States**: Skeleton loaders and smooth transitions

### User Experience
- **Progressive Web App**: Installable with offline capabilities
- **Real-time Updates**: Live notifications and chat
- **Image Optimization**: Automatic image optimization and lazy loading
- **Search & Filter**: Advanced filtering with instant results
- **Calendar Integration**: Intuitive booking calendar

## 🔐 Authentication

The app uses NextAuth.js with multiple providers:
- **Email/Password**: Traditional authentication
- **Google OAuth**: Social login integration
- **JWT Tokens**: Secure session management
- **Role-based Access**: Different interfaces for Clients, Photographers, and Admins

## 💳 Payment Integration

Stripe integration provides:
- **Secure Checkout**: Stripe Elements for secure payment forms
- **Multiple Payment Methods**: Cards, digital wallets, and more
- **Webhook Handling**: Real-time payment status updates
- **Payment History**: Complete transaction records

## 📱 Real-time Features

Socket.io implementation enables:
- **Live Chat**: Real-time messaging between users
- **File Sharing**: Image and document sharing in chat
- **Notifications**: Instant notifications for various events
- **Online Status**: Real-time user presence indicators

## 🖼️ Image Management

Cloudinary integration provides:
- **High-Quality Images**: Optimized image delivery
- **Responsive Images**: Automatic resizing for different devices
- **Image Upload**: Drag-and-drop with progress indicators
- **Image Editing**: Basic editing capabilities
- **CDN Delivery**: Fast global image delivery

## 📊 State Management

- **TanStack Query**: Server state management with caching
- **React Context**: Global state for authentication and socket
- **Local State**: React hooks for component-level state
- **Form State**: React Hook Form for complex forms

## 🧪 Testing

The project includes:
- **Component Testing**: React component testing setup
- **Integration Testing**: API integration testing
- **E2E Testing**: End-to-end testing capabilities
- **Type Safety**: TypeScript for compile-time error checking

## 🚀 Deployment

### Production Build
```bash
npm run build
npm run start
```

### Vercel Deployment
The app is optimized for Vercel deployment:
```bash
vercel --prod
```

### Environment Variables
Ensure all required environment variables are set in your deployment platform.

## 📈 Performance Optimizations

- **Code Splitting**: Automatic code splitting with Next.js
- **Image Optimization**: Next.js Image component with optimization
- **Lazy Loading**: Component and image lazy loading
- **Caching**: TanStack Query caching for API responses
- **PWA**: Service worker for offline functionality

## 🔧 Configuration

### Next.js Configuration
- **App Router**: Modern Next.js routing
- **TypeScript**: Full TypeScript support
- **PWA**: Progressive Web App configuration
- **Image Domains**: Configured for Cloudinary and other CDNs

### Tailwind Configuration
- **Custom Colors**: Brand-specific color palette
- **Responsive Design**: Mobile-first breakpoints
- **Component Classes**: Reusable component styles

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the UNLICENSED License.

## 🆘 Support

For support and questions, please contact the development team or create an issue in the repository.

## 🔄 Version History

- **v0.1.1** - Current version with full feature set
- Includes all major features for photographer booking platform

## 🌟 Key Features Showcase

### For Clients
- **Photographer Discovery**: Browse and search photographer portfolios with advanced filtering
- **Booking System**: Complete booking workflow with calendar integration and package selection
- **Payment Processing**: Secure Stripe checkout for bookings and album purchases
- **Real-time Communication**: Direct messaging with photographers via chat
- **Profile Management**: Personal profile with booking history and preferences
- **Gallery Access**: View and purchase photographer albums with secure payment
- **Review System**: Rate and review photographers after completed bookings
- **Notification System**: Real-time notifications for booking updates and messages

### For Photographers
- **Comprehensive Portfolio**: Hero section, featured photos, contact information, and testimonials
- **Album Management**: Create, edit, and manage photo albums with pricing and visibility controls
- **Package Management**: Create and manage service packages with detailed descriptions and pricing
- **Booking Management**: Handle booking requests with calendar integration and status tracking
- **Earnings Analytics**: Detailed earnings tracking with fee calculations and payment history
- **Settings Management**: Bank details, photographer categories, and profile customization
- **Testimonial Management**: Manage client reviews and testimonials with visibility controls
- **Feed Management**: Social media-like portfolio feed with like and save functionality
- **Event Management**: Create and manage photography events with calendar integration
- **History Tracking**: Complete transaction and booking history with detailed analytics

### For Admins
- **Dashboard Analytics**: Comprehensive platform analytics with revenue, user, and booking metrics
- **User Management**: Complete user administration, moderation, and account management
- **Payment Administration**: Payment handling, dispute resolution, and transaction management
- **Report Management**: Handle system reports, profile reports, and image reports
- **Content Moderation**: Platform content management and moderation tools
- **System Reports**: Platform-wide reporting and analytics with detailed insights
- **User Analytics**: Active user tracking and platform usage statistics
- **Revenue Analytics**: Monthly revenue tracking and payment analytics

---

Built with ❤️ using Next.js, React, TypeScript, and modern web technologies.