# CSS History, Present & Future

- CSS1 -> 1996
- CSS2 -> 1998
- CSS3 -> In Development
- Never CSS4

# Course Outline

- Basic Track

  - Getting Started
  - The Basics
  - Diving Deeper
  - More on Selector & CSS Features
  - Practicing the Basics
  - Positioning

- Advanced Track

  - Background & Images
  - Dimensions, Units & Sizes
  - JavaScript & CSS
  - Responsiveness
  - Styling Forms
  - Working with text and fonts

- Expert Track
  - Flexbox
  - CSS Grid
  - Transformations
  - Transitions & Animations
  - Writing Future-Proof CSS
  - SASS/SCSS Introduction

# Course Prerequisites

- HTML

# How to get the Most out of the Course

- Watch the videos
- Code Along & Do Exercises
- Debug Errors
- Ask in Q&A
- Answer in Q&A

# Recommended Tools

-

# Module Introduction

- How to Add CSS to HTML
- Setting up CSS Rules
- Selectors, Properties & Values
- Conflicting Styles

# Adding CSS to our Project with Inline Styles

-

# Understanding the <style> Tag & Creating a .css File

-

# Applying Additional Styles & Importing Google Fonts

- Default fonts are different in Chrome depending on the settings of that user.

# Theory Time - Selectors

- Elements = Set equal style for these elements
- h1 { color: red; }
- Classes = Zelfde stijl voor elementen die dezelfde class hebben.
- .blog-post {
  color: red;
  }
- Universal:

* {} rarely used, also bad-practice, only in a specific case.

- Id: style for a specific element
- #main-title { color: red; }
- Attributes -> Set equal styles to all elements with attributes.
- attribute selector
  - button disabled
  - [disabled] {color: red};

# Class

- You can re-use it.

# Id

- You can only use it one time.
- For one specific element.

# kebab-case

- Use kebab-case for id and class in your html and css

# Understanding the "Cascading" Style & Specificity

- Specificity zijn voorangsregels met CSS styles welke eerst toegepast worden.

# Cascading

- Multiple Rules can apply to the same element.

# Specificity

- Resolve conflicts arising from multiple rules.

# Specificity Pyramid

- 1. <tag> and ::pseudo-element selectors.
- 2. .class, :pseudo-class and [attribute] selectors.
- 3. #ID selectors
- 4. Inline Styles

# Understanding Inheritance

- Inheritance parent things are passed down to childs.
- Specicify not high.

# Adding Combinators

-

# Theory Time - Combinators

- Adjacent Sibling

  - Assign style to all <p> that directly comea after an h2 tag.
  - h2 + p {
    color: red;
    }
  - Elements have to share the same parent.
  - Second element comes immediately after first element.

- General Sibling

  - Selects the p after the h2 element and the rest of p elements.
  - h2 ~ p { color: red; }
  - Elements share the same parent.
  - Second element comes after first element.

- Child Combinator

  - Select every p child element inside div
  - div > p { color: red; }
  - Second element is a direct child of first element.

- Descendant
  - All p's inside the div
  - div p { color: red; }
  - Second element is a descendant of the first element.
  - Used most often.

# Summarizing Properties & Selectors

- Selectors

  - div
  - .blog-post
  - #main-title
  - [disabled]
  - -

- Properties

  - background-color
  - width
  - color
  - margin
  - display

- Values
  - red
  - 30%
  - #fa923f
  - 10px
  - block

# Value Types

- Values are tightly coupled to specific properties.

- Pre-defined Options

  - display: block;
  - overflow: auto;

- Colors

  - background: red;
  - color: #fa923f;
  - color: #ccc;

- Length, Sizes & Numbers

  - height: 100px;
  - width: 20px;
  - order: 1;

- Functions
  - background: url();
  - transform: scale();

# Wrap Up

- CSS works with Rules
- Different Types of Selectors
- Properties & Values
  - Long list of available properties and values
  - Check MDN or comparable references.
  - Different Type of Values, depending on Properties.
- Selectors with Combinators
- Inheritance & Specifity
  - Parent styles are generally inherited.
  - Multiple rules can apply to one element.
  - Specifity resolves "multiple rules" conflicts.
  - Inheritance defaults can be changed.

# Module Introduction

- The Box Model
- Height & Width
- The "display" Property
- "Properties Worth to Remember"
- Pseudo Classes & Elements

# Introducing the CSS Box Model

- Content = Blue
- Padding = Green
- Border = Yellow
- Margin = Orange

# Understanding the Box Model

-

# Margin Collapsing

- 2 elements next to each other and 2 margins become 1 margin.
- The bigger margin takes over for the 2 elements.
- To work around margin collapsing.
- Use margin-top OR margin-bottom.

# Shorthand Properties

- Combine values of multiple properties in a single property (the shorthand property).
- border: 2px dashed orange;
- margin: 5px 10px 5px 10px -> clockspin
- margin: 5px 10px -> top + bottom, left + right -> crossdraw
- margin: 10px -> all sides
- Always use shorter notation to stay clean.

# Pseudo Classes

- Defines the style of a special state of an element.
- :class name

# Pseudo Element

- Defines the styles of a specific part of an element.
- ::element name
- ::first-letter
- /_ a::after After a add some content _/
  .main-nav\_\_item a::after {
  content: " Karina";
  color: red;
  }

# Grouping Rules

- 2 selectors at the same time.
- DRY programming.
- Elements with the same styling.
  /_ Grouping elements _/
  .main-nav**item a:hover,
  .main-nav**item a:active {
  color: white;
  }

# Properties Worth to Remember

- color
- background-color
- display
- padding
- border
- margin
- width
- height

# Summary

-

# Module Introduction

- More on CSS Classes
- !important
- More on Pseudo Classes & Elements
- :not()

# More on CSS Classes

- You can use multiple classes one element.
- You can select a same-element combination.

# CSS Class Selectors vs ID Selectors

- CSS Class Selectors

  - .some-class {}
  - Re-usable
  - Allow you to "mark" and name things for styling purposes only.
  - Most-used selector type.

- CSS ID Selectors
  - #some-id {}
  - Only used once per page
  - Also got non-CSS meaning (e.g. on-page link)
  - Use if available anyways.

# Classes or IDs?

- Id's can be used to jump to specific links.

# !important

- Overwrites specifity and all other selectors.
- In general: Don't use !important!
  - Use specifity and rules to style your website according to your needs (and to write better CSS code in the end...)

# Selecting the Opposite with :not()

:not(p) select everything that is not p

# CSS & Browser Support

- Browser Compatibility Table on Mozilla MDN.

# Summary

- CSS Class Selectors

  - You can apply more than one class to an element.
  - You can chain selectors (e.g. a.active, .priority.highlighted)
  - Class selectors are the most-used type of CSS selectors.

- !important

  - Important: Don't use !important in 99% of cases.

- Pseudo Selectors & :not
  - You use the same pseudo-selectors in most cases (:hover, :active).
  - Explore your possibilities to solve edge cases with ease.
  - Use :not with caution but when needed to exclude certain elements.

# Positioning - How to change the position of elements

- Understanding the "position" Property
- Fixed Navigation Bars with "fixed"
- Positioning Elements with "z-index"
- Using "absolute" and "relative" - Stand Alone and Combined.
- "Sticky" Positioning
- The "Stacking Context"

# Keep navbar at same place

-

# Positioning Elements

- Position: static;
  - Normal document flow
- absolute
- relative
- fixed
- sticky

# Changing the Position

div - top left right bottom positioning changed in document flow.
top: 20px;

# Fixed Navigation Bar

position: fixed;
top: 0;
left: 0;

# Summary

- The position property

  - Fixed
  - Absolute
  - Relative
  - Sticky

- The Document Flow

  - The Default positioning behaviour of HTML elements.
  - Can be changed with position.
  - Elements can remain in the document flow or be excluded from it.

- Moving Elements

  - Top
  - Bottom
  - Left
  - Right

- Positioning Context

  - Defines the anchor point for your position change.
  - The viewport for fixed.
  - Another element for absolute.
  - The element itself for relative.
  - The viewport and another element for sticky.

- Z-Index

  - Changes the default element positioning along the z-axis.
  - auto (0) as default value.
  - Changes only possible when position is applied.
  - Larger values = element is position of top of other elements.

- Stacking Context
  - Created when applying fixed / sticky or absolute / relative in combination with z-index.
  - Defines stacking behaviour of child elements.

# Backgrounds & Images - Because a picture says more than a thousand words

-

# What's Inside This Module?

- Understanding the "background" property.
- Images & Background Images.
- Gradients.
- Filters.

# Understanding "background-size"

-

# The "background" Shorthand - Theory

- background: red;
  - Is a shorthan property
- background-image
  - Set one or ore background images.
- background-color
  - Set a background color.
- background-position
  - Set initial position, relative to background position layer.
- background-size
  - Set size of background image.
- background-repeat
  - Defines how background images are repeated.
- background-origin
  - Set background positioning area.
- background-clip
  - Define whether background extends underneath border.
- background-attachment
  - Sets the scrolling behaviour of the background-image.

# Using Multiple Backgrounds

- background:
- url(...)
- url(...)
- linear-gradient
- url(...)
- red -> Only one background-color may be used.

# Filters

-

# Summary

-

# Dimensions, Sizes & Units - Because there is more than "px"

- Theory - Which Units can we Use?
- "%" and the containing block
- "min-width" & "max-width"
- Understanding "rem" vs "em"
- Working with "vw" and "vh"

# Pixels, Percentages & More

- Units

  - Pixel (px)
  - Percentages (%)
  - root em = rem
  - em = em
  - viewport height = vh
  - viewport width = vw

- Which properties can I use in connection with these units?
- How is the size calculated?
- What's the right unit to choose?

# Where Units Matter

- Which properties can I use?
  - font-size
  - padding
  - border
  - margin
  - width
  - height
  - top
  - bottom
  - left
  - right

# How is the Size Calculated?

- Absolute Lengths

  - Most ignore user settings.
  - px -> used
  - cm
  - mm

- Viewport Lengths

  - Adjust to current viewport
  - vh -> used
  - vw
  - vmin
  - vmax

- Font-Relative Lengths
  - Adjust to default font size.
  - rem -> used
  - em -> used
  - ...
  - %

# How is the Box Size for % Units Calculated?

-

# 3 Rules to Remember

- Element

  - position: fixed;

- Viewport
  - Ancestor content + padding
  - position: absolute;

# Rules to Remember: Relative / Static Positioning & "%"

- Ancestor cotent
- position: static;
- position: relative;
- Block level element.

# Which Unit Should I Choose?

- Property

  - font-size (root element)
  - font-size

- Recommended Unit
  - %
  - -
  - rem (em => Children only)
  - px
  - rem
  - %
  - %

# Summary

-

# Summary

-

# Styling Form Elements - Handling user input with grace

- Styling Inputs & Buttons
- Validation Feedback Styles

# Advanced Attribute Selectors

- Element with attribute

  - [type] {
    color: red;
    }
  - <input type="text">

- Element with Specific Attribute Value

  - [type="email"] {
    color: red;
    }
  - <input type="email">

- Element with Specific Attribute Value in List

  - [lang~="en-us"] {
    color: red;
    }
  - <p lang="en-us en-gb">Hi!</p>

- Element with Specific Attribute Value/Value

  - [lang|="en"] {
    color: red;
    }
  - <p lang="en-us">Hi!</p>

- Element with Specific Attribute Value Prefix

  - [href^="#"] {
    color: red;
    }
  - <a href="#all">Link</a>

- Element with Specific Attribute Value Suffix

  - [href$=".de"] {
    color: red;
    }
  - <a href="ab.de">Link</a>

- Element with At Least One Attribute Value

  - [src*="cdn"] {
    color: red;
    }

- Check Values Case Insensitively
  - [src*="cdn" i] {
    color: red;
    }
  - <img src="i CDN com">

# Summary

-

# Working with Text and Fonts - How we can make our information look beautiful

- Generic & Font Families
- Using & Importing Font Families
- Font Properties
- Font Shorthand

# Generic Families & Font Families

- Generic
  - Serif -> Times New Roman, Georgia.
  - Sans-serif -> Helvetica, Verdana.
  - Cursive -> Brush Script, Mistral.
  - Monospace -> Courier New, Lucida Bright.
  - Fantasy ->

# What Will Be Displayed?

- Default -> Chrome, Firefox, Edge, Safari, IE.
- Generic Family -> CSS Code -> Chrome, FF, Edge, Safari, IE.
- Font Family -> User's Computer, Web Fonts.
- Retrieved From Server.

# Which Tools do we Have?

- Viewport
  - Adjust site to device viewport.
  - No design changes.
- Media Queries
  - Change design depending on size.
  - Design changes defined by us.

# Responsive Design - Let's make our page look awesome on all devices

- Hardware vs. Software Pixels
- The "viewport" <meta> tag in HTML
- Media Queries with @media

# CSS and JavaScript - Sometimes, content needs to change AFTER the page was loaded

- Manipulating Styles via JavaScript.
- Adding & Removing CSS Classes via JS.
-

<div><div> -> HTML
div { background: brown } -> CSS
div { background: brown; filter: blur(10px); }

# Working With Google Fonts

- @import is prefereed put it in the CSS file.

# font-display

- font-display

  - swap, block, fallback, optional, auto

- block-period

  - n/a
  - fallback
  - short

- swap-period
  - swap the fallback font.
  - infinite.
  - custom-font.

# Summary

-

# Working with Flexbox - The Modern Way To Change The Way Our Elements Are Displayed

- The Flex-Container
- Main Axis vs. Cross Axis
- The Flex Items

# Understanding Flexbox

- Parent = Flex Container

  - Property
    - display: flex; -> Flex Container
    - flex-flow:
    - justify-conent:
    - align-content:
    - align-items:

- Children = Flex Items
  - Property
    - order:
    - flex:
    - align-self:

# Flexbox (parent container) (homework)

Row = X
Column = Y
display: flex; /_ Displays childs in 1 row, childs become flex-items _/
display: inline-flex; -> Flex-items stay the same they don't scale.
flex-wrap: wrap; /_ When screen gets smaller the flex-item jumps to another row, responsive _/
flex-wrap: wrap-reverse; /_ When screen gets smaller the flex-item order reverses, responsive _/
flex-direction: column; /_ Every flex-item occupies their individual single row _/
flex-direction: column-reverse; /_ Every flex-item occupies their individual single row reversed _/
flex-direction: row; = Every flex-item fills x space in order until full.

# Main Axis vs Cross Axis (Homework)

- flex-direction: row; -> starts from left main-axis to right, cross-axis to left bottom.
- main-axis -> x-axis;
- cross-axis -> y-axis;
- flex-direction: row-reverse; -> starts from right main-axis to left, cross-axis to right bottom.
- flex-direction: column; -> main-axis top to bottom, cross-axis upper left to right.
- flex-direction: column-reverse; -> main bottom to top, cross-axis bottom left to right
- /_ flex-flow: row wrap; = flex-direction and flex wrap combined _/
- align-items: center; /_ Centers columns along the cross-axis _/
- align-items: flex-start; /_ Begin at start of the cross-axis _/
- align-items: flex-end; /_ Begin at end of the cross-axis _/
- align-items: flex-start; /_ Begin at start of the cross-axis _/
- justify-content: flex-end; /_ Start from end of main-axis _/

# Align Items and Justify Content (2D movement)

- justify-content controls the main-axis
- align-items control the cross-axis
- with flexbox you create 2D movement.

# And What About "align-content"?

# Practicing the Basics - Can't do that enough!

-

# Adding Style to our Plans

-

# Styling the Badge with "border-radius"

-

# Styling our List

-

# Working with "font-weight" & "border"

-

# Understanding an Unexpected "inline-block" Behaviour

-

# Adding Pseudo Classes

-

# Applying Shorthands in Practice

-

# Diving Into the Height & Width Properties

-

# Height & Width

-

# Adding the Header to our Project

-

# display: inline-block

- Inline but you can do block like styling margin, padding etc.

# Understanding an Unexpected "inline-block" Behaviour

-

# Working with "text-decoration" & "vertical-align"

-

# Grid Container <div>

- display: grid; /_ Grid container _/

# Defining Columns & Rows

- grid-template-columns: 200px 150px 20%; /_ 3 COLUMNS SET _/

# Positioning Child Elements in a Grid

- GRID SIZING
  grid-template-columns: 200px 2fr 20% 1fr; /_X 3 COLUMNS SET _/
  grid-template-rows: 5rem 2.5rem; /_ Y _/

- Check out CSS GRID IN DEVTOOLS
  grid-column-start: 3;
  grid-column-end: 5;
  grid-row-start: 1;
  grid-row-end: 3;

- justify = x
- align = y

# CSS Transforms - Rotating, scaling and moving things around

- Rotating, Moving, Skewing & Scaling Elements.
- 3D Transformations.

# Rotate

- rotateX(45deg)
- rotateY(45deg)
- rotateZ(45deg)

# Transitions & Animations - Keep Your Users Engaged

- Transitions
- Animations

# Transitions

- Built-in animation.
- Which Properties?
- Initial delay
- How long should it take?
- Timing Function: Start fast, end slow.

# Modern CSS - Because it's constantly evolving!

-

# CSS Modules & Their Working Groups

-

# CSS Variables

- Initialize colours in root.
  :root {
  --my-color: pink;
  }
- var(--my-color);
- variables are re-usable.

# Vendor Prefixes

- Browsers implement new features differently and at different speed.

.container {
display: -webkit-box;
display: -ms-flexbox;
display: -webkit-flex;
display: flex;
}

# Which Prefixes Should You Use?

- css autoprefixer on github
- Autoprefixer CSS online.

# Detecting Browser Support with @supports

- Support Queries
  - Some features just aren't implemented yet in some browsers.
    @supports (display: grid) {
    .container {
    display: grid;
    }
    }

# Polyfills

- A Polyfill is JavaScript Package which enables certain CSS features in Browsers which would not support it otherwise.
- Polyfills come at a cost! The JavaScript has to be loaded and parsed!

# Eliminate Cross-Browser Inconsistencies

- Browsers use different defaults
  - Different margins, paddings...
  - Different box-sizing...
- Use Reset-Library (e.g. Normalize CSS).
- Reset Styles Manually.

# Choosing Class Names Correctly

- Do
  - kebab-case
  - name by feature -> .page-title
- Don't
  - camelCase
  - name by style -> .title-blue

# Block Element Modifier (BEM)

- A uniform and consistent way of naming your CSS classes
<!-- - .block -> welk onderdeel van de site is het?
- \_\_element -> welk object is het?
- --modifier -> welke kleur heeft het? -->
<!-- - .menu-main__item--size-big
- .button\_\_--success -->

# Vanilla CSS vs CSS Frameworks

- Vanilla CSS

  - Write all your styles and layouts on your own.
  - Full Control.
  - No unnecessary code.
  - Name classes as you like.
  - Build everything from Scratch.
  - Danger of "Bad Code".

- Component Frameworks

  - Rapid Development
  - Follow Best Practices
  - No Need to be an Expert
  - No or Little Control
  - Unnecessary Overhead Code
  - All Websites Look the Same

  - Foundation
  - Bootstrap 4
  - Pre-styled components and utility features/ classes.

- Utility Frameworks

  - Faster Development
  - Follow Best Practices
  - No Expert Knowledge Needed
  - Little Control
  - Unnecessary Overhead Code

  - Tailwind CSS
  - Build your own styles and layouts with the help of utility features and classes.

# An Introduction to SASS - CSS On Steroids

-

# What's SASS / SCSS?

- CSS
- SASS (Syntactically Awesome Style Sheets)
  - Does NOT run in the Browser
  - Extends CSS (during Development)
  - Compiled to CSS before Production

# SASS Features

- Nested Rules
- Helper Functions
- Inheritance
- Mixins
- Partials
- Conditions & Loops
- Variables

# SASS Install

- Check out site via Node

# SASS to CSS Conversion

# SASS Improves

- Repetition in code.

# Nesting Selectors - SASS

- SASS is Python like CSS
- SCSS is just CSS Syntax
- Nesting Selectors is putting in selectors inside another one.
- Nesting Selectors are equivalant to descendant selectors in CSS.

# Adding Nested Properties - SASS

- Nested Properties = flex-x any names \*/
  flex: {
  direction: column;
  wrap: nowrap;
  }

# Understanding Variables - SASS

- Handy with repeating colours.
- $main-color: #521751;

# Storing Lists & Maps - SASS

/_ SCSS Variables used for colours, values _/
// $main-color: #521751;
/* Map = Collection of key value pairs (colors) */
$colors: (
main: #521751,
secondary: #fa923f,
);
/_ List = More than 1 value _/
$border-default: 0.05rem solid map-get($colors, main);

# Built-in Functions - SASS

- map-get() -> get key value pair from a map
- background: lighten(map-get($colors, main), 72%);

# Adding Simple Arithmetics - SASS

padding: $size-default _ 3 0; /_ Math with SASS \*/

# Adding Better Import and Partials - SASS

- partials start with \_ = \_variables.scss.
- you can include in many other .scss / .sass files.
- To hide your variables and keep code clean.
  @import "\_variables.scss";
  @import "typography.scss";
- html {
  font-size: 94.75%;

# Media Queries - SASS

/_ Media query for HTML element in SCSS _/
@media (min-width: 40rem) {
font-size: 125%;
}
}

# Understanding Inheritance - SASS

- Check Documentation.

# Adding Mixins - SASS

- Mixins

  - Reusable custom funcions

  /_ mixin your function in scss _/
  @mixin display-flex() {
  display: -webkit-box;
  display: -ms-flexbox;
  display: -webkit-flex;
  display: flex;
  }

@mixin media-min-width($width) {
/_ Media query for HTML element in SCSS _/
@media (min-width: $width) {
@content;
}
}

html {
font-size: 94.75%;

@include media-min-width(40rem) {
font-size: 125%;
}
}

# Using the Ampersand Operator

- Makes pseudo-classes available.
- .documentation-link {
  text-decoration: none;
  color: map-get($colors, main);
  display: block;
  padding: $size-tiny;
  border: $border-default;

  /_ Ampersand operator: makes pseudo-states available _/
  &:hover,
  &:active {
  color: white;
  background: map-get($colors, secondary);
      border-color: map-get($colors, secondary);
  }
  }
