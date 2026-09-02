
# HTML Attribute

    They provide additional information about the HTML elements.
     
    They specify only in the start tag.

    They must be in name='value'

syntax:
    <tag attribute="value">Content</tag>


exapmles:

    > href attribute

        <a href='https://www.amazon.com'>Visit Amazon</a>

    >src attribute

        <img src='sample_image.jpg> --> helps to insert the images

        <img src='sample_image.jpg' width-'500 height='600'>   --> the <img> tag should also contains the width and height

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

        
    
# Ways to specify the URL in src attribute

1.Absolute URL
    links to an external image that is hosted on another website.

2.Relative URL
    links to an image that is hosted within the website

# More attributes

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

D.Form/Input validation

    >type
    >name
    >value
    >placeholder
    >required
    >disabled
    >readonly
    >checked
    >selected
    >min
    >max
    >minlength
    >maxlength
    >pattern
    >autocomplete

    example:
        <input type='email' name='email' placeholder="Enter your email" required>

E.Global attributes

    >id
    >class
    >style
    >title
    >lang
    >dir
    >data-*

    <div id='product' class='card' data-product-id='101'>     

    here - data-product-id is a custom data attribute