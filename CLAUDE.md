# Finkargo Analiza - Version Management

## 🎯 Current Stable Version: v1.0-vector-stable

### Version History
- **v1.0-vector-stable** (2025-08-15): Complete UI overhaul with perfect vector design system
  - ✅ All DIAN → Aduanas replacements across platform
  - ✅ Perfect decorative vector system implementation
  - ✅ Enhanced vibrant color gradients (gray → blue/cyan/purple)
  - ✅ Auth pages complete redesign with improved UX
  - ✅ FAQ optimization with accordion functionality
  - ✅ Vector spacing and positioning perfected
  - ✅ Wompi payment integration with simulation mode
  - ✅ Consistent design system across all pages

## 🚀 Quick Start Commands

### Access Stable Version
```bash
git checkout v1.0-vector-stable
npm install
npm run dev
```

### Continue Development
```bash
git checkout development
npm install
npm run dev
```

### Create New Features
```bash
git checkout development
git checkout -b feature/your-feature-name
# Make changes
git commit -m "feat: your feature description"
git push origin feature/your-feature-name
```

## 🎨 Design System Documentation

### Vector System
- **Hexagon Blue**: `#5479F7` - Perfect SVG with viewBox "0 0 124 112"
- **Star Coral**: 6-ray star with stroke `#f97316` - Perfect SVG implementation  
- **BrandIcon**: Custom Finkargo brand icon with rays
- **Supporting Icons**: Database, Globe, Target with strategic positioning

### Color Palette
- **Primary**: `#2563eb` (Finkargo Blue)
- **Secondary**: `#06b6d4` (Cyan)
- **Coral**: `#f97316` (Brand Coral)
- **Gradients**: Blue to cyan, purple variations

### Component Structure
- Next.js 15.4.5 with TypeScript
- Tailwind CSS with custom design system
- Shadcn/ui components
- NextAuth.js authentication
- Prisma ORM with SQLite
- Wompi payment integration

## 📁 Architecture Notes

### Key Directories
```
src/
├── app/                    # Next.js 13+ app directory
│   ├── api/               # API routes
│   ├── auth/              # Authentication pages
│   ├── dashboard/         # Protected dashboard
│   ├── features/          # Features showcase
│   ├── precios/           # Pricing page
│   └── demo/              # Interactive demo
├── components/            # Reusable components
│   ├── ui/               # Base UI components
│   └── dashboard/        # Dashboard-specific
└── lib/                  # Utilities and configs
```

### Database Schema
- User authentication with NextAuth
- Subscription management
- Payment tracking with Wompi
- Company information storage

## 🔄 Version Management Strategy

### Semantic Versioning
- **v1.x.x**: Current stable branch
- **v1.1.x**: Minor features and enhancements
- **v1.x.1**: Hotfixes and patches
- **v2.0.0**: Major architectural changes

### Branch Strategy & Deployment Flow
```
development → staging → main/production
```

- **development**: Active development branch for new features
- **staging**: Testing and validation environment  
- **main**: Stable production-ready code
- **feature/***: Individual feature development (branch from development)
- **hotfix/***: Critical fixes for production (branch from main)

### Environment Mapping
- **development branch** → Local development (SQLite)
- **staging branch** → Staging environment (PostgreSQL) - https://finkargo-analiza-c.vercel.app
- **main branch** → Production environment (PostgreSQL) - https://finkargo-analiza.vercel.app

## 🛠️ Common Development Tasks

### Start New Feature Development
```bash
git checkout development
git pull origin development
git checkout -b feature/your-feature-name
# Make changes
git commit -m "feat: your feature description"
git push origin feature/your-feature-name
# Create PR to development branch
```

### Deploy to Staging
```bash
git checkout staging
git merge development
git push origin staging
# Verify changes at https://finkargo-analiza-c.vercel.app
```

### Deploy to Production
```bash
git checkout main
git merge staging
git tag -a v1.x.x -m "Release version x.x.x"
git push origin main --tags
# Verify changes at https://finkargo-analiza.vercel.app
```

### Hotfix for Production
```bash
git checkout main
git checkout -b hotfix/fix-description
# Make critical fix
git commit -m "fix: critical issue description"
git checkout main
git merge hotfix/fix-description
git checkout staging
git merge main  # Keep staging in sync
git push origin main staging
```

## 📞 Support & Documentation

### Payment Integration
- Wompi sandbox testing documented in `WOMPI_TESTING.md`
- Simulation mode available for development

### Authentication
- NextAuth.js configuration in `src/lib/auth.ts`
- Protected routes with middleware

### Database
- Prisma schema in `prisma/schema.prisma`
- SQLite for development, PostgreSQL for production

---

**Generated with Claude Code on 2025-08-15**
**Maintained by: Finkargo Development Team**