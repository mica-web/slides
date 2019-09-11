# HTML5 organizational elements

???
-  to date, mostly one-to-one elements to content
- `ul`, `ol` exceptions as they aren't visible and wrap list items
- going to explore some more elements that are like that; unlike lists, these elements can hold practically any other HTML elements
- @timer=


--
count: false

- `header`


--
count: false

- `footer`


--
count: false

- `main`


--
count: false

- `nav`


---
count: false

# Structural analysis

.cf[.left-float[
- `header`
- `footer`
]
.right-float[
- `main`
- `nav`
]]

--
count: false

- Identity structural elements
- Note elements you struggle to label


???
- @timer=
- partner up and take 10m to explore some web sites with these elements in mind
  - content-heavy sites vs ones _only_ visual
- what structural elements can you identify?
    - don't look at the markup yet!
- which elements do you struggle to label?
    - check markup: ⬅️ make sure everyone knows how to do this
      - agree/disagree?
      - if element is unfamiliar, look it up in MDN
- send me a link via DM in Slack to a site you want to present and discuss
- will post these instructions to the #general channel of Slack
- @timer=


---

# HTML5 organizational elements


???
- We'll dive more deeply into the sites you reviewed in a few, but first: how hard was it to identify the elements that make up the page?
- What made it difficult?
- Did you learn any new HTML elements?


--
count: false

## `header`

???
- Describe in your own words
- Can there be more than 1 header per page?


--
count: false

## `footer`


--
count: false

## `nav`


???
- purpose is to provide navigation LINKS within this document and to other documents; menu, indexes, table of contents
- more than one `nav` per page?
    - site nav/menu, pagination, ToC links like Wikipedia uses


--
count: false

## `main`


???
- dominant content and subject of the page
- unique content; should not include repeated elements like site header, nav or sidebars
- only one `main` per page
- @timer=


---

# Structural analysis, part II

- Recreate the site layout structure using no text, no images
    - Only colors and simple geometric shapes


???
- Using the software of your choice (e.g., InDesign, Illustrator or Sketch), recreate the layout structure of the site you explored
- Express the structure only using simple geometric shapes for the contents (e.g., header with thick black line, body text with thin grey line, image with green rectangular box, etc)
- Do not write any text or use any images
- Send me a DM with a a screenshot of the site you're working from and upload a JPG/PNG/GIF of your version of its layout structure
- https://github.com/cdaein/mica-gd220/blob/spring2019/lectures/w1-structure-analysis.md
- @timer=
- take an additional 10-15m to go through examples and discuss
  - what does the site do design-wise to communicate these elements and its hierarchy?
  - what does the abstraction/wireframe make more clear about the site?
- @timer=
- @break for dinner?

--
count: false

![layout structure examples](img/03_layout-structure.png)


---
count: false

# Agenda

1. ~~Slack Q&A~~
1. ~~Discuss W2 reading on history of web design~~
1. ~~HTML Q&A~~
1. HTML5 👈🏻
1. Discuss W3 reading
1. Style tiles
1. Proj 1 overview


---
# HTML5 organizational elements

--
count: false

## `section`


???
- standalone content
- usually has a heading


--
count: false

## `aside`

???
- indirectly related to main content

--
count: false

## `div`


???
- most generic container element
- consider if there are any other options
- this doesn't mean it needs to be avoided, just that it's generic enough and therefore too easy to default to

--
count: false

## `span`

???
- generic inline container
- add others based on discussion of structural analysis?
- @timer=


---
class: center, middle, title

# HTML structure Q&A


???
- Anything left unsaid?
- Anything remain confusing?
