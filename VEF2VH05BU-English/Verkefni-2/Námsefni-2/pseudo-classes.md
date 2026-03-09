### Pseudo-classes 

| Example | Classification | Explanation |
|---|---|---|
| a:link | Link Pseudo-class | Selects a link that has not been visited by a user |
| a:visited | Link Pseudo-class | Selects a link that has been visited by a user |
| a:hover | Action Pseudo-class | Selects an element when a user has hovered their cursor over it |
| a:active | Action Pseudo-class | Selects an element when a user has engaged it |
| input:focus | Action Pseudo-class | Selects an element when a user has made it their focus point |
| input:enabled | State Pseudo-class | Selects an element in the default enabled state |
| input:disabled | State Pseudo-class | Selects an element in the disabled state, by way of the disabled attribute |
| input:checked | State Pseudo-class | Selects a checkbox or radio button that has been checked |
| input:indeterminate | State Pseudo-class | Selects a checkbox or radio button that neither been checked or unchecked, leaving it in an indeterminate state |
| li:first-child | Structural Pseudo-class | Selects an element that is the first within a parent |
| li:last-child | Structural Pseudo-class | Selects an element that is the last within a parent |
| div:only-child | Structural Pseudo-class | Selects an element that is the only element within a parent |
| p:first-of-type | Structural Pseudo-class | Selects an element that is the first of its type within a parent |
| p:last-of-type | Structural Pseudo-class | Selects an element that is the last of its type within a parent |
| img:only-of-type | Structural Pseudo-class | Selects an element that is the only of its type within a parent |
| li:nth-child(2n+3) | Structural Pseudo-class | Selects an element that matches the given number or expression, counting all elements from the beginning of the document tree |
| li:nth-last-child(3n+2) | Structural Pseudo-class | Selects an element that matches the given number or expression, counting all elements from the end of the document tree |
| p:nth-of-type(3n) | Structural Pseudo-class | Selects an element that matches the given number or expression, counting only elements of its type from the beginning of the document tree
| p:nth-last-of-type(2n+1) | Structural Pseudo-class | Selects an element that matches the given number or expression, counting only elements of its type from the end of the document tree |
| section:target | Target Pseudo-class | Selects an element whose ID attribute value matches that of the URI fragment identifier |
| div:empty | Empty Pseudo-class | Selects an element that does not contain any children or text nodes |
| div:not(.awesome) | Negation Pseudo-class | Selects an element not represented by the stated argument |

### Pseudo-elements 

| Example | Classification | Explanation |
|---|---|---|
| .alpha:first-letter | Textual Pseudo-elements | Selects the first letter of text within an element |
| .bravo:first-line | Textual Pseudo-elements | Selects the first line of text within an element |
| div:before | Generated Content | Creates a pseudo-element inside the selected element at the beginning |
| a:after | Generated Content | Creates a pseudo-element inside the selected element at the end |
| ::selection | Fragment Pseudo-element | Selects the part of a document which has been selected, or highlighted, by a users’ actions |


