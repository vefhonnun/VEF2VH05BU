# Complex Selectors

### Common Selectors 

| Example  | Classification  | Explanation  |  
|---|---|---|
| h1 | Type Selector | Selects an element by its type |
| .tagline	| Class Selector | Selects an element by the class attribute value, which may be reused multiple times per page |
| #intro | ID Selector |	Selects an element by the ID attribute value, which is unique and to only be used once per page |

### Child Selectors

| Example | Classification | Explanation |
|---|---|---|
| article h2 | Descendant Selector | Selects an element that resides anywhere within an identified ancestor element |
| article > p | Direct Child Selector | Selects an element that resides immediately inside an identified parent element |

### Sibling Selectors 

| Example | Classification | Explanation |
|---|---|---|
| h2 ~ p | General Sibling Selector | Selects an element that follows anywhere after the prior element, in which both elements share the same parent |
| h2 + p | Adjacent Sibling Selector | Selects an element that follows directly after the prior element, in which both elements share the same parent |

### Attribute Selectors 

| Example | Classification | Explanation |
|---|---|---|
| a[target] | Attribute Present Selector | Selects an element if the given attribute is present |
| a[href="http://google.com/"] | Attribute Equals Selector | Selects an element if the given | attribute value exactly matches the value stated |
| a[href*="login"] | Attribute Contains Selector | Selects an element if the given attribute value contains at least once instance of the value stated |
| a[href^="https://"] | Attribute Begins With Selector | Selects an element if the given attribute value begins with the value stated |
| a[href$=".pdf"] | Attribute Ends With Selector | Selects an element if the given attribute value ends with the value stated |
| a[rel~="tag"] | Attribute Spaced Selector | Selects an element if the given attribute value is whitespace-separated with one word being exactly as stated |
| a[lang="en"] | Attribute Hyphenated Selector | Selects an element if the given attribute value is hyphen-separated and begins with the word stated |



#### Bjargir

* [Harmonikkulisti](https://code-boxx.com/simple-responsive-accordion-pure-css/)
* [Pop up Modal](https://codepen.io/imprakash/pen/GgNMXO)


#### Lesefni

* [Shayhowe, Flóknar stílsetningar - Complex Selectors](https://learn.shayhowe.com/advanced-html-css/complex-selectors/)
