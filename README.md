# CSS-Style-Guide
A component based CSS style guide taking cues primarily from SMACSS. High-level principals and formatting assumptions are used to balance consistency with flexible decision making. 

## Table of contents
1. [General principles](#general-principles)
  1. [Components](#Components)
  2. [Layout](#Layout)
2. Do's and Don'ts
3. [Formatting](#Format)


<a name="general-principles"></a>
## 1. General principles
Separate components and layout: 
* Define page components as standalone pieces that are unaware of their position or size. 
* Apply a layout layer to position and size components on a page,.

<a name="Components"></a>
####Components
Components are standalone pieces of a page that perform certain functions. For example – a call-to-action tile might highlight a thought or product and offer a "details" link for users to navigate to. (SMACSS classifies these as "modules". BEM classifies them as “Elements”.) 

```html
<div class=”productCallToAction”>
	<header>
		Summer gear
	</header>
	<article>
		<p>Shop from over 850 of the best summer gear we have!</p>
	</article>
	<a class=”details” >Shop summer gear</a> 
</div>
```

Other examples of a components include:
* branded buttons
* call-to-action tiles 
* carousels 
* accordions 
* twitter widgets 
* search bars

<a name="Layout"></a>
##Layout 
The layout portion of theming can be thought of as a layer that scaffolds the page’s higher parent level elements. Eg page header, page footer, main body content, sidebars etc.  (BEM refers to these as "Blocks").This is the appropriate place to define widths and positions.  Parent level elements also house "components" so, for example, a **twitter widget component** might live inside a **side bar parent level element**. This, in a sense, means that the layout layer controls the position and sizing of everything (excluding the guts of a component; that is defined at the component level).

Having the **layout layer** separate from the **defined components** allows developers to be flexible in their choice of implementation. For example, the layout layer can be done entirely with a CSS grid framework like Bootstrap. Or, for the purist (like me), you can code up the layout as a separate section in your CSS.  As long as the components are defined well, they will live amongst the scaffold layout and conform to their parent elements. Follow the Do’s and Don’ts below on how to define components. 





