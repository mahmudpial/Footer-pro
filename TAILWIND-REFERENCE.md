# Tailwind CSS Footer - Quick Reference Guide

## Essential Tailwind Classes for Footers

### Layout Classes

```
max-w-7xl          Max width container (80rem)
max-w-6xl          Max width container (64rem)
max-w-5xl          Max width container (64rem)
mx-auto            Center horizontally
px-4               Horizontal padding
py-12              Vertical padding
py-16              Larger vertical padding
```

### Grid & Flexbox

```
grid                Enable CSS Grid
grid-cols-1        1 column (mobile)
grid-cols-2        2 columns
grid-cols-3        3 columns
grid-cols-4        4 columns
grid-cols-5        5 columns
grid-cols-6        6 columns

md:grid-cols-2     2 columns on tablet+
md:grid-cols-3     3 columns on tablet+
md:grid-cols-4     4 columns on tablet+
lg:grid-cols-5     5 columns on desktop+

gap-6              Gap between grid items
gap-8              Larger gap
gap-12             Even larger gap

flex               Enable flexbox
flex-col           Column direction
flex-row           Row direction
justify-between    Space content apart
justify-center     Center content
items-center       Center items vertically
```

### Background Colors

```
bg-white           White background
bg-gray-50         Very light gray
bg-gray-100        Light gray
bg-gray-800        Dark gray
bg-gray-900        Very dark gray
bg-black           Black

bg-blue-500        Blue accent
bg-blue-600        Darker blue
bg-purple-600      Purple
bg-pink-600        Pink

bg-gradient-to-r   Right gradient
bg-gradient-to-b   Bottom gradient
from-blue-500      Gradient start
to-purple-600      Gradient end
```

### Text Colors

```
text-white         White text
text-gray-300      Light gray text
text-gray-600      Medium gray text
text-gray-900      Dark gray text
text-black         Black text

text-blue-600      Blue text
text-purple-600    Purple text

hover:text-white   Hover effect
hover:text-gray-900
hover:text-blue-500
hover:text-blue-700
```

### Borders & Dividers

```
border-t           Top border
border-b           Bottom border
border-l           Left border
border-r           Right border

border-gray-200    Light border color
border-gray-800    Dark border color

border-l-4         Left border (4px)
```

### Typography

```
text-xs            Extra small font
text-sm            Small font
text-base          Base font size
text-lg            Large font
text-xl            Extra large
text-2xl           2x large
text-3xl           3x large

font-normal        Normal weight
font-semibold      Semi-bold (600)
font-bold          Bold (700)

leading-relaxed    Larger line height
leading-tight      Smaller line height
```

### Spacing & Sizing

```
w-full             100% width
h-10               40px height
h-9                36px height

p-6                Padding all sides (6)
px-4               Padding horizontal
py-4               Padding vertical
py-8               More vertical padding
py-12              Even more

mb-4               Margin bottom
mb-6               More margin bottom
mb-8               Even more
mt-3               Margin top
mt-6               More margin top

rounded            Default border radius
rounded-lg         Larger border radius
rounded-full       Fully rounded

shadow             Drop shadow
shadow-sm          Small shadow
shadow-lg          Large shadow
```

### Interactive States

```
hover:bg-blue-600      Background on hover
hover:text-white       Text color on hover
hover:text-blue-600    Different text on hover
transition             Smooth transitions
transition-colors      Color transitions

focus:outline-none     Remove focus outline
focus:ring-2           Add focus ring
focus:ring-blue-500    Ring color
```

### Responsive Prefixes

```
(no prefix)         Mobile (320px+)
sm:                 Small (640px+)
md:                 Medium (768px+)
lg:                 Large (1024px+)
xl:                 Extra Large (1280px+)
2xl:                2X Large (1536px+)

Example:
md:grid-cols-4     4 columns on 768px+
lg:flex-row        Row direction on 1024px+
```

## Common Footer Patterns

### Dark Footer

```html
<footer class="bg-gray-900 text-gray-300">
  <div class="max-w-7xl mx-auto px-4 py-12">
    <!-- Content -->
  </div>
</footer>
```

### Light Footer

```html
<footer class="bg-white border-t border-gray-200">
  <div class="max-w-7xl mx-auto px-4 py-12">
    <!-- Content -->
  </div>
</footer>
```

### Grid Layout (4 Columns)

```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
  <div>Column 1</div>
  <div>Column 2</div>
  <div>Column 3</div>
  <div>Column 4</div>
</div>
```

### Link List

```html
<ul class="space-y-2">
  <li><a href="#" class="hover:text-white transition">Link</a></li>
  <li><a href="#" class="hover:text-white transition">Link</a></li>
</ul>
```

### Social Icons

```html
<div class="flex gap-4">
  <a href="#" class="hover:text-blue-500 transition">
    <i class="fab fa-twitter"></i>
  </a>
</div>
```

### Newsletter Form

```html
<form class="space-y-3">
  <input type="email" placeholder="Email" class="w-full px-4 py-2 rounded-lg" />
  <button class="w-full bg-blue-600 text-white py-2 rounded-lg">
    Subscribe
  </button>
</form>
```

## Color Combinations

### Professional Dark

- Background: `bg-gray-900`
- Text: `text-gray-300`
- Hover: `hover:text-white`
- Accent: `bg-blue-600`

### Modern Light

- Background: `bg-white`
- Text: `text-gray-900`
- Hover: `hover:text-blue-600`
- Border: `border-gray-200`

### Gradient Accent

- Background: `bg-gradient-to-r from-blue-500 to-purple-600`
- Text: `text-white`
- Border: Use for accent bars

## Tips & Tricks

1. **Responsive Design**: Always use mobile-first approach

   ```
   grid-cols-1 md:grid-cols-2 lg:grid-cols-4
   ```

2. **Smooth Interactions**: Add transition class

   ```
   class="hover:text-white transition"
   ```

3. **Spacing Consistency**: Use gap and margin together

   ```
   gap-8 mb-8 pb-8
   ```

4. **Typography Hierarchy**: Use different text sizes

   ```
   h4: text-white font-semibold
   p: text-gray-400 text-sm
   ```

5. **Icon Sizing**: Keep social icons consistent
   ```
   w-10 h-10 rounded-lg
   ```

## Common Mistakes to Avoid

❌ Mixing responsive prefixes incorrectly

```
grid-cols-md-4  ← WRONG
```

✅ Correct approach

```
md:grid-cols-4  ← RIGHT
```

❌ Forgetting transition class

```
<a href="#" class="hover:text-white">  ← No smooth transition
```

✅ Better

```
<a href="#" class="hover:text-white transition">
```

❌ Not responsive

```
<div class="flex gap-4">  ← Stacks badly on mobile
```

✅ Responsive layout

```
<div class="grid grid-cols-1 md:grid-cols-4 gap-4">
```

## Resources

- Tailwind Documentation: https://tailwindcss.com/docs
- Color Palette: https://tailwindcss.com/docs/customizing-colors
- Component Examples: https://tailwindui.com/
- Font Awesome Icons: https://fontawesome.com/icons

---

**Pro Tip:** Copy this file as a reference while building your footers!
