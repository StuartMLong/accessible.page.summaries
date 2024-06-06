The Problem Is Unintended Systemic Bias

Existing technology is systemically denying blind screen reader users an equal user experience. Because summary information about Web pages is being withheld from blind assistive technology users. Conversely, robots have had access to summary information in the form of meta description tags, open graph tags and SEO markup for many years. While sighted Web page users can often determine when a Web page is of interest to them in under three seconds. Yet blind screen reader users have been expected to tab from heading to heading and alt text to alt text, literally flying blind through HTML, in order to determine when a Web page is of interest to them. To make blind assistive technology users equal to sited users and robots, I'm proposing the adoption of Accessible Page Summaries. Because including a brief summary, along with information about content size, will allow blind screen reader users to finally make quick determinations about Web pages, just like sited users and robots have been able to do for a long time.

Why not rely on open graph and meta description tags for summarized content? Because the needs of search engines and the needs of blind assistive technology users are fundamentally different. Basically, SEO is a methodical reaction to every Web page jockeying for position on Search Engine Results Pages. Which is why open graph and meta description tags attempt to include every relevant search term, in order to increase the odds of click through's. What blind screen reader users need is not a competition for their attention. They need concise summaries that get right to the point, composed specifically for humans, and valid information about content length.

The Solution

Introducing Accessible Page Summaries, an innovative way to provide high quality preliminary information (who, what, where, when and why) including content size, intended specifically to serve the needs of blind assistive technology users.

Features

The default configuration is opt-out, requiring screen reader users to opt-in.
Accessible Page Summaries cannot be seen by sighted users and will not alter the appearance of standards compliant Web pages.
Accessible Page Summaries have no dependencies so they will always work without fail and work offline too. Being integrated into each Web page means it will never be subjected to URL and redirect errors.
100% WCAG 2.1 AAA compliant.

How It Works

By design, the Accessible Page Summary is positioned so far to one side that no one can see it and it will not change the appearance of any Web page. When screen reader users visit a Web page with an Accessible Page Summary, they have the option to open it and access the preliminary content, or by default, continue past it when revisiting a Web page.

Risks and Mitigation

The included CSS does three things. 1. It provides functionality to open the Accessible Page Summary. 2. It positions the Accessible Page Summary off screen. 3. It formats the Accessible Page Summary to pass WCAG 2.1 AAA.

Because CSS is fundamental to HTML, CSS was chosen over Java script, to handle the opt-in "open" function that can be selected by screen reader users.

Here is why the CSS must be included in the head section. Because when the functionality of the CSS is sourced from a dependency CSS file it may not function offline, may not function due to CDN failure, may fail due to redirect errors and may fail as a result of DNS errors. By being included in the head section, and by being 100% free of dependencies, the CSS opt-in "open" function cannot fail, the summary will always remain off screen, and will be WCAG 2.1 AAA compliant at all times.

What Else Is Possible?

Future versions could be opened by an "i" for information button, to be included in every Web browser, intended for sited users, that would open complete Accessible Page Summary content in a sidebar. Then everyone will be able to benefit from Accessible Page Summaries.

What Happens Next

The variations provided here are for Web pages. More work is needed to develop Accessible Page Summaries for PDF's, Ebooks, and other document types. It is my hope that talented engineers will be inspired by this open source project and help make it happen.

The Accessible Page Summary should be a WCAG requirement. It might also make sense to include the Accessible Page Summary as fundamental to HTML5.

https://ada-ps.org

How To Use

1. The CSS must be included in the head section of the Web page. Never add it to a dependency CSS file.
2. The HTML is added to the Web page immediately following the h1 tag.
3. Keep the preliminary information brief and always include who, what, where, when and why.
4. Conclude the summary with information about content size, such as a word count, running time, long read, short read, etc.

For Typical Web Pages
<code><!-- Accessible Page Summary CSS - BEGIN -->
<style>/* Opt-Out (default) */.ADA-ps {display: none}/* Opt-In (selectable) */.Summary-Opt-In:focus+.ADA-ps {display: block}/* WCAG 2.1 AAA */.ada-ps-css-01 {background: #fff; color: #000;display: inline-block; font-size: 1.5rem; line-height: 150%; margin-left: -3000rem; position: absolute; z-index: 997}</style>
<!-- Accessible Page Summary CSS - END -->
<!-- FOR TYPICAL WEB PAGES - ADA P.S. 1 -->
<!-- Accessible Page Summary - BEGIN -->
<!-- Passed WCAG 2.1 AAA 08/25/2023 -->
    <section role="complementary" aria-label="Note about usage" class="ada-ps-css-01">
    <h2>To Hear a Brief Summary of This Web Page Including Content Size Click Open. Then use the down arrow.</h2>
    <button aria-pressed="false" value="Open" class="Summary-Opt-In">Open</button>
    <section role="complementary" aria-label="Note about usage" class="ADA-ps">
    <p><!-- description -->
    Web Page Description.<br>
    Replace this line with a Description of the Web page that does not duplicate the meta description tag.</p>
    <p><!-- alt text summary -->
    Alt Text Summary.<br>
    Replace this line with a very brief summation of all images.</p>
    <p><!-- content size -->
    Content Size.<br>
    Replace this line with the word count or, short reed, long reed, length of video, etc.
    <!-- never remove this line -->
    That completes the Summary. The Web page content starts now.</p>
    </section></section>
<!-- Accessible Page Summary - END --></code>

For 100% Text Web Pages
<code><!-- Accessible Page Summary CSS - BEGIN -->
<style>/* Opt-Out (default) */.ADA-ps {display: none}/* Opt-In (selectable) */.Summary-Opt-In:focus+.ADA-ps {display: block}/* WCAG 2.1 AAA */.ada-ps-css-01 {background: #fff; color: #000;display: inline-block; font-size: 1.5rem; line-height: 150%; margin-left: -3000rem; position: absolute; z-index: 997}</style>
<!-- Accessible Page Summary CSS - END -->
<!-- FOR 100% TEXT WEB PAGES - ADA P.S. 2 -->
<!-- Accessible Page Summary - BEGIN -->
<!-- Passed WCAG 2.1 AAA 08/25/2023 -->
    <section role="complementary" aria-label="Note about usage" class="ada-ps-css-01">
    <h2>To Hear a Brief Summary of This Web Page Including Content Size Click Open.
    Then use the down arrow.</h2>
    <button aria-pressed="false" value="Open" class="Summary-Opt-In">Open</button>
    <section role="complementary" aria-label="Note about usage" class="ADA-ps">
    <p><!-- description -->
    Web Page Description.<br>
    Replace this line with a Description of the Web page that does not duplicate the meta description tag.</p>
    <p><!-- content size -->
    Content Size.<br>
    Replace this line with the word count
    or, short reed, long reed, length of video, etc.
    <!-- never remove this line -->
    That completes the Summary.
    The Web page content starts now.</p>
    </section></section>
<!-- Accessible Page Summary - END --></code>

For 100% Images Web Pages
<code><!-- Accessible Page Summary CSS - BEGIN -->
<style>/* Opt-Out (default) */.ADA-ps {display: none}/* Opt-In (selectable) */.Summary-Opt-In:focus+.ADA-ps {display: block}/* WCAG 2.1 AAA */.ada-ps-css-01 {background: #fff; color: #000;display: inline-block; font-size: 1.5rem; line-height: 150%; margin-left: -3000rem; position: absolute; z-index: 997}</style>
<!-- Accessible Page Summary CSS - END -->
<!-- FOR 100% IMAGES WEB PAGES - ADA P.S. 3 -->
<!-- Accessible Page Summary - BEGIN -->
<!-- Passed WCAG 2.1 AAA 08/25/2023 -->
    <section role="complementary" aria-label="Note about usage" class="ada-ps-css-01">
    <h2>To Hear a Brief Summary of This Web Page Including Content Size Click Open.
    Then use the down arrow.</h2>
    <button aria-pressed="false" value="Open" class="Summary-Opt-In">Open</button>
    <section role="complementary" aria-label="Note about usage" class="ADA-ps">
    <p><!-- description -->
    Web Page Description.<br>
    Replace this line with a Description of the Web page that does not duplicate the meta description tag.</p>
    <p><!-- alt text summary -->
    Alt Text Summary.<br>
    Replace this line with a very brief summation
    of all images.</p>
    <p><!-- never remove this line -->
    That completes the Summary.
    The Web page content starts now.</p>
    </section></section>
<!-- Accessible Page Summary - END --></code>

For 100% Infographic Web Pages
<code><!-- Accessible Page Summary CSS - BEGIN -->
<style>/* Opt-Out (default) */.ADA-ps {display: none}/* Opt-In (selectable) */.Summary-Opt-In:focus+.ADA-ps {display: block}/* WCAG 2.1 AAA */.ada-ps-css-01 {background: #fff; color: #000;display: inline-block; font-size: 1.5rem; line-height: 150%; margin-left: -3000rem; position: absolute; z-index: 997}</style>
<!-- Accessible Page Summary CSS - END -->
<!-- FOR 100% INFOGRAPHIC WEB PAGES - ADA P.S. 4 -->
<!-- Accessible Page Summary - BEGIN -->
<!-- Passed WCAG 2.1 AAA 08/25/2023 -->
    <section role="complementary" aria-label="Note about usage" class="ada-ps-css-01">
    <h2>To Hear a Brief Summary of This Web Page Including Content Size Click Open. Then use the down arrow.</h2>
    <button aria-pressed="false" value="Open" class="Summary-Opt-In">Open</button>
    <section role="complementary" aria-label="Note about usage" class="ADA-ps">
    <p><!-- description -->
    Web Page Description.<br>
    Replace this line with a Description of the Web page that does not duplicate the meta description tag.</p>
    <p><!-- alt text summary -->
    Alt Text Summary.<br>
    Replace this line with a very brief summation of all images.</p>
    <p><!-- content size -->
    Content Size.<br>
    Replace this line with the word count or, short reed, long reed, length of video, etc.
    <!-- never remove this line -->
    That completes the Summary. The infographic content starts now</p>
    </section>
    <section role="complementary" aria-label="Note about usage">
    <h2>The infographic content starts now.</h2>
    <p><!-- complete infographic content -->
    Infographic Information.<br>
    Statistics.<br>
    Facts.<br>
    Analysis.<br>
    Takeaway.<br>
    Sources.<br>
    <!-- never remove this line -->
    That completes the Infographic.</p>
    </section></section>
<!-- Accessible Page Summary - END --></code>

https://www.gofundme.com/help-me-help-the-blind-use-the-web
