# tech-doc
<script src="https://cdn.freecodecamp.org/testable-projects-fcc/v1/bundle.js"></script>
<!DOCTYPE html>
<html>

<head>
    <meta lang="8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" type="text/css"
        href="C://Users/Rebekah Quinn/Documents/Studio Ninty/Studio Ninty Online/HTML/tech.doc.css">
</head>

<body>
    <nav id="navbar">
        <header>
            <h1 id="nav-header">Responsive Web Documentation</h1>
        </header>
        <ul>
            <li>
                <a class="nav-link" href="#Introduction">
                    Introduction
                </a>
            </li>

            <li>
                <a class="nav-link" href="#Previous_Knowledge_Needed">
                    Previous Knowledge Needed
                </a>
            </li>

            <li>
                <a class="nav-link" href="#Media_Queries">
                    Media Queries
                </a>
            </li>

            <li>
                <a class="nav-link" href="#Responsive_Images">
                    Responsive Images
                </a>
            </li>

            <li>
                <a class="nav-link" href="#High_Resolution_Images">
                    High Resolution Images
                </a>
            </li>

            <li>
                <a class="nav-link" href="#Responsive_Text">
                    Responsive Text
                </a>
            </li>

            <li>
                <a class="nav-link" href="#Flexbox">
                    Flexbox
                </a>
            </li>

            <li>
                <a class="nav-link" href="#Flex_Containers">
                    Flex Containers
                </a>
            </li>

            <li>
                <a class="nav-link" href="#Flex_Items">
                    Flex Items
                </a>
            </li>

            <li>
                <a class="nav-link" href="#CSS_Grids">
                    CSS Grids
                </a>
            </li>

            <li>
                <a class="nav-link" href="#CSS_Grids_-_Important_Terminology">
                    CSS Grids - Important Terminology
                </a>
            </li>

            <li>
                <a class="nav-link" href="#Powerful_Lines_in_Grid">
                    Powerful Lines in Grid
                </a>
            </li>

            <li>
                <a class="nav-link" href="#Grid_Containers">
                    Grid Containers
                </a>
            </li>

            <li>
                <a class="nav-link" href="#Grid_Items">
                    Grid Items
                </a>
            </li>

            <li>
                <a class="nav-link" id=bottom-link href="#Reference">
                    Reference
                </a>

            </li>
        </ul>
    </nav>

    <main id="main-doc">
        <section class="main-section" id="Introduction">
            <header>
                <h3>Introduction</h3>
            </header>
            <p>Responsive Web design is the approach that suggests that design and development should respond to the
                user’s behavior and environment based on screen size, platform and orientation.
                The practice consists of a mix of flexible grids and layouts, images and an intelligent use of CSS media
                queries. As the user switches from their laptop to iPad, the website should automatically switch to
                accommodate for resolution, image size and scripting abilities.
                In other words, the website should have the technology to automatically respond to the user’s
                preferences. This would eliminate the need for a different design and development phase for each new
                gadget on the market.
            </p>
        </section>

        <section class="main-section" id="Previous_Knowledge_Needed">
            <header>
                <h3>Previous Knowledge Needed</h3>
            </header>
            <p>Knowledge of basic HTML and basic CSS is needed to use Responsive Website CSS and you should know how to
                write them. You should also have a program to use them and an internet connection to see changes as you
                learn.</p>
        </section>

        <section class="main-section" id="Media_Queries">
            <header>
                <h3>Media Queries</h3>
            </header>
            <p>Media Queries are a new technique introduced in CSS3 that change the presentation of content based on
                different viewport sizes. The viewport is a user's visible area of a web page, and is different
                depending on the device used to access the site.

                Media Queries consist of a media type, and if that media type matches the type of device the document is
                displayed on, the styles are applied. You can have as many selectors and styles inside your media query
                as you want.

                Here's an example of a media query that returns the content when the device's width is less than or
                equal to 100px:
                <br>
                <code>@media (max-width: 100px) { /* Your CSS Rules Go In Here  */ }</code>
                <br>
                and the following media query returns the content when the device's height is more than or equal to
                350px:
                <br>
                <code>@media (min-height: 350px) { /* Your CSS Rules Go In Here */ }</code>
                <br>
                Remember, the CSS inside the media query is applied only if the media type matches that of the device
                being used.</p>
        </section>

        <section class="main-section" id="Responsive_Images">
            <header>
                <h3>Responsive Images</h3>
            </header>
            <p>
                Making images responsive with CSS is actually very simple. You just need to add these properties to an
                image:
                <br>
                <code>
                img {
                max-width: 100%;
                height: auto;
                }
                </code>
                <br>
                The max-width of 100% will make sure the image is never wider than the container it is in, and the
                height of auto will make the image keep its original aspect ratio.
            </p>
        </section>

        <section class="main-section" id="High_Resolution_Images">
            <header>
                <h3>High Resolution Images</h3>
            </header>
            <p>
                With the increase of internet connected devices, their sizes and specifications vary, and the displays
                they use could be different externally and internally. Pixel density is an aspect that could be
                different on one device from others and this density is known as Pixel Per Inch(PPI) or Dots Per
                Inch(DPI). The most famous such display is the one known as a "Retina Display" on the latest Apple
                MacBook Pro notebooks, and recently iMac computers. Due to the difference in pixel density between a
                "Retina" and "Non-Retina" displays, some images that have not been made with a High-Resolution Display
                in mind could look "pixelated" when rendered on a High-Resolution display.

                The simplest way to make your images properly appear on High-Resolution Displays, such as the MacBook
                Pros "retina display" is to define their width and height values as only half of what the original file
                is. Here is an example of an image that is only using half of the original height and width:

                <code>
                        /*CSS*/
                        img { height: 250px; width: 250px; }
                       /*HTML*/
                      <img src="coolPic500x500" alt="A most excellent picture">
                </code>
            </p>
        </section>

        <section class="main-section" id="Responsive_Text">
            <header>
                <h3>Responsive Text</h3>
            </header>
            <p>
                Instead of using em or px to size text, you can use viewport units for responsive typography. Viewport
                units, like percentages, are relative units, but they are based off different items. Viewport units are
                relative to the viewport dimensions (width or height) of a device, and percentages are relative to the
                size of the parent container element.

                The four different viewport units are:
            <ul id="resp-text-list">
                <li><code>vw (viewport width)</code>: 10vw would be 10% of the viewport's width.</li>
                <li><code>vh (viewport height)</code>: 3vh would be 3% of the viewport's height.</li>
                <li><code>vmin (viewport minimum)</code>: 70vmin would be 70% of the viewport's smaller dimension
                    (height or
                    width).</li>
                <li><code>vmax (viewport maximum)</code>: 100vmax would be 100% of the viewport's bigger dimension
                    (height
                    or width).</li>
            </ul> Here is an example that sets a body tag to 30% of the viewport's width.

            <pre>body 
                    { width: 30vw; 
                }</pre>
            </p>
        </section>

        <section class="main-section" id="Flexbox">
            <header>
                <h3>Flexbox</h3>
            </header>
            <p>
                The Flexbox Layout module aims at
                providing a more efficient way to lay out, align and distribute space among items in a container, even
                when their size is unknown and/or dynamic.
                <br>
                The main idea behind the flex layout is to give the container the ability to alter its items’
                width/height (and order) to best fill the available space (mostly to accommodate to all kind of display
                devices and screen sizes). A flex container expands items to fill available free space or shrinks them
                to prevent overflow.
                <br>
                Most importantly, the flexbox layout is direction-agnostic as opposed to the regular layouts (block
                which is vertically-based and inline which is horizontally-based). While those work well for pages, they
                lack flexibility (no pun intended) to support large or complex applications (especially when it comes to
                orientation changing, resizing, stretching, shrinking, etc.).

                Flexbox layout is most appropriate to the components of an application, and small-scale layouts,
                while the <a href="#css-grids">Grid</a> layout is intended for larger scale layouts.
            </p>
        </section>

        <section class="main-section" id="Flex_Containers">
            <header>
                <h3>Flex Containers</h3>
            </header>
            <p>Containers are the Parent Element like so: <br><img id="flex-container-img"
                    src="https://i.stack.imgur.com/bjGWl.png" width="434px" height="258px"><br>They hold the child
                elements, the Flex Items.</p>
            <h4>Properties for the Parent</h4>
            <p>
            <h4>Display</h4>
            This defines a flex container; inline or block depending on the given value. It enables a flex context
            for all its direct children.
            <br>
            <br>
            <pre>
                .container {
                display: flex; /* or inline-flex */
                }
            </pre>
            <br>
            <strong>Note that CSS columns have no effect on a flex container.</strong></p>
            <br>
            <h4>Flex-direction</h4>
            <img src="https://mdn.mozillademos.org/files/15649/Basics1.png" width="261px" height="76px">
            <br>
            <br>
            <img src="https://mdn.mozillademos.org/files/15615/Basics2.png" width="354.5px" height="113.5px">
            <p>
                The four possible values of flex-direction being shown: top to bottom, bottom to top, right to left, and
                left to right

                This establishes the main-axis, thus defining the direction flex items are placed in the flex container.
                Flexbox is (aside from optional wrapping) a single-direction layout concept. Think of flex items as
                primarily laying out either in horizontal rows or vertical columns.
                <br>
                <br>
            <pre>
                .container {
                flex-direction: row | row-reverse | column | column-reverse;
                }
            </pre>
            <br>
            <ul id="flex-cont-list">
                <li><code>row (default):</code> left to right in ltr; right to left in rtl</li>
                <li><code>row-reverse:</code> right to left in ltr; left to right in rtl</li>
                <li><code>column:</code>same as row but top to bottom</li>
                <li><code>column-reverse:</code> same as row-reverse but bottom to top</li>
            </ul>
            </p>
            <h4>Flex-wrap</h4>
            <img id="flex-wrap-img" src="https://flexbox.tech-academy.co.uk/files/2017/10/flex-wrap.png" width="466.5px"
                height="179px">
            <p>

                Two rows of boxes, the first wrapping down onto the second
                By default, flex items will all try to fit onto one line. You can change that and allow the items to
                wrap as needed with this property.
                <br>
            <pre>
                .container {
                flex-wrap: nowrap | wrap | wrap-reverse;
                }</pre>
            <br>
            <ul id="flex-wrap-list">
                <li><code>nowrap (default):</code> all flex items will be on one line</li>
                <li><code>wrap:</code> flex items will wrap onto multiple lines, from top to bottom.</li>
                <li><code>wrap-reverse:</code> flex items will wrap onto multiple lines from bottom to top.</li>
            </ul>
            There are some visual demos of flex-wrap <a
                href="https://css-tricks.com/almanac/properties/f/flex-wrap/">here</a>.
            </p>
            <br>
            <h4>Flex-flow</h4>
            <p>

                This is a shorthand for the flex-direction and flex-wrap properties, which together define the flex
                container’s main and cross axes. The default value is row nowrap.
            <pre>
                .container {
                flex-flow: column wrap;
                }
                </pre>
            </p>
            <br>
            <h4>Justify-content</h4>
            <p>
                Flex items within a flex container demonstrating the different spacing options

                This defines the alignment along the main axis. It helps distribute extra free space leftover when
                either all the flex items on a line are inflexible, or are flexible but have reached their maximum size.
                It also exerts some control over the alignment of items when they overflow the line.
                <br>
            <pre>
                .container {
                justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | start |
                end | left | right ... + safe | unsafe;
                }
                </pre>
            <br>
            <img src="https://flexbox.tech-academy.co.uk/files/2017/10/justify-content.png">
            <br>
            <ul id="justify-cont-list">
                <li><code>flex-start (default):</code> items are packed toward the start of the flex-direction.</li>
                <li><code>flex-end:</code> items are packed toward the end of the flex-direction.</li>
                <li><code>start:</code> items are packed toward the start of the writing-mode direction.</li>
                <li><code>end:</code> items are packed toward the end of the writing-mode direction.</li>
                <li><code>left:</code> items are packed toward left edge of the container, unless that doesn’t make
                    sense with the
                    flex-direction, then it behaves like start.</li>
                <li><code>right:</code> items are packed toward right edge of the container, unless that doesn’t make
                    sense with the
                    flex-direction, then it behaves like start.</li>
                <li><code>center:</code> items are centered along the line.</li>
                <li><code>space-between:</code> items are evenly distributed in the line; first item is on the start
                    line, last item on
                    the end line</li>
                <li><code>space-around:</code> items are evenly distributed in the line with equal space around them.
                    Note that visually
                    the spaces aren’t equal, since all the items have equal space on both sides. The first item will
                    have
                    one unit of space against the container edge, but two units of space between the next item because
                    that
                    next item has its own spacing that applies.</li>
                <li><code>space-evenly:</code> items are distributed so that the spacing between any two items (and the
                    space to the
                    edges) is equal.</li>
            </ul>
            <br>
            <p id="justify-para">
                Note that that browser support for these values is nuanced. For example, space-between never got support
                from some versions of Edge, and start/end/left/right aren’t in Chrome yet. MDN has detailed charts. The
                safest values are <code>flex-start</code>, <code>flex-end</code>, and <code>center</code>.

                There are also two additional keywords you can pair with these values: <code>safe</code> and
                <code>unsafe</code>. Using <code>safe</code>
                ensures that however you do this type of positioning, you can’t push an element such that it renders
                off-screen (e.g. off the top) in such a way the content can’t be scrolled too (called “data loss”).</p>
            </p>
            <br>
            <h4>Align-items</h4>
            <p>

                Demonstration of differnet alignment options, like all boxes stuck to the top of a flex parent, the
                bottom, stretched out, or along a baseline

                This defines the default behavior for how flex items are laid out along the cross axis on the current
                line. Think of it as the justify-content version for the cross-axis (perpendicular to the main-axis).
            <pre>
                .container {
                align-items: stretch | flex-start | flex-end | center | baseline | first baseline | last baseline |
                start | end | self-start | self-end + ... safe | unsafe;
                }
                </pre>
            <br>
            <img src="https://codropspz-tympanus.netdna-ssl.com/codrops/wp-content/uploads/2014/10/align-content-illustration.jpg"
                width="405.5" height="715.5px">
            <br>
            <ul id="align-items-list">
                <li><code>stretch (default)</code>: stretch to fill the container (still respect min-width/max-width).
                </li>
                <li><code>flex-start / start / self-start</code>: items are placed at the start of the cross axis. The
                    difference between
                    these is subtle, and is about respecting the flex-direction rules or the writing-mode rules.</li>
                <li><code>flex-end / end / self-end</code>: items are placed at the end of the cross axis. The
                    difference again is subtle
                    and is about respecting flex-direction rules vs. writing-mode rules.</li>
                <li><code>center</code>: items are centered in the cross-axis.</li>
                <li><code>baseline</code>: items are aligned such as their baselines align</li>
            </ul>
            </p>
            <p id="align-items-para">
                <!--add code element and css line height 40px here for safe and unsafe-->
                The <code>safe</code> and <code>unsafe</code> modifier keywords can be used in conjunction with all the
                rest of these keywords
                (although note browser support), and deal with helping you prevent aligning elements such that the
                content becomes inaccessible.</p>

            <br>
            <h4>Align-content</h4>
            <p>
                <img src="https://codropspz-tympanus.netdna-ssl.com/codrops/wp-content/uploads/2014/10/align-content-illustration.jpg"
                    width="405.5" height="715.5">
                <br>
                Examples of the align-content property where a group of items cluster at the top or bottom, or stretch
                out
                to fill the space, or have spacing.

                This aligns a flex container’s lines within when there is extra space in the cross-axis, similar to how
                justify-content aligns individual items within the main-axis.

                Note: this property has no effect when there is only one line of flex items.</p>
            <br>
            <pre>
            .container {
            align-content: flex-start | flex-end | center | space-between | space-around | space-evenly | stretch |
            start | end | baseline | first baseline | last baseline + ... safe | unsafe;
            }
            </pre>
            <br>
            <ul id="align-cont-list">
                <li><code>flex-start / start</code>: items packed to the start of the container. The (more supported)
                    flex-start honors the
                    flex-direction while start honors the writing-mode direction.</li>
                <li><code>flex-end / end</code>: items packed to the end of the container. The (more support) flex-end
                    honors the
                    flex-direction while end honors the writing-mode direction.</li>
                <li><code>center</code>: items centered in the container</li>
                <li><code>space-between</code>: items evenly distributed; the first line is at the start of the
                    container while the last one
                    is at the end.</li>
                <li><code>space-around</code>: items evenly distributed with equal space around each line.</li>
                <li><code>space-evenly</code>: items are evenly distributed with equal space around them.</li>
                <li><code>stretch (default)</code>: lines stretch to take up the remaining space.</li>
            </ul>
            <br>
            <p id="align-cont-para">
                The <code>safe</code> and <code>unsafe</code> modifier keywords can be used in conjunction with all the
                rest of these keywords
                (although note browser support), and deal with helping you prevent aligning elements such that the
                content
                becomes inaccessible.</p>
            </p>

            </p>
        </section>
        <!--FINISH ADDING INFORMATION AND REUPLOAD TO CODEPEN AND GITHUB-->
        <section class="main-section" id="Flex_Items">
            <header>
                <h3>Flex Items</h3>
            </header>
            <p>Flex items are the child of the container parent like in the image shown <a
                    href="#flex-container-img">above.
                    They include the properties below.
                </a></p>
            <h4>Order</h4>
            <p>
                By default, flex items are laid out in the source order. However, the order property controls the order
                in which they appear in the flex container.
            <pre>
                .item {
                order: 5; /* default is 0 */
                }
                </pre>
            <br>
            <img src="https://miro.medium.com/max/1222/1*sWPnINZSEx_BK-bqWG5wdw.png">
            <br>
            <h4>Flex Grow</h4>
            <p>
                This defines the ability for a flex item to grow if necessary. It accepts a unitless value that serves
                as a proportion. It dictates what amount of the available space inside the flex container the item
                should take up.

                If all items have flex-grow set to 1, the remaining space in the container will be distributed equally
                to all children. If one of the children has a value of 2, the remaining space would take up twice as
                much space as the others (or it will try to, at least).
            <pre>
                .item {
                flex-grow: 4; /* default 0 */
                }
                </pre>

            <strong>Negative numbers are invalid.</strong>
            </p>
            <h4>Flex Shrink</h4>
            <p>
                This defines the ability for a flex item to shrink if necessary.
            <pre>
                .item {
                flex-shrink: 3; /* default 1 */
                }
                </pre>
            <strong>Negative numbers are invalid.</strong>
            </p>
            <h4>Flex Basis</h4>
            <p>
                This defines the default size of an element before the remaining space is distributed. It can be a
                length (e.g. 20%, 5rem, etc.) or a keyword. The <code>auto</code> keyword means “look at my width or
                height property”
                (which was temporarily done by the <code>main-size</code> keyword until deprecated). The
                <code>content</code> keyword means “size
                it based on the item’s content” – this keyword isn’t well supported yet, so it’s hard to test and harder
                to know what its brethren <code>max-content, min-content, and fit-content</code> do.

            <pre>
                .item {
                flex-basis: | auto; /* default auto */
                }
                </pre>
            If set to 0, the extra space around content isn’t factored in. If set to auto, the extra space is
            distributed based on its flex-grow value.
            </p>
            <h4>Flex</h4>
            <p id="flex-para">
                This is the shorthand for <code>flex-grow, flex-shrink and flex-basis</code> combined. The second and
                third
                parameters <code></code>(flex-shrink and flex-basis)</code> are optional. The default is
                <code>0 1 auto</code>, but if you set it with a
                single number value, it’s like <code>1 0</code>.

            <pre>
                .item {
                flex: none | [ <'flex-grow'>
                    <'flex-shrink'>? || <'flex-basis'> ]
                            }
                            </pre>
            <strong>
                It is recommended that you use this shorthand property rather than set the individual
                properties.
                <br>
                The shorthand sets the other values intelligently.</strong>
            </p>
            <!--Text not staying in margins or justified check all at end-->
            <h4>Align Self</h4>
            <p>
                This allows the default alignment (or the one specified by align-items) to be overridden for individual
                flex items.

                Please see the align-items explanation to understand the available values.
            <pre>
                .item {
                align-self: auto | flex-start | flex-end | center | baseline | stretch;
                }
                </pre>
            <br>
            <strong>Note that float, clear and vertical-align have no effect on a flex item.</strong>
            </p>
        </section>

        <section class="main-section" id="CSS_Grids">
            <header>
                <h3>CSS Grids</h3>
            </header>
            <p>CSS Grid Layout is the most powerful layout system available in CSS. It is a 2-dimensional system,
                meaning it can handle both columns and rows, unlike flexbox which is largely a 1-dimensional system. You
                work with Grid Layout by applying CSS rules both to a parent element (which becomes the Grid Container)
                and to that element’s children (which become Grid Items).</p>
        </section>

        <section class="main-section" id="CSS_Grids_-_Important_Terminology">
            <header>
                <h3>CSS Grids - Important Terminology</h3>
                <p>
                    Before diving into the concepts of Grid it’s important to understand the terminology. Since the
                    terms involved here are all kinda conceptually similar, it’s easy to confuse them with one another
                    if you don’t first memorize their meanings defined by the Grid specification. But don’t worry, there
                    aren’t many of them.
                </p>
                <h4>Grid Container</h4>
                <p>
                    The element on which <code>display: grid</code> is applied. It’s the direct parent of all the grid
                    items. In this
                    example <code>container</code> is the grid container.

                    <xmp>
                        <div class="container">
                            <div class="item item-1"> </div>
                            <div class="item item-2"> </div>
                            <div class="item item-3"> </div>
                        </div>
                    </xmp>
                <h4>Grid Item</h4>
                <p>
                    The children (i.e. direct descendants) of the grid container. Here the <code>item</code> elements
                    are grid items,
                    but <code>sub-item</code> isn’t.
                    <xmp>
                        <div class="container">
                            <div class="item"> </div>
                            <div class="item">
                                <p class="sub-item"> </p>
                            </div>
                            <div class="item"> </div>
                        </div>
                    </xmp>
                </p>
                <h4>Grid Line</h4>
                <p>The dividing lines that make up the structure of the grid. They can be either vertical (“column grid
                    lines”) or horizontal (“row grid lines”) and reside on either side of a row or column. Here the
                    yellow line is an example of a column grid line.</p>
                <img src="https://css-tricks.com/wp-content/uploads/2018/11/terms-grid-line.svg" width="375"
                    height="255">
                <h4>Grid Cell</h4>
                <p></p>The space between two adjacent row and two adjacent column grid lines. It’s a single “unit” of
                the
                grid.
                <br>Here’s the grid cell between row grid lines 1 and 2, and column grid lines 2 and 3.
                </p>
                <img src="https://css-tricks.com/wp-content/uploads/2018/11/terms-grid-cell.svg" width="375"
                    height="255">
                <h4>Grid Track</h4>
                <p>The space between two adjacent grid lines. You can think of them like the columns or rows of the
                    grid. Here’s the grid track between the second and third row grid lines.</p>
                <img src="https://css-tricks.com/wp-content/uploads/2018/11/terms-grid-track.svg" width="375"
                    height="255">
                <h4>Grid Area</h4>
                <p>The total space surrounded by four grid lines. A grid area may be composed of any number of grid
                    cells. Here’s the grid area between row grid lines 1 and 3, and column grid lines 1 and 3.</p>
                <img src="https://css-tricks.com/wp-content/uploads/2018/11/terms-grid-area.svg" width="375"
                    height="255">
            </header>
        </section>

        <section class="main-section" id="Powerful_Lines_in_Grid">
            <header>
                <h3>Powerful Lines in Grid</h3>
                <p>
                    Fluid width columns that break into more or less columns as space is available, with no media
                    queries!
                    <xmp>
                        .grid {
                        display: grid;
                        grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
                        /* This is better for small screens, once min() is better supported */
                        /* grid-template-columns: repeat(auto-fill, minmax(min(200px, 100%), 1fr)); */
                        grid-gap: 1rem;
                        /* This is the standardized property now, but has slightly less support */
                        /* gap: 1rem */
                        }
                    </xmp>
                </p>
            </header>
        </section>

        <section class="main-section" id="Grid_Containers">
            <header>
                <h3>Grid Containers</h3>
            </header>
            <p>Properties for the Parent Elements</p>
            <br>
            <h4>Display</h4>
            <p>Defines the element as a grid container and establishes a new grid formatting context for its
                contents.

                Values:

                <code>grid</code> – generates a block-level grid
                <code>inline-grid</code> – generates an inline-level grid
                <xmp>.container {
                    display: grid | inline-grid;
                    }</xmp>
            </p>
            <h4>Grid Template Columns and Rows</h4>
            <p id="grid-col-row-para">
                <code>grid-template-columns</code>
                <br>
                <code>grid-template-rows</code>
                Defines the columns and rows of the grid with a space-separated list of values. The values represent
                the track size, and the space between them represents the grid line.

                Values:</p>
                <xmp>
                    <track-size>
                </xmp> – can be a length, a percentage, or a fraction of the free space in the grid (using the
                <code>fr</code> unit)
                <xmp>
                    <line-name>
                </xmp> – an arbitrary name of your choosing
                <pre>
                    .container {
                    grid-template-columns: ... | ...;
                    grid-template-rows: ... | ...;
                    }</pre>
                Examples:

                When you leave an empty space between the track values, the grid lines are automatically
                assigned positive and negative numbers:
                <pre>
                    .container {
                    grid-template-columns: 40px 50px auto 50px 40px;
                    grid-template-rows: 25% 100px auto;
                    }</pre>

                But you can choose to explicitly name the lines. Note the bracket syntax for the line names:
                <pre>
                    .container {
                    grid-template-columns: [first] 40px [line2] 50px [line3] auto [col4-start] 50px [five] 40px
                    [end];
                    grid-template-rows: [row1-start] 25% [row1-end] 100px [third-line] auto [last-line];
                    }</pre>
                Grid with user named lines

                Note that a line can have more than one name.
                <br><br>For example, here the second line will have
                two names: <code>row1-end and row2-start:</code>
                <pre>
                    .container {
                    grid-template-rows: [row1-start] 25% [row1-end row2-start] 25% [row2-end];
                    }</pre>
                If your definition contains repeating parts, you can use the <code>repeat()</code> notation to
                streamline
                things:
                <pre>
                    .container {
                    grid-template-columns: repeat(3, 20px [col-start]);
                    }</pre>
                Which is equivalent to this:
                <pre>
                    .container {
                    grid-template-columns: 20px [col-start] 20px [col-start] 20px [col-start];
                    }</pre>
                If multiple lines share the same name, they can be referenced by their line name and count.
                <pre>
                    .item {
                    grid-column-start: col-start 2;
                    }</pre>
                The <code>fr</code> unit allows you to set the size of a track as a fraction of the free space of
                the
                grid container. <br><br>For example, this will set each item to one third the width of the grid
                container:
                <pre>
                    .container {
                    grid-template-columns: 1fr 1fr 1fr;
                    }</pre>
                The free space is calculated after any non-flexible items. <br><br>In this example the total amount
                of free space available to the <code>fr</code> units doesn’t include the <code>50px</code>:
                <pre>
                    .container {
                    grid-template-columns: 1fr 50px 1fr 1fr;
                    }
                </pre>
            </p>
            <h4>Grid Template Areas</h4>
            <p id="grid-temp-para">Defines a grid template by referencing the names of the grid areas which are
                specified with the
                grid-area property. Repeating the name of a grid area causes the content to span those cells. A
                period signifies an empty cell. The syntax itself provides a visualization of the structure of the
                grid.

                Values:

                <xmp>
                    <grid-area-name>
                </xmp> – the name of a grid area specified with grid-area
                <code>.</code> – a period signifies an empty grid cell
                <code>none</code> – no grid areas are defined
                <pre>
                    .container {
                    grid-template-areas:
                    " | . | none | ..."
                    "...";
                    }
                </pre>
                Example:
                <pre>
                    .item-a {
                    grid-area: header;
                    }
                    .item-b {
                    grid-area: main;
                    }
                    .item-c {
                    grid-area: sidebar;
                    }
                    .item-d {
                    grid-area: footer;
                    }

                    .container {
                    display: grid;
                    grid-template-columns: 50px 50px 50px 50px;
                    grid-template-rows: auto;
                    grid-template-areas:
                    "header header header header"
                    "main main . sidebar"
                    "footer footer footer footer";
                    }
                </pre>
            </p>
            <p id="boom">
                That’ll create a grid that’s four columns wide by three rows tall. The entire top row will be
                composed of the header area. The middle row will be composed of two main areas, one empty cell,
                and one sidebar area. The last row is all footer.

                Example of grid-template-areas
                Each row in your declaration needs to have the same number of cells.

                You can use any number of adjacent periods to declare a single empty cell. As long as the
                periods have no spaces between them they represent a single cell.

                Notice that you’re not naming lines with this syntax, just areas. When you use this syntax the
                lines on either end of the areas are actually getting named automatically. If the name of your
                grid area is foo, the name of the area’s starting row line and starting column line will be
                foo-start, and the name of its last row line and last column line will be foo-end. This means
                that some lines might have multiple names, such as the far left line in the above example, which
                will have three names: header-start, main-start, and footer-start.</p>
        </section>

        <section class="main-section" id="Grid_Items">
            <header>
                <h3>Grid Items</h3>
            </header>
            <h4>Grid Template</h4>
            <p>
                A shorthand for setting grid-template-rows, grid-template-columns, and grid-template-areas in a single
                declaration.

                Values:

                <code>none</code> – sets all three properties to their initial values
                <xmp>
                    <grid-template-rows> / <grid-template-columns>
                </xmp> – sets <code>grid-template-columns</code> and <code>grid-template-rows</code> to
                the specified values, respectively, and sets <code>grid-template-areas</code> to <code>none</code>
                <pre>
                    .container {
                    grid-template: none | <grid-template-rows> / <grid-template-columns>;
                            }</pre>

                It also accepts a more complex but quite handy syntax for specifying all three. Here’s
                an example:
                <pre>
                    .container {
                    grid-template:
                    [row1-start] "header header header" 25px [row1-end]
                    [row2-start] "footer footer footer" 25px [row2-end]
                    / auto 50px auto;
                    }
                </pre>
                That’s equivalent to this:
                <pre>
                    .container {
                    grid-template-rows: [row1-start] 25px [row1-end row2-start] 25px [row2-end];
                    grid-template-columns: auto 50px auto;
                    grid-template-areas:
                    "header header header"
                    "footer footer footer";
                    }
                </pre>
            </p>
            <p id="zoom">
                Since grid-template doesn’t reset the implicit grid properties <code>(grid-auto-columns,
                        grid-auto-rows, and grid-auto-flow)</code>, which is probably what you want to do in most
                cases, it’s recommended to use the grid property instead of grid-template.
            </p>
            <h4>Column-Gap Row-Gap Grid-Column-Gap Grid-Row-Gap</h4>

            <p>Specifies the size of the grid lines. You can think of it like setting the width of the gutters between
                the
                columns/rows.

                Values:
                <xmp>
                     <line-size></xmp> – a length value</p>
                <pre>
                .container {
                /* standard */
                column-gap: line-size;
                    row-gap: line-size;

                        /* old */
                        grid-column-gap: line-size;
                            grid-row-gap: line-size;
                                }</pre>
                                <p>
                                    Example:
                                    <pre>
                                        .container {
                                        grid-template-columns: 100px 50px 100px;
                                        grid-template-rows: 80px auto 80px;
                                        column-gap: 10px;
                                        row-gap: 15px;
                                        }</pre>
                                <p>
                                    Example of <code>grid-column-gap</code> and <code>grid-row-gap</code>
                                    The gutters are only created between the columns/rows, not on the outer edges.

                                    Note: The <code>grid- </code>prefix will be removed and <code>grid-column-gap</code>
                                    and <code>grid-row-gap</code> renamed to
                                    <code>column-gap</code> and <code>row-gap</code>. The unprefixed properties are
                                    already supported in Chrome 68+,
                                    Safari 11.2 Release 50+ and Opera 54+.</p>
                                
                                    
                                    <h4>Gap, Grid-Gap</h4>


                                    <p>
                                        A shorthand for row-gap and column-gap

                                        Values:</p>
                                    <xmp>
                                        <p>
                                            <grid-row-gap>
                                                <grid-column-gap> – length values
                                                    .container {
                                                    /* standard */
                                                    gap: <grid-row-gap>
                                                        <grid-column-gap>;

                                                            /* old */
                                                            grid-gap: <grid-row-gap>
                                                                <grid-column-gap>;
                                                                    }
                                    </xmp>
                                    Example:
                                    <pre>
                                        .container {
                                        grid-template-columns: 100px 50px 100px;
                                        grid-template-rows: 80px auto 80px;
                                        gap: 15px 10px;
                                        }</pre>
                                    </p>If no <code>row-gap</code> is specified, it’s set to the same value as
                                    <code>column-gap</code>
                                    </p>
                                    <p>
                                        Note: The grid- prefix is deprecated (but who knows, may never
                                        actually be removed from browsers). Essentially grid-gap renamed
                                        to gap. The unprefixed property is already supported in Chrome
                                        68+, Safari 11.2 Release 50+, and Opera 54+.</p>

                                    <h4>Justify-Items</h4>
                                    <p>
                                        Aligns grid items along the inline (row) axis (as opposed to
                                        align-items which aligns along the block (column) axis). This
                                        value applies to all grid items inside the container.
                                        <!--style all lists, use unique ids-->
                                        Values:</p>
                                    <ul id="justify-items-list">
                                        <li>
                                            <code>start</code> – aligns items to be flush with the start
                                            edge of their
                                            cell</li>
                                        <li>
                                            <code>end</code> – aligns items to be flush with the end edge of their cell
                                        <li>
                                            <code>center</code> – aligns items in the center of their cell</li>
                                        <li>
                                            <code>stretch</code> – fills the whole width of the cell (this is the
                                            default)</li>

                                    </ul>
                                    <!--list styling end for this one-->
                                    <pre>.container {
                                        justify-items: start | end | center | stretch;
                                        }</pre>

                                    Examples:
                                    <pre>
                                        .container {
                                        justify-items: start;
                                        }</pre>

                                    Example of justify-items set to start
                                    <pre>.container {
                                        justify-items: end;
                                        }</pre>
                                    Example of justify-items set to end
                                    <pre>.container {
                                        justify-items: center;
                                        }</pre>
                                    Example of justify-items set to center
                                    <pre>.container {
                                        justify-items: stretch;
                                        }</pre>
                                    <p>Example of <code>justify-items</code> set to stretch
                                    This behavior can also be set on individual grid items via the
                                    <code>justify-self</code> property.</p>

                                    <h4>Align-Items</h4>
                                    <p>Aligns grid items along the block (column) axis (as opposed to
                                        justify-items which aligns along the inline (row) axis). This
                                        value applies to all grid items inside the container.

                                        Values:</p>
                                    <!--add list element-->
                                    <ul id="align-items-list">
                                    <li><code>start</code> – aligns items to be flush with the start edge of their
                                    cell</li>
                                    <li><code>end</code> – aligns items to be flush with the end edge of their cell</li>
                                    <li><code>center</code> – aligns items in the center of their cell</li>
                                    <li><code>stretch</code> – fills the whole height of the cell (this is the
                                    default)</li>
                                    </ul><!--list end here-->
                                    <xmp>
                                        .container {
                                        align-items: start | end | center | stretch;
                                        }</xmp>
                                    Examples:
                                    <xmp>
                                        .container {
                                        align-items: start;
                                        }
                                    </xmp>
                                    Example of align-items set to start
                                    <xmp>.container {
                                        align-items: end;
                                        }</xmp>
                                    Example of align-items set to end
                                    <xmp>.container {
                                        align-items: center;
                                        }</xmp>
                                    Example of align-items set to center
                                    <xmp>.container {
                                        align-items: stretch;
                                        }</xmp>
                                    Example of align-items set to stretch

                                    <p>This behavior can also be set on individual grid items via the
                                        align-self property.</p>
                                    <h4>Place Items</h4>

                                    <p>place-items sets both the align-items and justify-items
                                        properties in a single declaration.

                                        Values:</p>
                                        <xmp>
                                        <align-items> / <justify-items>
                                    </xmp> – <p>The first value sets
                                        <code>align-items</code>, the second value <code>justify-items</code>. If the
                                        second value is omitted, the first value is assigned to
                                        both properties.
                                        All major browsers except Edge support the place-items
                                        shorthand property.</p>
                                    <h4>
                                        Justify Content</h4>
                                    <p>Sometimes the total size of your grid might be less than
                                        the size of its grid container. This could happen if all
                                        of your grid items are sized with non-flexible units
                                        like <code>px</code>. In this case you can set the alignment of the
                                        grid within the grid container. This property aligns the
                                        grid along the inline (row) axis (as opposed to
                                        align-content which aligns the grid along the block
                                        (column) axis).
                                        
                                        Values:</p>
                                    <!--list all values in all section ctrl f values-->
                                    <p><ul id="justify-content-para">
                                        <li><code>start</code> – aligns the grid to be flush with the start edge
                                        of the grid container</li>
                                        <li><code>end</code> – aligns the grid to be flush with the end edge of
                                        the grid container</li>
                                        <li><code>center</code> – aligns the grid in the center of the grid
                                        container</li>
                                        <li><code>stretch</code> – resizes the grid items to allow the grid to
                                        fill the full width of the grid container</li>
                                        <li><code>space-around</code> – places an even amount of space between
                                        each grid item, with half-sized spaces on the far ends</li>
                                        <li><code>space-between</code> – places an even amount of space between
                                        each grid item, with no space at the far ends</li>
                                        <li>space-evenly – places an even amount of space between
                                        each grid item, including the far ends</li></p></ul>
                                    <pre>.container {
                                        justify-content: start | end | center | stretch |
                                        space-around | space-between | space-evenly;
                                        }</pre>
                                    <br>
                                    <p>Examples:</p>
                                    <pre>
                                        .container {
                                        justify-content: start;
                                        }</pre>

                                        <p>Example of justify-content set to start</p>
                                        <pre>.container {
                                            justify-content: end;
                                            }</pre>
                                        <p>Example of justify-content set to end</p>
                                        <pre>.container {
                                            justify-content: center;
                                            }</pre>
                                        <p>Example of justify-content set to center</p>
                                        <pre>.container {
                                            justify-content: stretch;
                                            }</pre>
                                        <p>Example of justify-content set to stretch</p>
                                        <pre>.container {
                                            justify-content: space-around;
                                            }</pre>
                                        <p>Example of justify-content set to space-around</p>
                                        <pre>.container {
                                            justify-content: space-between;
                                            }</pre>
                                        <p>Example of justify-content set to space-between</p>
                                        <pre>.container {
                                            justify-content: space-evenly;
                                            }</pre>

                                        <h4>Align Content</h4>
                                        <p>
                                            Sometimes the total size of your grid might be less than
                                            the size of its grid container. This could happen if all
                                            of your grid items are sized with non-flexible units
                                            like px. In this case you can set the alignment of the
                                            grid within the grid container. This property aligns the
                                            grid along the block (column) axis (as opposed to
                                            justify-content which aligns the grid along the inline
                                            (row) axis).

                                            Values:</p>
                                        <!--list here--><ul id="justify-cont-list">
                                        <li><code>start</code> – aligns the grid to be flush with the start edge
                                        of the grid container</li>
                                        <li><code>end</code> – aligns the grid to be flush with the end edge of
                                        the grid container</li>
                                        <li><code>center</code> – aligns the grid in the center of the grid
                                        container</li>
                                        <li><code>stretch</code> – resizes the grid items to allow the grid to
                                        fill the full height of the grid container</li>
                                        <li><code>space-around</code> – places an even amount of space between
                                        each grid item, with half-sized spaces on the far ends</li>
                                        <li><code>space-between</code> – places an even amount of space between
                                        each grid item, with no space at the far ends</li>
                                        <li><code>space-evenly</code> – places an even amount of space between
                                        each grid item, including the far ends</li>
                                        <!--List end--></ul>
                                        <xmp>
                                            .container {
                                            align-content: start | end | center | stretch |
                                            space-around | space-between | space-evenly;
                                            }</xmp>
                                        Examples:
                                        <xmp>
                                            .container {
                                            align-content: start;
                                            }</xmp>
                                        Example of align-content set to start
                                        <xmp>.container {
                                            align-content: end;
                                            }</xmp>
                                        Example of align-content set to end
                                        <xmp>.container {
                                            align-content: center;
                                            }</xmp>
                                        Example of align-content set to center
                                        <xmp>.container {
                                            align-content: stretch;
                                            }</xmp>
                                        Example of align-content set to stretch
                                        <xmp>.container {
                                            align-content: space-around;
                                            }</xmp>
                                        Example of align-content set to space-around
                                        <xmp>.container {
                                            align-content: space-between;
                                            }</xmp>
                                        Example of align-content set to space-between
                                        <xmp>.container {
                                            align-content: space-evenly;
                                            }</xmp>

                                        <h4>Place Content</h4>
                                        <p>Place-content sets both the align-content and
                                            justify-content properties in a single declaration.

                                            Values:</p>

                                        <xmp>
                                            <align-content> / <justify-content>
                                        </xmp>
                                        <p>The first value
                                            sets align-content, the second value
                                            justify-content. If the second value is omitted,
                                            the first value is assigned to both properties.
                                            All major browsers except Edge support the
                                            place-content shorthand property.

                                            For more details, see align-content and
                                            justify-content.</p>


                                        <h4> Grid Auto Columns
                                            Grid Auto Rows</h4>
                                        <p>Specifies the size of any auto-generated grid
                                            tracks (aka implicit grid tracks). Implicit
                                            tracks get created when there are more grid
                                            items than cells in the grid or when a grid item
                                            is placed outside of the explicit grid. (see The
                                            Difference Between Explicit and Implicit Grids)

                                            Values:</p>
                                        <!--list  start firgure out what to do for whole thing BIG LIST-->

                                        <xmp>
                                            <track-size>
                                        </xmp> <p>– can be a length, a percentage, or
                                        a fraction of the free space in the grid
                                        (using the fr unit)</p>
                                        <pre>.container {
                                        grid-auto-columns: <track-size> ...;
                                                grid-auto-rows: <track-size> ...;
                                                    }</pre>
                                        <p>To illustrate how implicit grid
                                        tracks get created, think about
                                        this:</p>
                                        <pre>
                                                    .container {
                                                    grid-template-columns: 60px 60px;
                                                    grid-template-rows: 90px 90px;
                                                    }</pre>
                                        <p>Example of 2x2 grid
                                        This creates a 2 x 2 grid.

                                        But now imagine you use grid-column
                                        and grid-row to position your grid
                                        items like this:</p>
                                        <pre>
                                                    .item-a {
                                                    grid-column: 1 / 2;
                                                    grid-row: 2 / 3;
                                                    }
                                                    .item-b {
                                                    grid-column: 5 / 6;
                                                    grid-row: 2 / 3;
                                                    }</pre>
                                        <p>Example of implicit tracks
                                        We told <code>.item-b</code> to start on column
                                        line 5 and end at column line 6, but
                                        we never defined a column line 5 or
                                        6. Because we referenced lines that
                                        don’t exist, implicit tracks with
                                        widths of 0 are created to fill in
                                        the gaps. We can use
                                        <code>grid-auto-columns</code> and <code>grid-auto-rows</code>
                                        to specify the widths of these
                                        implicit tracks:</p>

                                        <pre>
                                                    .container {
                                                    grid-auto-columns: 60px;
                                                    }</pre>
                                                    <code>
                                                    grid-auto-columns-rows
                                                    grid-auto-flow</code></pre>
                                                    <p>If you have grid items that you
                                                    don’t explicitly place on the grid,
                                                    the auto-placement algorithm kicks
                                                    in to automatically place the items.
                                                    This property controls how the
                                                    auto-placement algorithm works.</p>

                                                    Values:
                                                        <ul id="final-list">
                                                    <li></li><code>row</code> – tells the auto-placement
                                                    algorithm to fill in each row in
                                                    turn, adding new rows as necessary
                                                    (default)</li>
                                                    <li><code>column</code> – tells the auto-placement
                                                    algorithm to fill in each column in
                                                    turn, adding new columns as
                                                    necessary</li>
                                                    <li></li><code>dense</code> – tells the auto-placement
                                                    algorithm to attempt to fill in
                                                    holes earlier in the grid if smaller
                                                    items come up later</li></ul>
                                                    <pre>
                                                    .container {
                                                    grid-auto-flow: row | column | row
                                                    dense | column dense;
                                                    }</pre>
                                        <p>Note that dense only changes the
                                        visual order of your items and might
                                        cause them to appear out of order,
                                        which is bad for accessibility.</p>

                                        Examples:

                                        Consider this HTML:
                                        <xmp>
                                            <section class="container">
                                                <div class="item-a">item-a</div>
                                                <div class="item-b">item-b</div>
                                                <div class="item-c">item-c</div>
                                                <div class="item-d">item-d</div>
                                                <div class="item-e">item-e</div>
                                            </section>
                                        </xmp>
                                        <p>You define a grid with five columns
                                        and two rows, and set <code>grid-auto-flow</code>
                                        to row (which is also the default):</p>
                                        <xmp>
                                            .container {
                                            display: grid;
                                            grid-template-columns: 60px 60px
                                            60px 60px 60px;
                                            grid-template-rows: 30px 30px;
                                            grid-auto-flow: row;
                                            }</xmp>
                                        <p>When placing the items on the grid,
                                        you only specify spots for two of
                                        them:</p>
                                        <xmp>
                                            .item-a {
                                            grid-column: 1;
                                            grid-row: 1 / 3;
                                            }
                                            .item-e {
                                            grid-column: 5;
                                            grid-row: 1 / 3;
                                            }</xmp>
                                        <p>Because we set <code>grid-auto-flow</code> to
                                        <code>row</code>, our grid will look like this.
                                        Notice how the three items we didn’t
                                        place <code>item-b, item-c and item-d</code>
                                        flow across the available rows:

                                        Example of <code>grid-auto-flow</code> set to row
                                        If we instead set <code>grid-auto-flow</code> to
                                        <code>column</code>, item-b, item-c and item-d
                                        flow down the columns:</p>
                                        <pre>
                                                    .container {
                                                    display: grid;
                                                    grid-template-columns: 60px 60px
                                                    60px 60px 60px;
                                                    grid-template-rows: 30px 30px;
                                                    grid-auto-flow: column;
                                                    }</pre>
                                        Example of <code>grid-auto-flow</code> set to

                                        <h4>Column Grid</h4>
                                        <p>
                                            A shorthand for setting all of the
                                            following properties in a single
                                            declaration: <code>grid-template-rows,
                                                    grid-template-columns,
                                                    grid-template-areas, grid-auto-rows,
                                                    grid-auto-columns,
                                                    grid-auto-flow</code> (Note: You can only
                                            specify the explicit or the implicit
                                            grid properties in a single grid
                                            declaration).</p>

                                        <p>Values:

                                        <code>none</code> – sets all sub-properties to
                                        their initial values.</p>
                                        <xmp>
                                            <grid-template>
                                        </xmp> <p>– works the same as
                                        the grid-template shorthand.
                                        <code>grid-template-rows</code> / [
                                        auto-flow && dense? ]
                                        <code>grid-auto-columns?</code> – sets
                                        <code>grid-template-rows</code> to
                                        the specified value. 
                                        <br>
                                        If
                                        the <code>auto-flow</code> keyword is
                                        to the right of the
                                        slash, it sets
                                        <code>grid-auto-flow</code> to
                                        column. 
                                        <br>
                                        If the dense
                                        keyword is specified
                                        additionally, the
                                        <code>auto-placement</code> algorithm
                                        uses a “dense” packing
                                        algorithm. 
                                        <br>
                                        If
                                        <code>grid-auto-columns</code> is
                                        omitted, it is set to
                                        auto.
                                        <code>grid-auto-rows</code> /
                                        <code>grid-template-columns</code>
                                        – sets
                                        <code>grid-template-columns</code>
                                        to the specified
                                        value. 
                                        <br>
                                        If the
                                        <code>auto-flow</code>
                                        keyword is to
                                        the left of the
                                        slash, it sets
                                        <code>grid-auto-flow</code>
                                        to row. 
                                        <br>
                                        If the
                                        dense keyword is
                                        specified
                                        additionally,
                                        the
                                        <code>auto-placement</code>
                                        algorithm uses a
                                        “dense” packing
                                        algorithm.
                                        <br>    
                                        If <code>grid-auto-rows</code>
                                        is omitted, it
                                        is set to <code>auto</code>.
                                        Examples:

                                        The following
                                        two code blocks
                                        are equivalent:</p>
                                        <pre>
                                        .container {
                                        grid: 100px
                                        300px / 3fr 1fr;
                                        }

                                        .container {
                                        grid-template-rows:
                                        100px 300px;
                                        grid-template-columns:
                                        3fr 1fr;
                                        }</pre>
                                        <p>The following
                                        two code blocks
                                        are equivalent:</p>
                                        <pre>
                                        .container {
                                        grid: auto-flow
                                        / 200px 1fr;
                                        }

                                        .container {
                                        grid-auto-flow:
                                        row;
                                        grid-template-columns:
                                        200px 1fr;
                                        }</pre>
                                        <p>The following
                                        two code blocks
                                        are equivalent:</p>
                                        <pre>
                                        .container {
                                        grid: auto-flow
                                        dense 100px /
                                        1fr 2fr;
                                        }

                                        .container {
                                        grid-auto-flow:
                                        row dense;
                                        grid-auto-rows:
                                        100px;
                                        grid-template-columns:
                                        1fr 2fr;
                                        }</pre>
                                        <p>And the
                                        following two
                                        code blocks are
                                        equivalent:</p>
                                        <pre>
                                        .container {
                                        grid-auto-flow:
                                        row dense;
                                        grid-auto-rows:
                                        100px;
                                        grid-template-columns:
                                        1fr 2fr;
                                        }

                                        .container {
                                        grid-template-rows:
                                        100px 300px;
                                        grid-auto-flow:
                                        column;
                                        grid-auto-columns:
                                        200px;
                                        }</pre>
                                        <p>It also accepts
                                        a more complex
                                        but quite handy
                                        syntax for
                                        setting
                                        everything at
                                        once. You
                                        specify<code>
                                        grid-template-areas,
                                        grid-template-rows,
                                        grid-template-columns</code>,
                                        and all the
                                        other
                                        sub-properties
                                        are set to their
                                        initial values.
                                        What you’re
                                        doing is
                                        specifying the
                                        line names and
                                        track sizes
                                        inline with
                                        their respective
                                        grid areas. This
                                        is easiest to
                                        describe with an
                                        example:</p>
                                        <pre>
                                        .container {
                                        grid:
                                        [row1-start]
                                        "header header
                                        header" 1fr
                                        [row1-end]
                                        [row2-start]
                                        "footer footer
                                        footer" 25px
                                        [row2-end]
                                        / auto 50px
                                        auto;
                                        }</pre>
                                        <p>That’s
                                        equivalent to
                                        this:</p>
                                        <pre>
                                        .container {
                                        grid-template-areas:
                                        "header header
                                        header"
                                        "footer footer
                                        footer";
                                        grid-template-rows:
                                        [row1-start] 1fr
                                        [row1-end
                                        row2-start] 25px
                                        [row2-end];
                                        grid-template-columns:
                                        auto 50px auto;
                                        }</pre>
        </section>

        <section class="main-section" id="Reference">
            <header>
                <h3>Reference</h3>
            </header>
            <p>Click on the links for the documentation that all this information came from.</p>
            <a href="https://www.smashingmagazine.com/2011/01/guidelines-for-responsive-web-design/">Introduction</a>
            <br>
            <a href="https://www.freecodecamp.org/learn/responsive-web-design">Responsive Web Design</a>
            <br>
            <a href="https://css-tricks.com/snippets/css/a-guide-to-flexbox/">Flexbox</a>
            <br>
            <a href="https://css-tricks.com/snippets/css/complete-guide-grid/">Grid</a>

        </section>
    </main>


</body>

</html>
