# Team notes
This is for maintaining communication about your team's working meetings to "ship" the project.

## Meeting notes
These are notes to be maintained PER date that you meet. What you did and what the next steps are
### Meeting Date

#### What we did:


#### What we'll do next

## October 5
#### What are the characteristics of the card?
- icon
- colored banner
- headers and subheader (banner)
- content body
#### What design considerations must we take into account?
- contrast
- tab to body content
- heading order
#### What accessibility concerns do we potentially have?
- i18n
#### What security concerns do we potentially have?
- flexibility of the content security
#### What "states" does this card have?
- hover
- disabled
- click to show
- type of card 
#### What do we call it?
- sci-card-hover
- sci-card-disabled
- sci-card-focus
- sci-card-resize
#### What areas do we need to account for flexible content / HTML entry of any kind?
- size of card
- heading overflow
#### Do we have room for additional reusable atoms to be produced? (there are 4 total by my count)
- icon
- body
- title
- header/banner
#### What should we call each of them?
- sci-card -> Nick
- sci-card-banner -> Bailey
- sci-card-icon -> Nicole
- sci-card-content-body -> Noelle

## October 14
#### What did you take away from the portion of class about implementing SimpleColors?
-	It seems like a simpler way to add and balance coloring in the project.
-	Very valuable functionality to extend a functional dark theme that reverses colors out of the box.
#### What did you learn from other groups?
-	I learned that there is an extra layer of difficulty in if you copy and paste from the template for each element vs if you pull pieces of the code out as you need them to get it to work as expected.
-	I learned more my portion of the project being the icon. I worked with the other people in the groups who were also working on the icon section and learned what they are doing and told them about what my ideas were.
-	I also learned that it's important to think of each of the four elements modularly, to think about how their spacing and function will interact within the scaffolded bounds of the card. 
#### What are your next steps?
-	Get the basic header/banner working
-	Get the basic icon working
-	Work on developing our expandable card scaffold via using the details and summary tags which support expandable content natively.

## October 19
#### What approaches can you leverage from his example to enhance your team's element?
- different rendering functions
- css styles
- responsive design (proportions)
#### How could you take his approach and envision a more flexible version?
- implement the slot within a slot approach as shown in class to make it more flexible
- refine the different rendering functions to reduce repetitive code
#### What are your next steps?
- update css
- responsive design
- icon changes

## Status check ins
These are dedicated status check-ins as this is a multi-week project
### Check-in 1
- The possible names of our four elements are:
  - sci-card -> Nick
    - Properties & Design:
      - Slide State (Open/Closed)
      - Disabled
      - Expanded State
      - Pane Focus
      - Given that this card will involve a 2 pane system, where the top pane slides to "reveal" content below it, the design will need to specify horizontal scroll boundaries so that the upper pane can only slide so far open as to not overflow other content on the page.
  - sci-card-banner -> Bailey
    - Properties & Design:
      - Class
      - Theme
      - Title
      - The banner will contain a header and a subheader within it, and contain a variation of the icon element as well.
      - The banner will need to be responsive based on the width of the card itself.
      - The banner will need to adapt the font size of the heading and subheading text depending on the size of the header so that the text follows appropriate typography hierarchy.
  - sci-card-icon -> Nicole
    - Properties & Design:
      - Size/Dimensions
      - Theme/Color Scheme
      - Supporting a number of themes and different sizes could create readability or contrast issues if the icon gets too small. Understanding which icon designs are still visible with smaller dimensions will be crucial for supporting smaller displays.
  - sci-card-content-body -> Noelle
    - Properties & Design:
      - Content Type (Text, image, etc.)
      - Text
      - Max-length
      - The design of the body will need to take into account the max size or length of content in the body, and potentially hide overflow content inside of an optional dropdown drawer if the amount of text was too large.

- Card will support swiping to expand a drawer on the side of the card. The drawer will contain a list of icons that can be clicked to update the content displayed on the card's front pane.


- Next reponsibilities:
  - Nick: Begin experimenting with how to create a layered card while controling the horizontal "slide" distance and behavior.
  - Bailey: Research flexbox and begin designing the banner layout to support various card widths.
  - Nicole: Investigate the best way to support various icon sizes, both within our header and on the inner card pane. Also ideate upon the types of card content we want to support and finding icons that accurately represent that content.
  - Noelle: Research on flexbox and how to appropriately contain different types of content in the same card body area. This includes text content, images, and and potentially iFrames. Would conditional rendering be enough, or would this create issues with resposiveness of content relative to the card scaffolding?

### Check-in 2
- For Check-in 2, we worked to create a scaffold for a basic API for the overall card.  From there, we integrated in the header/banner element with an icon modeled after the example provided and supporting two named slots (main header and sub header).  Lastly, we worked to dynamically import the icon definition in the life-cycle of the header/banner element. 

- Nick: Integrated elements that exist to date into the scaffold
- Bailey: Scaffolded the banner element out, setting up the the main-header and sub-header slots to render appropriate text content
- Nicole: Planned out icon handling and API rendering
- Noelle: Helped with card content layout and research. She was ill and out of class for most of the week so she is getting reintegrated to Project 2 as well.
### Check-in 3
- As of this point, we've worked to create a scaffold for the overall card, banner elements, and the icon. We spent time reviewing comments from the last check-in and class discussion to improve our elements.  All of the elements have been started, the icon element is essentially finished and is dynamically rendering, the header/banner element is looking like the example, and the card scaffolding is being worked on.
- A problem we faced was determining how we wanted the overall scaffolding of the card to work, but through discussion in class and within our group, the structure was figured out.
- Our team chose to implement a custom Google font (Open Sans) as part of our blog post, utilizing the swap functionality provided by Lit.
- Our next steps will be to continue to work on improving the card given the feedback and discussion in class this week. We will work on improving the CSS styling for the card and start to look at what it would look like to implement our button from the last assignment within this card.
### Check-in 4
- For this check in, we worked to finish up some of the things we've been working on including adding the use of simple colors and the button from the last project.
- We also created the storyboard for the project and added a default card style for when one of the 3 types is not selected
- Things we need to do (may or may not be done for this check in)
  - make expanded by default
  - finish adding button
  - create tests
