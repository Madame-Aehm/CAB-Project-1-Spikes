# Spike 1 notes

- As explained on the LMS - the Internet is an INTERconnected NET of computers. Servers hold information, and client computers can make requests and recieve documents in return that can then be viewed in a browser. We will learn how to build some of those documents.

- HTML = Hyper Text Markup Language.

- In a new html file, use **!** shortcut to boilerplate.

- <head> tag holds:
  - <title> title of the page, will also help with SEO (search engine optimization)
  - <style> can be used to define styles for an html page.
  - <script> client-side JavaScript, but it is better to put the JS scripts at the end of the body. This ensures all hard-coded HTML is already mounted before the script starts running.
  -	<link> links two documents, or links an external source. Most commonly used to link to the CSS stylesheet - use link:css to boilerplate.
  -	<meta> specifies the character set (how the computer reads the text), viewport settings (the the browser displays on your device screen), page description, keywords and author of the document (also relevant for SEO).

- <body> holds all our actual website content.

- HTML tags open and close with angled brackets. A single element will usually have an opening and closing tag - closing tag indicated with a forward slash before the element name.

- Some select HTML elements are self closing, usually because they hold no content and so two seperate tags are pointless.

- Some examples of regular tags (h1, p), and self-closing (img).

- Many elements will have attributes that can modify their look, functionality, or behaviour - class, type, src, etc. This is always in the opening tag.

- <div> and <span> elements hold other elements like boxes. Difference is whether they position inline or block.

- Other nested elements, show ul as example. Some elements are not to be nested inside others (eg. p > div).

- Dev tools/Inspector

- CSS - Cascading Style Sheet can be linked in the head tag of an html document. Recommend against using any CSS libraries for the first project so they can get to understand the basic ways HTML and CSS interact.

- Selector targets the element/s to which the styles will be applied (multiple elements can take the same style instructions). Recommend looking up selectors on W3Schools, and playing CSS Diner.

- Commonly used:

  - selector = element by type
  - .selector = classname
  - #selector = id
  - selector1, selector2 = multiple selectors can be seperated by a comma
  - selector1 > selector2 = all selector2 as direct child of a selector1
  - selector1 selector2 = all selector2 nested inside a selector1

- Pseudo-classes can be added to selectors to specify that the styles only apply during a special state. Common examples are :hover, :focus, :active.

- Specificity determines which selector is the most relevant to an element that has conflicting selectors (ie .class is more specific than type). Inline styles are always highest specificity.

- Curly braces surround the style specifications - a property that is to be modified, and the value of that modification: property: value. Property-value pairs must be seperated by a semi-colon.

- CSS units - relative (rem, %, vw) and absolute (cm, mm, px). Recommend using relative values for scalability

- Validator demo - https://validator.w3.org/

- Project kick-off slides: https://docs.google.com/presentation/d/1tXoWvfL2OQvxMnJJTIayL_1n0UPS0mDfW2mgJX2rzp8/edit#slide=id.g25f6af9dd6_0_0
