# Spike 1 notes

- As explained on the LMS - the Internet is an **INTER**connected **NET** of computers. **Servers** hold information, and **client** computers can make requests to a server for documents that are then displayed in a browser. We will learn how to build some of those documents.

- HTML = **Hyper Text Markup Language**.

- In a new index.html file, use **!** shortcut to boilerplate.

- **&lt;head&gt;** tag holds:

  - **&lt;title&gt;**: title of the page, will also help with SEO (search engine optimization).
  - **&lt;style&gt;**: can be used to define styles for an html page.
  - **&lt;script&gt;** client-side JavaScript, but it is better to put the JS scripts at the end of the body. This ensures all hard-coded HTML is already mounted before the script starts running.
  - **&lt;link&gt;** links two documents, or links an external source. Most commonly used to link to the CSS stylesheet - use **link:css** to boilerplate.
  - **&lt;meta&gt;** specifies the **character set** (how the computer reads the text), **viewport** settings (how the browser displays the document on your device screen), **page description**, **keywords** and **author** of the document (also relevant for SEO).

- **&lt;body&gt;** holds all our actual website content.

- HTML tags open and close with angled brackets. A single element will usually have an opening and closing tag - closing tag indicated with a forward slash before the element name. eg:

  ```html
  <p>paragraph content</p>
  ```

- Some select HTML elements are self-closing, usually because they hold no content and so two seperate tags are pointless. eg:

  ```html
  <img src="img-source" alt="img alt text" />
  ```

- Many elements will have **attributes** that can modify their look, functionality, or behaviour - class, type, src, etc. This is always in the opening tag.

- **&lt;div&gt;** and **&lt;span&gt;** are like boxes that hold other elements. The only difference is positioning: **&lt;div&gt;** default to **block**, while **&lt;span&gt;** default to **inline**.

- Other elements can be **nested**, such as **&lt;li&gt;** inside **&lt;ul&gt;**. However there are some rules and best-practices that should be followed (eg. **&lt;p&gt;** cannot hold a **&lt;div&gt;**). An [HTML validator](https://validator.w3.org/) will help to prevent these mistakes.

- Dev tools/Inspector can be opened in a browser by right-clicking and selecting **inspect**, or with keyboard shortcuts <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>i</kbd> for Windows, and <kbd>command</kbd> + <kbd>option</kbd> + <kbd>i</kbd> for Mac (I think?).

- **CSS** - Cascading Style Sheet can be linked in the head tag of an HTML document. For your first project, I recommend against using any CSS libraries so you can get to understand the basic ways HTML and CSS interact.

- **Selectors** target the element/s to which the styles will be applied (multiple elements can take the same style specs). I recommend looking up "CSS selectors" on W3Schools. Playing games like [CSS Diner](https://flukeout.github.io/) and [CSS Speedrun](https://css-speedrun.netlify.app/) is a fun way to get in some practise.

- Commonly used:

  - selector = element by type
  - .selector = class
  - #selector = id
  - selector1, selector2 = multiple selectors can be seperated by a comma
  - selector1 > selector2 = all selector2 that are a direct child of a selector1
  - selector1 selector2 = all selector2 nested inside a selector1

- **Pseudo-classes** can be added to selectors to specify that the styles only apply during a special state. Common examples are **:hover**, **:focus**, **:active**.

- **Specificity** determines which selector is the most relevant to an element that has conflicting selectors (ie **.class** is more specific than **type**). **Inline styles** are always highest specificity.

- **Curly braces** surround the style - a **property** that is to be modified, and the **value** of that modification. Property-value pairs must be seperated by a **semi-colon**. eg:

```css
selector {
  color: red;
  font-size: large;
}
```

- CSS **units** can be **relative** (rem, %, vw) or **absolute** (cm, mm, px). Relative values are safer to use for scalability purposes.

- [Project kick-off](https://lms.codeacademyberlin.com/content/web/Module-1/Project-1/Sprint-1#epic2:projectkick-off)
