## Structure web pages with HTML

### New HTML5 Layout elements
HTML5 introduces a new set of elements that allow you to divide up the parts of a page. The names of these elements indicate the kind of content you will find in them. They are still subject to change, but that has not stopped many web page authors using them already.

- Headers & FooTers
  - The <header> and <footer> elements can be used for:
    - The main header or footer that appears at the top or bottom of every page on the site.
    - A header or footer for an individual <article> or <section> within the page.
- Navigation
  - The <nav> element is used to contain the major navigational blocks on the site such as the primary site navigation.
- Articles
  - The <article> element acts as a container for any section of a page that could stand alone and potentially be syndicated.
  - This could be an individual article or blog entry, a comment or forum post, or any other independent piece of content.
- Asides
  - The <aside> element has two purposes, depending on whether it is inside an <article> element or not.
- Sections
  - The <section> element groups related content together, and typically each section would have its own heading.
- Heading groups
  - The purpose of the <hgroup> element is to group together a set of one or more <h1> through <h6> elements so that they are treated as one single heading.
- Figures
  - You already met the <figure> element in Chapter 5 when we looked at images. It can be used to contain any content that is referenced from the main flow of an article (not just images).
  - It is important to note that the article should still make sense if the content of the <figure> element were moved (to another part of the page, or even to a different page altogether).
- Sectioning Elements
  - It may seem strange to follow these new elements by revisiting the <div> element again. (After all, the new elements are often going to be used in its place.)
  - However, the <div> element will remain an important way to group together related elements, because you should not be using these new elements that you have just met for purposes other than those explicitly stated.

### Summary
1. The new HTML5 elements indicate the purpose of different parts of a web page and help to describe its structure.
1. The new elements provide clearer code (compared with using multiple <div> elements).
1. Older browsers that do not understand HTML5 elements need to be told which elements are block-level elements.
1. To make HTML5 elements work in Internet Explorer 8 (and older versions of IE), extra JavaScript is needed, which is available free from Google.
