# React Performance Checklist

A practical checklist for shipping fast React applications.

## Rendering
- [ ] Memoize expensive components with `React.memo` where profiling shows benefit
- [ ] Split large components and lazy-load routes with `React.lazy` + `Suspense`
- [ ] Avoid creating new object/array literals in props on every render
- [ ] Use stable keys in lists — never use array index for reorderable lists
- [ ] Virtualize long lists (react-window / tanstack virtual)

## State Management
- [ ] Colocate state as close to usage as possible
- [ ] Derive values instead of duplicating state
- [ ] Debounce expensive search/filter operations
- [ ] Prefer URL state for shareable UI state when appropriate

## Data Fetching
- [ ] Cache server responses (React Query, SWR, or RTK Query)
- [ ] Prefetch critical routes and data on hover/intent
- [ ] Paginate or infinite-scroll large datasets
- [ ] Show skeleton UI instead of layout-shifting spinners

## Assets & Network
- [ ] Code-split by route and heavy libraries
- [ ] Compress and lazy-load images; use modern formats (WebP/AVIF)
- [ ] Preload critical fonts; subset font files
- [ ] Enable gzip/brotli on the CDN

## Build & Monitoring
- [ ] Analyze bundle size in CI (vite-bundle-visualizer / webpack analyzer)
- [ ] Track Core Web Vitals in production
- [ ] Set performance budgets for LCP, INP, and CLS
- [ ] Profile with React DevTools Profiler before optimizing

---
Created by Dhaval Gediya — Senior Full Stack Developer
https://github.com/dhavalgediya
