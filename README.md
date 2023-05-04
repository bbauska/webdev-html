# webdev-html
This HTML course for web developers provides a solid overview for developers, from novice to expert level HTML.

HyperText Markup Language, or HTML, is the standard markup language for describing the structure of documents displayed on the web. HTML consists of a series of elements and attributes which are used to mark up all the components of a document to structure it in a meaningful way.

HTML documents are basically a tree of nodes, including HTML elements and text nodes. HTML elements provide the semantics and formatting for documents, including creating paragraphs, lists and tables, and embedding images and form controls. Each element may have multiple attributes specified. Many elements can have content, including other elements and text. Other elements are empty, with the tag and attributes defining their function.

There are several categories of elements, including 
  - metadata, 
  - sectioning, 
  - text, 
  - inline semantic, 
  - form, 
  - interactive, 
  - media, 
  - component, and 
  - scripting. 

We'll cover most of these in the series. But first, what is an element?

## Elements
HTML consists of a series of elements, which you use to enclose, or wrap, different parts of the content to make it appear or act in a certain way. HTML elements are delineated by tags, written using angle brackets (&lt; and &gt;).

Our page title is a heading, level one, for which we use the &lt;h1&gt; tag. The actual title, "Machine Learning Workshop", is the content of our element. The content goes between the open and closing tags. The entire thing—the opening tag, closing tag, and the content—is the element.
![image](https://user-images.githubusercontent.com/41387907/236105813-d08bcd3d-c6ae-4517-bd48-f11ab85aef4e.png)

The closing tag is the same tag as the opening tag, preceded by a slash.

Elements and tags aren't the exact same thing, though many people use the terms interchangeably. The tag name is the content in the brackets. The tag includes the brackets. In this case, &lt;h1&gt;. An "element" is the opening and closing tags, and all the content between those tags, including nested elements.

```
<p>This paragraph has some
  <strong><em>strongly emphasized</em></strong>
  content</p>
```

This paragraph element has other elements nested in it. When nesting elements, it's important that they are properly nested. HTML tags should be closed in the reverse order of which they were opened. In the above example, notice how the &lt;em&gt; is both opened and closed within the opening and closing &lt;strong&gt; tags, and the &lt;strong&gt; is both open and closed within the &lt;p&gt; tags.

Browsers do not display the tags. The tags are used to interpret the content of the page.

HTML is very, very forgiving. For example, if we omit the closing &lt;/li&gt; tags, the closing tags are implied.

```
<ul>
  <li>Blendan Smooth
  <li>Hoover Sukhdeep
  <li>Toasty McToastface
</ul>
```

Although it is valid to not close an &lt;li&gt;, it isn't good practice. The closing &lt;/ul&gt; is mandatory. If the unordered list's closing tag is omitted, the browser will try to determine where your list and list items end, but you might not agree with the decision.

The specification for each element lists whether the closing tag is mandatory or not. "Neither tag is omissible" in the specification means both an opening tag and a closing tag are required. The specification provides a list of all the required closing tags.

If the &lt;em&gt; or &lt;strong&gt; in the example earlier had not been closed, the browser may or may not close the element for you. Not closing an &lt;em&gt; simply leads to content possibly being rendered differently than you intended. If a &lt;/ul&gt; is omitted and the next tag is a closing tag for the list's parent container, you're lucky. If, on the other hand, it's an opening &lt;h1&gt; tag, the browser will assume the header is part of the list, including inheriting styles. Some omitted closing tags cause bigger issues: not closing some tags, such as &lt;script&gt;, &lt;style&gt;, &lt;template&gt;, &lt;textarea&gt;, and &lt;title&gt;, breaks subsequent content as shown in the following example.

```[html]
<p>If you add <strong>Strong</oops> text and <em>emphasised</doh> text but forget to close your tags, that doesn't cause the worst problems.</ohno>
<p>All that happens is your text continue to be bold and emphasized.</ohno>

<p>But not closing a `style` or `script` is a more serious issue. 
  <p>The script only shows because we changed the display.
  <style>
    p {
      color:red;
    }
    style {
      display: unset;
     }
  <p>text coming after 
  <table>
    <tr>
      <th>Optional closing
    <tr>
      <td>table cell
```

