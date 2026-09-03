## Quotation and citation Elements

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

                <bdo dir="rtl">
                    This text will be displayed from right to left.
                </bdo>
