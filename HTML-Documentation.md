# HTML - Hyper Text Markup Language

## What is HTML?

    HTML Stands for Hyper Text Markup Language(HTML), defines the structure and the meaning of content on a web page.

    It helps us to defines things such as 
        -headings
        -paragraphs
        -images
        -links
        -lists
        -tables
        -forms
        -buttons
        -videos
        -sections

    It focus on the what the content is and how it is structured.

    It is not a Programming Language it is a **Markup Language**.Because it does not have any concepts such as the conditions,loops or functions in the programming like.

    ### HyperText

        HyperText means that can connect to other information through links.

        example:

            <a href="https://www.google.com">Visit Example</a>

            when we click the visit example.The browser takes you to another page.

            here , the idea is 

                Document 1 -----> Document 2 
                            link
    ### Markup Language

        Markup means adding special symbols/tags/labels/information to normal content to give that content meaning or structure.

        example:

            if we write the code like this

                ```Welcome to the page```

            the browser cannnot understand it is a heading,paragraphs or anyother ,so we need markup.

            ```
            <h1>Welcome to the page</h1>

            ```

    ### Language

        A language is a way of communicating information using the rules.

        rules such as:
            -how elements are writte
            -how elements are nested
            -what elements mean
            -what attributes can be used
            -how document is structured
    

    ### example html code:

    ```
     <!DOCTYPE html>  ---> defines this document is an HTML5 document.
        <html>  --->  root element of an HTML page

            <head>  ---> contains the meta information about the html page
                <title>Page Title</title>  --->shows in the browser's title bar or in the page's tab
            </head>

            <body>  ---> container for all the visible contents like headings,paragraphs,tables etc...

            <h1>My First Heading</h1>  ---> heading element
            <p>My first paragraph.</p>  ---> paragraph element

            </body>

        </html> 

    ```

    # What Tech is used before the html

        Before HTML, there wasn't one single technology that was simply replaced by the HTML.

        Time line:

            1960s -1980s
                1.plain text files
                2.SGML
                3.Other document systems
                           V
                       1989 -1991
                           V
                          HTML
                           v
                          WWW
                           v
                        Web browsers

        ### 1. Plain text:
            simplest ways computers stored information was as plain text. 

            example:
                My notes    

                Introduction 

                This document explains Computer networks.

                chapter 1

            The computer knows this is a text,but 
            
            it doesn't know 
                - "My notes" is a title
                - "Introduction" is a heading
                - which is paragraph?
                

        ### 2.SGML - Standard Generalized Markup Language

            SGML was created to provide a standard way of describing the structure of the documents.

            it gives the idea of using markup to describe document structure.

            example:

                document
                ├── title
                ├── section
                │    ├── heading
                │    └── paragraph
                └── section

            HTML was influenced by SGML.

            But unlike the SGML,HTML was created for sharing the documents on the www.

        ### HTML

            In 1989, Tim Berners-Lee proposed the idea of the World Web Web while working at the CERN(European Organization for Nuclear Research).

            In 1990-1991, he had develped the basic pieces needed for the web including:
                -HTML
                -HTTP
                -URL/URI concepts
                -The first web server
                -The first web browser

        ### Problems faced:

            1.Documents were isolated

                Computer 1 ---> Document 1 
                Computer 2 ---> Document 2
                Computer 3 ---> Document 3

            2.Different computer systems used different formats

                System A ---> Format A
                System B ---> Format B
                System C ---> Format C

            3.Information was difficult to connect 

            My notes
            |
            └── References
                    |
                    ├── Document 1
                    ├── Document 2
                    └── Document 3
            The information was related, but there wasn't a universal system where you could simply go to the related document.

            4.Information was difficult to find

            At the time, Organizations had information spread across:
                -different computers
                -different networks
                -different document systems
                -different locations
                -different people

            here the problem was not that information didn't exists.

            The problem was make all this information easily accessible and connected.

        ### Proposed solution:
            ***Web***
                The important idea wasn't just creating the HTML,that was creating the system that allows information on different computers to be connected and accessed easily.

                This led to the fundamental pieces of the Web


                      World Wide Web
                            V
                    HTML    URL    HTTP
                     v       v       v
                Structure  Address  Communication
                    |         |           |
                     ----------------------
                            Web Browser

                HTML 
                    Describes the structure and meaning of a document.

                URL - Uniform Resource Locator

                    Identifies where a resource can be found.

                    a url is basically an address used to locate a resource on a network,especially on a web.

                    example: https://www.amazon.com/products/shoes?id=10

                    URL contains:   
                        https - protocol for communication (TLS)
                        www.amazon.com - host or domain
                        /products/shoes -path
                        ?id=10 - query string,additional parameters to the server

                HTTP - Hyper Text Transfer Protocol

                    Defines how the browser and the server communicate to request and receive the resources.

                    Browser                         Server
                    │                              │
                    │────── HTTP Request ─────────>│
                    │                              │
                    │<───── HTTP Response ─────────│
                    │                              │

                    The browser is usually a client.
                    The computer/service providing the resource is the server.

                    Commonly used Protocol
                        1.HTTP  ---> http://
                        2.HTTPS  ---> https://

                    HTTP
                        Communication uses the HTTP without TLS encryption.

                    HTTPS
                        The communication between the browser and the server is protected by an encrypted TLS connection.

                    TLS - Transport Layer Security
                        TLS is a security protocol that protects data while it travels between your browser and a server.

                        When we log in to a website and send without TLS encrytion,someone can intercept the network traffic can potentially see the information.

                            username: dinesh
                            password: mypassword

                            Browser ────────────────> Server
                                        username
                                        password

                        With TLS 
                            Browser ──> encrypted ──> Server

                        ### what TLS provide
                            TLS mainly provides three important security properties.

                                1.Encryption:
                                    It prevents others from easily reading the data traveling between the browser and the server.

                                    Original :hello World
                                    
                                    Browser (Encrypted) --->server(decrypts it).

                                    Encrypted ---> 8fA$2x#91...kL@7
                                    Decrypts  ---> hello World

                                2.Integrity
                                    TLS helps ensure that the data wasn't modified while traveling.
                                    
                                3.Authentication
                                    TLS helps the browser verify that it is communicating with the intended website/server.

                                    https://amazon.com

                                    The server presents a digital certificate.

                                    The certificate helps establish that the server is authorized for example.com.

                Browser
                    Reads the HTML and present the document to the user.

        ### What happens when we enter the URL

            work flow:

            example URL: https://amazon.com/index.html

            1.Enter the URL
                    v
            2.Browser interprets URL
                    V
            3.DNS finds server IP address
                    V
            4.Browser establishes connection
                    V
            5.Browser sends HTTP request
                    V
            6.Server Processes request
                    V
            7.Server Sends the HTTP response
                    V
            8.Browser receives the HTML
                    V
            9.Browser parses HTML
                    v
            10.Browser builds the page 


        ### What happens when you visit HTTPS?

            example URL --> https://example.com

            process:    

            1. Browser reads URL
                    V
            2. DNS finds server IP
                    V
            3. Connection is established
                    V
            4. TLS handshake happens
                    V
            5. Browser and server establish encryption
                    V
            6. HTTP request is sent through the secure TLS connection
                    V
            7. Server sends HTTP response through TLS
                    V
            8. Browser receives and processes the HTML

        ###             TLS Handshake
                            V
            Browser ─────────────────── Server
                            V
                    Secure connection
                            V
                        HTTP messages

            TLS - Transport Layer Security

            Before securely exchanging normal data,the browser and server need to establish the secure connection.

            The initial process is called the TLS handshake.

            Browser                         Server
                │                              │
                │──── Hello ─────────────────>│
                │                              │
                │<── Certificate ──────────────│
                │                              │
                │──── Key exchange ───────────>│
                │                              │
                │<── Secure communication ─────│
                │                              │
                │════ Encrypted HTTP data ════│

            TLS CERTIFICATE

                A Certificate is a digitally signed document that helps establish the identity of a server/domain.

                URL - amazon.com

                TLS Certificate
                    V
                Trusted Certificate Authority
                    V
                Browser can verify the certificate

                The browser checks the certificate and other TLS information before trusting the connection.

            ### What is SSL?

                -SSL (Secure Socket Layer) used before the TLS.
                -The modern web application used the SSL.
                -Basically SSL replaced by the TLS

        
# How does a browser render a web page?

    We take the example URL - https://amazon.com

    1.URL - https://amazon.com

        Browser needs to find the server associated with that domain.

    2.DNS finds the server

        The browser needs an IP address to communicate with the server.

        for example:
            www.amazon.com
                V
               DNS
                V
            93.232.223.465 (IP addresss )

    3. The Browser establishes the connection

        The browser establish the connection securely using the TLS

        BROWSER ---------------> SERVER
                  TLS handshake

    4.Browser sends an HTTPS request

        The browser asks the server for the resource.

        example:
            GET / HTTP/1.1
            HOST: amazon.com

    5.Server Sends an HTTPS response

        The server responds.

        example:
            HTTP/1.1 200 OK
            Content-Type: text/html

            then it sends:
                <!DOCTYPE html>

                <html>

                    <head>
                        <title>My Website</title>
                    </head>

                    <body>
                        <h1>Hello World</h1>
                        <p>Welcome to my website.</p>
                    </body>

                </html>

            Now the browser has received the HTML.The browser has to understand and process it.

    6.Browser parse the HTML

        The browser has an HTML parser.
        It reads the HTML and understand the elements.

        example:
            <h1>Hello World</h1>
            <p>Welcome to my website.</p>

            The browser recognizes that 
                -<h1> is the heading and 
                -<p> is the paragraph
        
        Then it builds a tree-like structure called DOM (Document Object Model).

        <h1>Hello World</h1>
        <p>Welcome to my website.</p> is just a text received from the server.

        The browser converts that text into objects/nodes that programs can work with.

        HTML Text ===> HTML Parser ===> DOM.

        JavaScript can then interact with the DOM.JS changes the DOM, and the browser can update what you see.


        7.Browser also downloads CSS

            Suppose the HTML contains:
                <link rel="Stylesheet" href="style.css">

            after seeing the style.css the browser sends the requests then the server returns,

            h1 {
                color: blue;
                font-size: 40px;
            }

            p {
                color: gray;
            }

            
            The browser parses this CSS.

            It creates another structure called the CSSOM.
            CSSOM ==> CSS Object Model

            work flow:
                CSS ==> CSS Parser ==> CSSOM

                we now have:

                    HTML ==> DOM
                    CSS ==> CSSOM

        8.Browser combines DOM + CSSOM

            Now the browser knows HTML and CSS

            It combines the relevent information to create what is called the Render Tree

            DOM + CSSOM = Render Tree

            The render tree contains the information needed for displaying the visible page.

        9.Layout

            Now the browser needs to find where should everthing appear on the screen?

            The browser calculate the thingd such as 
                - x positions 
                - y positions
                - width 
                - height
                
            example:
                h1
                x = 100px
                y = 50 px
                width = 300 px
                height = 48 px

            This process is called the Layout.


        10. Paint

            Now the browser knows where everything should be.

            It needs to actually draw the pixels.

            examples:
                Text
                Background
                Borders
                Images
                Shadows
            The browser creates drawing commands for these visual elements.

            This is called the Paint.


        11.Compositing

            Modern browsers often divide the page into differnt layers.

            Those layerscan be processed and combined efficiently.

            example:
                Layer 1 --> Background
                Layer 2 --> Page content
                Layer 3 --> Animation
                Layer 4 --> Fixed Element

            The combining of the layers to produce the final image called compositing.


        12. Displays the final view.

# HTML Versions
    
    1.HTML - 1991:
    
        Tim Berners-Lee created the first version of HTML while developing the WWW at CERN.

        Purpose:
            The original goal was to allow researchers to create documents containing:
                - headings
                -paragraphs
                -lists
                -links
                -references
            and connect those document together using the hyperlinks.

        Example:
            A very simple document

            <h1>My Research</h1>
            <p>This is a very simple para</p>
            <a href="other.html">Read another document</a>

        Use cases:
            Sharing and linking scientific/information documents across the early Web.

    2.HTML 2.0 - 1992:

        HTML 2.O was the first formal HTML specification standardized through the IETF.

        IETF -The Internet Engineering Task Force (IETF) is an open, volunteer-driven standards organization that develops and promotes foundational technical standards for the Internet.

        It is essentially documented and standardized the HTML features that had developed in the early Web.

        Purpose:
            HTML 2.0 includes/support standardized concepts such as 
                - headings
                - paragraphs
                - lists
                - hyperlinks
                - images
                - forms
                - tables-related capabilities were limited.

        Use cases:
            The Web started moving beyond Read documents toward Interact with websites.

            Forms were particularly important ,they allowed users to send information to a server.

    3.HTML 3.2 - 1997

        HTML 3.2 was developed under the W3C (The World Wide Web Consortium).

        By this time ,browsers were becoming more capable and websites were becoming more visually sophisticated,HTML 3.2 standardized many features that browsers had introduced.

        Purpose:
            notable additions/standardizations were:
                -table
                -apples
                -text alignment
                -background colors
                -fonts-related presentation features
                -scripting support
                -improved forms

        use cases:
            Web pages were moving toward visually formatted pages.

        Problem:
            HTML was increasingly being used for the presentation, not just structure.
            
            For example,developers started using the HTML to control things like font,color,alignment,background.

            This eventually contributed to the need for CSS to handle presentation separately.

    4.HTML 4.0 - 1997

        HTML 4.0 was a major step forward.

        it focused more strongly on: 
            -separating structure from presentation
            -scripting
            -accessibility
            -internationalization
            -forms
            -stylesheets
            -frames

        Purpose:
            >CSS integration
                HTML 4 encouraged using the CSS for presentation.

                instead of 

                    <font color='red'>
                        Hello
                    </font>

                we can use  

                    <p class='Important'>
                        Hello
                    </p>
                This was a very important architectural change.

            >HTML 4 also provides stronger support fot the scripting through

                <script>
                    //javascript code
                </script>

                Helped the pages interactive.

            >Frames
                HTML 4 supports frames,Frames allowed a browser window to be divided into multiple documents.

                later frames became obsolete and are no longer part of the modern HTML.

        Use cases:
            Website were becoming the structure,Presentation,Behavior.
            This separation is still fundamental to web development today.

        
    5.HTML - 2014

        HTML5 was a major evolution of HTML.

        It was designed around the need of modern Web applications.

        It introduced or standardized many important features.

        Features:
            >Semantic elements:
                HTML5 introduced semantic elements such as:
                    <header>
                    <nav>
                    <main>
                    <section>
                    <article>
                    <aside>
                    <footer>

            >Audio and Video
                Before HTML5, Playing multimedia often depended on browser plugins such as Flash.HTML 5 introduces the native elements:

                <audio controls>
                    <source src="music.mp3">
                </audio>

                <video controls>
                    <source src="movie.mp4">
                </video>

                problem solved:
                    removes the plugins

            >Canvas 
                HTML5 introduced the <canvas> element.
                    <canvas></canvas>

                Javascript can use it to draw graphics.

                Uses:
                    -games
                    -charts
                    -drawing applications
                    -animations
                    -visualizations

            >SVG 
                Modern HTML supports SVG(Scalable Vector Graphics) for vector graphics.

                Purpose:
                    -icons
                    -diagram
                    -logos
                    -scalable graphics

            >Better forms
                HTML5 introduced many useful form input types.

                example:
                    <input type="email">

                    <input type="date">

                    <input type="number">

                    <input type="range">

                    <input type="search">

                    <input type="url">

                Purpose:
                    It also introduced built-in validation capabilities.

                    like <input type="email" required>
                    This makes that the browser can check whether the user entered something that looks like an email address.

            >New Structural elements
                HTML5 introduced elements such as:
                    <figure>
                    <figcaption>
                    <details>
                    <summary>
                    <mark>
                    <time>

    # What happened after HTML5?

        HTML5 is the latest version of HTML.


# Elements

    The HTML elements is a building block of a web page.

    HTML tags are not case sensitive ( <p> and <P> are same).

    syntax:
        <tagname>Content</tagname>

    example:
        <h1>heading</h1> --> HTML Element
        here:
            <h1> --> is a opening tag
            heading --> is a content
            </h1> --> is a closeing tag


    ## Nested HTML elements

        HTML elements can be nested.

        example:
        <html>   --> root element that defines the whole HTML document

            <body>  --> defines the document's body

                <h1>Heading</h1>
                <p>Paragraph</p>

            </body>

        </html>

    ## Empty HTML Elements

        HTML elements with no contents ,and is an empty elements without a closing tag.

        examples:
            <br> --> sigle line break 
            <hr> --> give a horizontal line
            <img> --> insert the image into the document
            <input> --> get the input using the web based forms

    ## Parent and child elements

        Parent Element: The outer element that contains other elements.
        Child Element: The immediate inner element contained directly inside a parent element.

        <body> --> parent element

            <h1>heading</h1>  -->child element
            <p>Paragraph</p>

        </body>

    ## HTML Tags

        An HTML tag is a hidden keyword enclosed in brackets (< and >) that format and display content

        exapmles:
            <!--...--> --> used for commenting
            <!DOCTYPE> --> used for document type 
            <a> --> used for hyperlink
            <b> --> bold
            <p> --> Paragraph
            <body> --> defines document's body
            <br> --> single line break
            <button> --> creates a clickable button

            <h1> - </h1> --> used to defines the font size
            <h2> - </h2>
            <h3> - </h3>
            <h4> - </h4>
            <h5> - </h5>
            <h6> - </h6>

            <img> --> helps to insert the images
            <div> --> division Tag


    ## Two types of elements

        In HTML , elements are broadly categorized into two types based on how they display in the document layout.

            1.Block level Elements:
                Block level elements start on a new line,occupy the fully available width,stack vertically and can contains both block level and inline elements.

            examples:
                <div>: A general-purpose container for other elements.

                <p>: Defines a paragraph.

                <h1>, <h2>, ..., <h6>: Heading elements of different levels.

                <ol>, <ul>: Ordered and unordered lists.

                <table>: Defines a table.

                <form>: Used for HTML forms to collect user inputs.

                <section>, <article>, <nav>, <aside>, <header>,<footer>: Semantic elements that define areas of a webpage.

                code:

                <!DOCTYPE html>
                    <html>
                    <body>

                        <h1>Student Information</h1>        ---> block

                        <p>Name: Dinesh</p>        ---> block

                        <p>Course: Artificial Intelligence and Data Science</p>        ---> block

                        <div>        ---> block
                            This is a block-level div.
                        </div>

                        <div>        ---> block
                            This is another block-level div.
                        </div>

                    </body>
                    </html>

                    Block-level elements are used to structure the page into separate sections or blocks of content.

            2.Inline Elements:
                Inline elements do not start on a new line,take only the width of their content,and are used within the block-level elements to add or style content.
                
            examples:
            <span>: A general-purpose inline container for phrasing content.
            
            <a>: Creates hyperlinks.

            <img>: Embeds an image.

            <strong>, <b>: Used for strong emphasis and bold text, respectively.

            <em>, <i>: Used for emphasis and italic text, respectively.

            <br>: Inserts a line break within text.

            <input>: Creates interactive controls for forms.

            code:

                <!DOCTYPE html>
                <html>
                    <body>

                        <p>
                            I am learning
                            <strong>HTML</strong> ---> Stays on the same line as the surrounding text.
                            and
                            <em>CSS</em>.
                        </p>

                        <p>
                            This is <b>bold</b> text.
                        </p>

                        <p>
                            This is <i>italic</i> text.
                        </p>

                        <p>
                            Visit <a href="https://www.google.com">Google</a>.
                        </p>

                        <p>
                            This is <mark>highlighted</mark> text.
                        </p>

                        <p>
                            This is <small>small</small> text.
                        </p>

                        <p>
                            Water formula is H<sub>2</sub>O.
                        </p>

                        <p>
                            10<sup>2</sup> = 100.
                        </p>

                    </body>
                </html>

# Attributes

    They provide additional information about the HTML elements.
     
    They specify only in the start tag.

    They must be in name='value'

    syntax:

    <tag attribute="value">Content</tag>


    exapmles:

        > href attribute

            <a href='https://www.amazon.com'>Visit Amazon</a>

            here,href is an attribute

        >src attribute

            <img src='sample_image.jpg'> -->src helps to insert the images

            <img src='sample_image.jpg' width-'500 height='600'> 
            
            here,the <img> tag should also contains the width and height

        >alt attribute

            alt attribute for the <img> tag specifies an alternative text for an image.

            <img src='smaple.jpg' alt="bike on road">
        
        >Style attribute

            used to add style to an element,such as color,font,size and more.

            <p style="color:red;">This is a red Paragrap.</p>

        >lang attribute

            lang attribute always include inside the <html> tag to declare the language of the web page.

            <!DOCTYPE html>
            <html lang='en'>  --> to mention the language type.

        >title attribute

            The title attribute defines some extra information about an element.

            the value of the attribute displayed as a tooltip when you mouse over the element.

            <p title='iam a car'>BMW</p> 

            
        
    ## Ways to specify the URL in src attribute

    1.Absolute URL
        links to an external image that is hosted on another website.

    2.Relative URL
        links to an image that is hosted within the website

    ## More attributes

    1.Basic attributes
        >id
        >class
        >style
        >title
        >hidden

        example:
            <p id='intro' class='text' title='Introduction'>Hello</p>

    B.Link attributes
        >href
        >target
        >rel
        >download

        example:
            <a href='about.html' target='_blank'>About </a>

    C.Image attributes
        >src
        >alt
        >width
        >height
        >loading 

        example:
            <img src='profile.jpg' alt='Profile photo' width="200">

# Headings

    HTML headings are titles or the subtitles that you want to display in the web.

    ## Advantages:
        > Search engines use the headings to index the structure and content of your web pages.
        > Important to show the documentation structure.

    examples:
        h1 --> Main title
        h2 --> Major title
        h3 --> sub-sections
        h4 --> Sub-subsection
        h5 --> Smaller subsection
        h6 --> Lowest heading level

    code:

        <h1>My Personal Profile</h1>
        <h2>About Me</h2>
        <h3>Programming Languages</h3>
        <h4>Java</h4>
        <h5>Python Basics</h5>
        <p>Variables, loops and functions.</p>
        <h5>Advanced Topics</h5>
        <h6>Decorators</h6>
        <p>Decorators allow us to modify the behavior of functions.</p>

    ## Bigger heading 
        > Heading tag has a default size. we can also specify the size.
        > With the help of the style attribute using the css font size property.

        code:   

            <h1 style="font-size:60px;" >Heading 1 </h1>

# Paragraphs

    A paragraph always starts on a new line ,and usually a block of text.

    Denoted by the <p>.

    Automatically removes the extra spaces.

    <p> --> Opening tag
    This is a paragraph.  --> Content
    </p>  --> Closing tag

    <p>
        This paragraph contains a lot of lines in the source code, but the browser ignores it.
    </p>

    ## HTML Horizontal Rules

        The <hr> tag defines a thematic break,
        used to display as a horizontal rule.

        It is used to seperate content in an HTML page.

        code:

            <h1>This is project 1</h1>
            <p>This is project description.</p>
            <hr>

            <h2>This is project 2</h2>
            <p>This is project description.</p>
            <hr> 



    ## HTML Line Break

        The <br> element defines a line break.

        It is used when we need a line break (a new line) without starting a new paragraph.

        example:

            <p> This is <br> a paragraph <br> With line breaks.</p>


    ## <pre> Element 

        Defines pre-formatted text

        The HTML <pre> element is displayed in a fixed-width font, and it preserves both spaces and the line breaks.

        <pre>
            My Bonnie lies over the ocean.
            My Bonnie lies over the sea.
            My Bonnie lies over the ocean.
            Oh, bring back my Bonnie to me.
        </pre>


    ## Special Characters

        For the display of the special character we need to use the HTML entities:

        example:
                > &lt;     shows --<
                > &gt;     shows -->
                > &amp;     shows --&
                > &quot;     shows --"
                > &nbsp;     non-breaking-space

        use case:

            <h2>Product Information</h2>

            <p>Storage:500 &nbsp;GB</p>

            <p>Price:$8nbsp;499</p>

            <p>Company : HC &amp; HC </p>

            <p>Requirement: Age &gt; 18</p>

            <h2>HTML Code</h2>

            <p>
                &lt;h1&gt;Hello World&lt;/h1&gt;
            </p>

            <p>
                class=&quot;container&quot;
            </p>

# HTML Styles

    The HTML style attribute is used to add styles to the elements like color,font,size and more. 

    example: 
        Changing the color,
        Changing the font,
        changing the size etc


    ## HTML Style attribute

        style attribute helps to style the HTML elements 

        syntax:

            <tagname style="property:value;">

            here both the property and the values are css value.

    ## Background color
        
        <body style="background-color:black;">

            <h1 style='background-color:blue' >This is a heading</h1>

            <p style='background-color:white' >This is a paragraph.</p>

        </body>

    ## Text color

        using the style attribute we can change the text color for an HTML element

        <h1 style='color:blue'>This is a heading</h1>

        <p style='color:white'>This is a paragraph.</p>

    ## Fonts 

        The css font-family property defines the font in the web page

        <h1 style="font-family:verdana;">This is heading</h1>
        
        <p style="font-family:courier;">This is a paragraph.</p> 

    ## Text size

        This helps us to defines the font size for an HTML elements.

        <h1 style="font-size:300%;">This is a heading</h1>

        <p style="font-size:160%;">This is a paragraph.</p> 

    ## Text Allignment

        This property defines the horizontal text alignment for an HTML element.

        <h1 style="text-align:center;">Centered Heading</h1>

        <p style="text-align:center;">Centered paragraph.</p> 

# HTML Text Formatting

    HTML gives several elements to format.we can make text bold,italic,highlighted,smaller,deleted,inserted, or displayed as superscript and the superscript.

    example
        <p> This is <b>bold text</b>.</p> --> makes them bold

        <p>Please read the <strong>important instructions</strong>.</p>

        <p>This is <i>italic text</i>.</p>

        
    ## Formatting Elements are 
        <b> --> Bold text
        <strong> --> Important text
        <i> --> Italic text
        <em> --> Emphasized text
        <mark> --> Marked text
        <small> --> Smaller text
        <del> --> Deleted text
        <ins> --> Inserted text
        <sub> --> Subscript text
        <sup> --> Superscript text

    codes:

        1.BOLD Text

        <p>
            My favorite programming language is <b>Python</b>.
        </p>

        use case:
            Use it when you want to visually draw attention to a word without giving it special importance.


        2.STRONG Text

        <p>
            <strong>Warning:</strong> Do not share your password.
        </p>

        use case:
            Warnings, important instructions, critical information

        3.Italic Text

        <p>
            The scientific name is <i>Homo sapiens</i>.
        </p>     

        use case:
            Common uses include:
                -Scientific names
                -Foreign words
                -Technical terms
                -Thoughts or terminology that is -conventionally italicized

        4. Emphasized text

        <p>
            You <em>must</em> complete the assignment today.
        </p>

        use case:
            The emphasis changes the meaning of the sentence.

        5. Mark

        <p>
            You searched for <mark>HTML</mark>.
        </p>

        use cases:
            Imagine Google-like search results.

        6.small 

            <p>
                This product is available for ₹499.
                <small>Terms and conditions apply.</small>
            </p>

        use case:
            copyright
            legal information
            reminder

        7.del

            <p>
                Original price:
                <del>₹999</del>
            </p>

            <p>
                New price: ₹699
            </p>
        
        use case:
            commonly used in the pricing.

        8.inserted text

            <p>
                The project deadline is
                <del>Monday</del>
                <ins>Wednesday</ins>.
            </p>

        use case:
            showing changes to a policy.

        9.Subscript

            <p>
                The chemical equation of the water is H<sub>2</sub>O
            </p>

            <p>CO<sub>2</sub></p>
            <p>H<sub>2</sub>O</p>
            <p>O<sub>2</sub></p>

            <p>a<sub>1</sub></p>
            <p>a<sub>2</sub></p>
            <p>a<sub>3</sub></p>

        use case:
            used in the chemical formulas.
            used in the mathematical notaions

        10.superscript

            <p>
                The power of 10<sup>2</sup> = 100
            </p>

            <p>
                HTML was created for the Web.<sup>1</sup>
            </p>

        use cases:
            Maths
            units
            Footnotes

# Quotation and citation Elements

    HTML gives a special elements for displaying quotation,references,abbreviations and information about the source of content.

    example:

        > For display a long quotation taken from another source ---> <blockquote>

            <blockquote cite="https://example.com/article">
                Learning never stops. Every day is an opportunity to learn something new.
            </blockquote>

        > For specify the source we use <cite> attribute. like name of the work or the work title.

            <p><cite>This New Car</cite> was designed by Edvard.</p>
        
        > For short quotation we will use the <q>.

            <p>My teacher said <q>Practice makes perfect.</q></p>

        >For Abbreviations we will use the <abbr> like WHO -->World Health Organization.

            <p>The <abbr title="Hyper Text Markup Language">HTML</abbr> used to create web application.</p>

        >For mentioning any address we will use the <address> for contact information like email address,URL,Physical address,phone number ,document owner of the artical.

        syntax:
            <address>
                Contact information
            </address>

            <address>
                Written by Dinesh KS<br>
                Email: dinesh@gmail.com<br>
                Phone: +91 98765 43210<br>
                Erode, Tamil Nadu, India
            </address>

        > For forcing the direction in which the text need to be displayed. --> <bdo> Bi-Directional Override.

            dir="ltr" means Left to Right
            dir="rtl" means Right to Left

            example:

                <bdo dir="rtl">
                    This text will be displayed from right to left.
                </bdo>

                <bdo dir="lft">
                    This text will be displayed from left to right.
                </bdo>

# HTML Comments 
    
    HTML comments are not displayed in the browser,but they can help the developer to read and understand the source code.

    ## HTML Comment Tag

        <!--comments-->

    > Comments helps us to place notifications and reminders in code.

    > They can hide the content Temporarily.

    > We can also add more than one line as comment.

    ## Hide inline Content

        Comments can also able to hide the middle parts of the code.

        <p> This is a <!--car--> .</p>
    
     
# Favicon

    A favicon is a small icon associated with a website or the web page.

    Favourite + Icon = Favicon

    It is commonly displayed in the browser tab next to the page title.

    ## use case:
        -It helps to identify a website quickly.

    It appears in places such as
        Browser tabs
        Bookmarks
        Browser history
        Home-screen shortcuts
        Other browser UI areas
    
    favicon is normally added inside the <head> section of an HTML document.

    example:

    <!DOCTYPE html> 
    <html> 

        <head> 
            <title>My Personal Profile</title> <link rel="icon" href="favicon.ico">
        </head> 
        
        <body> 
            <h1>My Personal Profile</h1> 
        </body> 
    </html>

    here,
        <link rel="icon" href="favicon.ico">

        <link> is an HTML element used to establish a relationship between the current HTML document and an externa; resource.

        rel="icon" is an attribute

        href="favicon.ico" find the file named favicon.ico.

        it should be placed inside <head> tag.

        <head> 
            <title>My Personal Profile</title> <link rel="icon" href="favicon.ico">
        </head> 

    common Favicon file formats
        Favicons can be provided in several image formats.such as
            .ico
            .png
            .svg

# HTML Colors
    HTML itself provides the structure,while css color properties control how that content looks.

    There are several ways to specify colors:
        1.Color name
        2.RGB
        3.HRX
        4.HSL
        5.RGBA
        6.HSLA

    1.Color names
        The simplest method is using a predefined color name.

        example:

            we can change the text color

            <h2 style="color: blue;">
                About Me
            </h2>

            we can also change the background

            <p style="background-color: lightgray;">
                I am learning HTML.
            </p>

    2.RGB Colors
        RGB Stands for Red Green Blue.

        Each parameter (red, green, and blue) defines the intensity of the color with a value between 0 and 255.

        This means that there are 256 x 256 x 256 = 16777216 possible colors.

        <p style="color: rgb(255, 0, 0);">
            This is red text.
        </p>

        here,
            Red - 255
            Green - 0
            Blue - 0

        For example, rgb(255, 0, 0) is displayed as red, because red is set to its highest value (255), and the other two (green and blue) are set to 0.

        #Shades of gray:
            Shads of gray are often defined using the equal values for all three parameters.

            example
                rgb(60,60,60)

        3.HEX Colors
            HEX means hexadecimal color notation.

            It starts with # and normally contains six hexadecimal characters.

            <p style="color: #ff0000;">
                This is red text.
            </p>

            structure is #RRGGBB
                RR-Red
                GG-Green
                BB-Blue

            examples
                #ff0000 -> Red
                #00ff00 -> Green
                #0000ff -> Blue
                #000000 -> Black
                #ffffff -> White

            code:
                <h1 style="color: #1e3a8a;">
                    My Personal Profile
                </h1>

        4.HSL Colors
            HSL means 
                H -> Hue (degere on the color wheel from 0 - 360,0 is red,120 is green and 240 is blue).

                S -> Saturation (intensity, 0 means shade of gray,and 100 is full color)  is percentage value %.

                L -> Lightness (0% is black and 100% is white)  is percentage value %
                
            <p style="color: hsl(0, 100%, 50%);">
                This is red text.
            </p>
        
            <h2 style="color: hsl(120, 60%, 30%)">
                My Skills
            </h2>

        5.Transparency with RGBA
            RGBA adds an Alpha value to RGB.

            Alpha controls Transparency

                R -> Red
                G -> Green
                B -> Blue
                A -> Alphs

            0 - completely transparent 
            1 - completely opaque

            example:

                rgba(0, 0, 255, 0) -> invisible

                rgba(0, 0, 255, 0.5) -> 50% transparent

                rgba(0,0,255,1) -> fully visible

            <p style="background-color: rgba(0, 0, 255, 0.5);">
                Semi-transparent blue background.
            </p>











             