<!-- HTML Fundamentals: 



0. Document Object Model (DOM) Tree
                 document node:
                 <document> 
                    |
                root element node:
                  <html>
     _______________|_______________________________
    |                                               |
element node:                                   element node:       
  <head>                                          <body>
    |                                               |
element node:                                   element node:    
  <title>                                         <div>
    |                            ___________________|____________
text node:                      |
  "..."                           



1. HTML Document
- HTML: 
    + HyperText <Markup> Language (HTML)
        > markup not displayed 
        > browser interpret markup on how to render the page display
    + HyperText Transport Protocol (HTTP)
    + Universal Resource Identifier (URI)
    + Universal Resource Locator (URL)
- HTML document: 
    + <!DOCTYPE HTML>
        <html>
        <head>
            ...document metadata (browser window)... 
        </head>
        <body>
            ...document content (browser page)...
        </body>
        </html>
- HTML document elements: 
    + <head>
        - <title></title>: element tag that define document title shown in browser's title bar or page's tab
            > attributes/modifiers: <global attributes>
        - <meta>: element tag that define document metadata which cannot be expressed with other elements
            > attributes: <charset|name|content|http-equiv> + <global attributes>
        - <link>: element tag that specifiy relation of external resources(CSS) to document.
            > attributes: <href|rel|media|hreflang|type|sizes|crossorigin|integrity> + <global attributes>
            > <rel=(alternate/author/dns-prefetch/help/icon/license/next/pingback/preconnect/prefetch/preload/prerender/prev/search/stylesheet)>
            > ~<body> 
            <a></a> (similar to but NOT the same)
            </body> 
        - <script></script>: element tag that allow inline/linked JS scripts
            > attributes: <async|type|defer|src|charset|integrity|text|language|defer|crossorigin> + <global attributes> 
        - <style></style>: element tag that embed CSS style information in documents 
            > attributes: <media|type|title> + <global attrbutes>
        - <base>: element tag that specify URL which non-absolute URLs are relative to
            > attributes: <global attributes>
    </head>
    + <body>
        - <element>
            > <block-elements>: always start on new line & takes up full width available 
            > <inline-elements>: do not start on new line & take up as width as necessary 
        - text: 
            > general text display
        - link: 
            > linking to documents (sourced anchor)
            > linking within documents (targeted anchor)
        - list
            > unordered list (modern list document format implication) 
            > ordered list (modern list document format implication) 
            > description list (modern list document format implication)
        - table: 
            > used ONLY for data/database display (NOT used for document formatting)
        - media: 
            > display picture/images
            > display audio
            > display video
        - form: 
            > allow interactive user input 
    </body>
- HTML layout/semantics elements: 
    + <!DOCTYPE HTML>
        <html>
        <head>
            ...document metadata (browser window)...
        </head>
        <body>
        - <main>: tag specify the main content of a document with ONLY 1 main element/doc
            + do NOT contribute to the document's outline (strictly informative)
            + must NOT be descendant of <header>, <nav>, <article>, <aside>, <footer>
        - <header>: define a header for a document or a section
            + <nav>: define a container for navigation links
        - <nav>: define a container for navigation links
        - <section>: define a section in a document
        - <article>: define an independent self-contained article
            + scenarios: <section>     <article>      <section>        <article>
                            <article>       <section>       <section>       <article>         
        - <aside>: define content aside from the content (like a sidebar)
            + <nav>: define a container for navigation links
        - <details>: define additional details
            + <summary>: define a heading for the <details> element as toggled disclosure widget
        - <mark>: define marked/highlighted text
        - <figure>: specify self-contained image content
            + <figcaption> define a caption for a <figure> element
        - <time>: define a date/time
        - <footer>: define a footer for a document or a section
            + <nav>: define a container for navigation links    
        </body>
        </html>
- HTML nonsematics elements: 
    + block elements: 
        - <div></div>: generic container/section with no semantic meaning which can be used for group styling & should be used only when no other semantic element is appropriate 
            > attributes: <global attributes>
            > can nest other block/inline elements
    + inline elements:
        - <span></span>: generic inline container with no semantic meaning which can be used for group styling & should be used only when no other semantic element is appropriate
            > attributes: <global attributes>
            > can nest ONLY other inline elements
    + ...
-  HTML element <global attributes>: 
    + <element_tag class>: specify a classname for an element 
        > each element tag allow >= 1 classes separated by " "
    + <element_tag id>: specify a unique ID for an element 
        > each element tag allow only 1 unique ID 
    + <element_tag title>: specify extra text info about an element 
    + <element_tag style>: specify an inline style for an element 
    + <element_tag lang>: specify a language code for an element code 
    + <element_tag spellcheck>: specify if element's option for spelling & grammer checked 
    + <element_tag accesskey>: specify a keyboard shortcut to access an element
    + <element_tag ...>


2. <html><body> Text </body></html>
- block elements:
    + <p></p>: element tag for paragraph of text content 
        > attributes: <global attributes>
    + <h1></h1>: primary heading element tag for current section
    + <h2...h6></h2...h6>: secondary heading element tag for current section
        > attributes: <global attributes>
    + <pre></pre>: element tag for block of preformatted text
        > attributes: <global attributes>
    + <hr>: element tag for paragraph-level thematic break
        > attributes: <global attributes>
    + <blockquote></blockquote>: block quotation from another source
        > attributes: <cite> + <global attributes>
- inline elements: 
    + <textarea></textarea>: element tag for Multiline free-form text input. 
        >  attributes: <autocomplete|autofocus|cols|disabled|dirname|form|name|readonly|required|rows|maxlength|minlength|placeholder|wrap|selectionDirection|selectionEnd|selectionStart|spellcheck> + <global attributes>
    + <br>: element tag for line break
        > attributes: <global attributes>
    + <sub></sub>: element tag for subscript text
        > attributes: <global attributes>
    + <sup></sup>: element tag for superscript text
        > attributes: <global attributes>
    + <cite></cite>: element tag for reference to a work title
        > attributes: <global attributes>
    + <q></q>: indicates a short inline quotation from another source
        > attributes: <cite> + <global attributes>
    + <abbr></abbr>:  represents an abbreviation and optionally provides a full description for it
        > attributes: <global attributes>  
    + <code></code>: represents a fragment of computer code
        > attributes: <global attributes>
    + <samp></samp>: represent a sample output from computer program. 
        > attributes: <global attributes>    
    + <kbd></kbd>: represents user input (usually keyboard) for a program
        > attributes: <global attributes>
    + <var></var>: represents a variable in a mathematical expression /  programming context
        > attributes: <global attributes>
    + &<character_entities>: reserved characters in HTML
        > &nbsp;    : 	non-breaking space
        > &lt;      :   less than <
        > &gt;      :   greater than >
        > &quot;    : 	double quotation mark "
        > &apos;    :   single quotation mark (apostrophe) ' 
        > &amp;     :   ampersand & 
        > &copy;    :   copyright ©
        > &reg;     :   registered trademark ®



3. <html><body> Link </body></html>
- block elements: 
    + <N/A>
- inline elements: 
    + Hyperlink: hypertext anchor 
        - <a></a>: element tag that define a hypertext anchor/hyperlink to a location on the same page/any other page on the Web.
            > attributes: <href|hreflang|media|rel|target|type|download|ping|referrerpolicy> + <global attributes> 
            > <rel=(alternate/author/bookmark/external/help/license/next/nofollow/noreferrer/noopener/prev/search/tag)>      
            > <target=(_self/_blank/_parent/_top)>      
    + Linking to documents: sourced anchor
        - external web address: <a href="http://absoluteURL">link text</a>
        - internal web address: <a href="./relativeURL">link text</a>
    + Linking within document: targeted anchor
        - named (explicit) anchor by local reference: <a href="#location">link text</a> + <a name="location"></a>
        - implicit anchor by id global attribute: <div id="location">link text</div>
    + Linking to documents'anchor: sourced anchor + targeted anchor
        - <a href="http://absoluteURL#location">link text</a>
        - <a href="./relativeURL#location">link text</a>
    + Link other metadata attributes: 
        - <global attributes> language: <a href="..." lang="...">
        - <global attributes> access key: <a href="..." accesskey="...">
        - relationship between current & linked: <a href="..." rel="...">
        - document content type: <a href="..." type="...">
        - target link open: <a href="..." target="_self/_blank/_parent/_top">
        - links security measure: <a href="..." rel="noreferrer noopener">



4. <html><body> List </body></html>
- block elements: 
    + unordered list: unordered list of items typically displayed with a bullet/dot/circle/squared. 
        - <ul>
            <li>...</li>
            ...
            <li>...</li>
        </ul>
    + ordered list: ordered list of items typically displayed with a preceding numbering which can be any form like numerals/letters/Romans numerals/even simple bullets.
        - <ol>
            <li>...</li>
            ...
            <li>...</li>
        </ol>
    + description list: encloses a list of pairs of terms and descriptions. 
        - <dl>
            <dt>...</dt> 
            <dd>...<dd>
            ...
            <dt>...</dt>
            <dd>...<dd>
        </dl>
    + <ul></ul>: unordered list
        > attributes: <global attributes>
    + <ol></ol>: ordered list
        > attributes: <start|reversed|type> + <global attributes>
    + <li></li>:used to represent an item in a list
        > attributes: <value> + <global attributes>
    + <dl></dl>:  description list
        > attributes: <global attributes>
    + <dt></dt>: term/name part of a term-description group
        > attributes: <global attributes>
    + <dd><dd>: description/definition/value part of a term- description group
        > attributes: <global attributes>
- inline elements: 
    + <N/A>



5. <html><body> Table </body></html> 
- block elements: 
    + table: tabular data information expressed via >=2 dimensions using <tr>: <th>/<td> table row basis
        - <table>
            <thead>
            <tr>
            <th>colHeading1</th>...<th>colHeadingN</th>
            </tr>
            </thead>

            <tbody>
            <tr>
            <td>colCell1</td>...<td>colCellN</td>
            </tr>
            ...
            <tr>
            <td>colCell1</td>...<td>colCellN</td>
            </tr>
            </tbody>

            <tfoot>
            <tr>
            <td>colSummary1</td>...<td>colSummaryN</td>
            </tr>
            </tfoot>
        </table>
    + <table></table>: table element tag 
        > attributes: <summary> + <global attributes>
    + <caption></caption>: table title that represents title of a table 
        > attributes: <global attributes>
    + <thead></thead>: table header defines a set of rows defining the head of the columns of the table
        > attributes: <global attributes>
    +  <tbody></tbody>: table body defines >=1 <tr> element tag to be the body of its parent <table> element
        > attributes: <global attributes>
    + <tfoot></tfoot>: table footer defines a set of rows summarizing the columns of the table as aggregate values 
        > attributes: <global attributes>
    + <tr></tr>: table row of cells that define a row of cells in a table which can be either: row of <th> | <th colspan> | <td> | <td colspan|rowspan> elements
        > attributes: <global attributes>
- inline elements: 
    + <th></th>: table header cell that define a cell as a header for a group of cells of a table
        > attributes: <colspan|rowspan|headers> + <global attributes>
    + <td></td>: table cell that define a cell of a table that contains data
        > attributes: <colspan|rowspan|headers> + <global attributes>


6. <html><body> Media </body></html>
- block elements: 
    + picture: element tag used to embed image content which holds two different tags: one or more <source> tags and one <img> tag.
        - <picture>
            <source>
            ...
            <source>
            <img>
        </picture>
    + audio: element tag used to embed sound content in a document which can contain one or more audio sources.
        - <audio>
            <source>
            ...
            <source>
        </audio>
    + video: element tag to embed video content in a document which can contain one or more video sources.  
        - <video>
            <source>
            ...
            <source>
        </video>
    + <audio></audio>: audio element tag
        > attributes: <autoplay|buffered|preload|loop|controls|src|muted|played|volume> + <global attributes> 
    + <video></video>: video element tag
        > attributes: <autoplay|controls|height|loop|poster|preload|src|width|buffered|crossorigin|muted|played> + <global attributes>        
- inline elements: 
    + <img>: image element tag represents an image in the document
        > attributes: <alt|src|height|ismap|usemap|width|crossorigin|longdesc|referrerpolicy|sizes|srcset> + <global attributes>
    + <source>: empty element tag that offer the same media content in multiple file formats in order to provide compatibility for either <picture>/<audio>/<video> element (NOT block/inline)
        > attributes: <media|src|type|sizes|srcset> + <global attributes>



7. <html><body> Form </body></html>
- block elements: 
    + form: element tag for document section that contains interactive controls to submit information to a web server which used to create an HTML form for user input.
        - <form>
            <fieldset>
            <legend>Title</legend>
            <input><label>...</label>
            </fieldset>
        </form>
    + <form></form>: form element tag
        > attributes: <action|autocomplete|name|novalidate|accept-charset|enctype|method|target(_self|_blank|_parent|_top)> + <global attributes>
    + <fieldset></fieldset>: 
- inline elements: 
    + <input>: 
    + <legend></legend>: 
    + <label></label>: 


8. HTML Accessibility  
- https://caniuse.com/ -->
