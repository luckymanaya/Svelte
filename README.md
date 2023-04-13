# Svelte

## Fundamentals of Web Development

## Website: Lucky’s Website

## Topic: Fashion Magazine Website

## Description

<p align = "justify">My website which I named, <i>"Lucky's Website"</i>, is a fashion magazine website that provides users with fashion related content. It is built using a code editor called 'Visual Studio Code' where I used HTML, CSS, Javascript and a web framework called 'Svelte'. Lucky's Website is designed to be responsive in order to adapt to different devices with different screen sizes, increasing its accessibility. Moreover, the website is also very easy to navigate, making it user-friendly and enjoyable to use as the website follows the typical horizontal navigation menu, consisting of a 'Home' page, an 'About' page, a dropdown menu for the 'Pages' and a 'Contact Me' page. Not only it is user-friendly, but it also has a simple, yet modern look due to its black & white palette, allowing its content to become more visible which catches users' attention. It also contains animations, a slideshow and other interactive aspects in order to be considered 'visually appealing' to the users thus improving user experience and user engagement. In addition, this website also follows the usability heuristics which is used as a guide in order to create an attractive, yet functional website.
</p>

## Installation Steps

1. Clone repository
2. Install the dependencies using **npm install**
3. Display Website using **npm run dev -- --open**

## Inspirations from 3 sites(What elements did you like? Why?)

### Website #1: [Halo Media Website](https://halomedia.com/)
1. **Sans-serif fonts**

<p align = "justify">I chose the sans-serif fonts to incorporate into my website. This is because according to my research, sans-serif fonts are more ‘friendly’ and ‘approachable’ which is an effect I want my website to have. On the other hand, serif fonts are considered 'classic’ and ‘elegant’ and are ideal if you want to make your website appear ‘serious’. In addition, sans-serif fonts are considered to be more legible than serif fonts as they are more ‘clean’ and ‘simple’ due to its lack of ‘curls’ and additional ‘lines.’ This increased readability makes it ideal for people who have dyslexia or reading difficulties to read the text, which is also a feature I want in order to increase the accessibility of my website. As a result, I will use the font, ‘Arial’, as it is one of the fonts that appears ‘less crowded’. 
</p>

2. **Multiple Images**

<p align = "justify">Multiple images in large sizes attract users’ attention thus making them more involved. Too much text may irritate the users. Furthermore, for my images, I decided to make all of them have rounded corners as not only are they ‘easy on the eyes’, but rounded corners also gave a more ‘warm’ and ‘friendly’ impact in comparison to images with sharp edges. 
</p>

3. **Animation**

<p align = "justify">Animation is also a feature I want to incorporate into my website. Animations such as, zooming in an image when hovered and text animation such as the ‘fly animation’ to make the text appear vertically will make my website look ‘visually appealing’ and catch the user’s attention. It will also allow my website to share information in a more fun and memorable way. However, I plan not to use too much animation as based on my research, too much animation can distract and even annoy users.
</p>

### Website #2: [Selected Website](https://selectedbase.com/)
1. **Large font size** 

<p align = "justify">I want to use relatively large font sizes for my website because not only does it make the text legible, but it also makes it readable for the users to read. For example, a 12pt font size may be legible, however, it is not large enough to make the users actually stay in your website and read the whole text as readability takes emotions and ease of reading into consideration. As a result, I am going to make the text to have a larger font size, but not too large that it takes up a lot of space in the website. This is so that it catches users’ attention and I will also try to display less text as people do not want to read a long, daunting paragraph with a very small font size.
</p>

2. **Black & White colors** 

<p align = "justify">The black & white color palette makes the website have a minimalistic yet modern look.  Not only do the black & white colors promote simplicity but it also creates a bold contrast and makes the visual elements such as the pictures and text stand out more, which is a feature I want to incorporate into my website. 
</p>

### Website #3: [Ana Deufont - Portfolio Photography Website](https://polite-hill-00eb08f10.1.azurestaticapps.net/)
1. **Navigation Buttons**

<p align = "justify">Buttons increase interactivity between the users and the site. For my website, I will make a ‘Next’ button in order for the user to go to the next page as well as a ‘Go Back’ button so that the user can go back to the previous page whenever they like which supports one of the usability heuristics known as ‘User Control & Freedom’, meaning the user can undo an action or a mistake, allowing them to have more control and freedom. This feature will make my website to behave more like a magazine which is what I intended to do. Also, I am going to set the cursor to a 'pointer' to make the buttons appear clickable.
</p>

2. **Slideshow**

<p align = "justify">I want to incorporate this into my website as another interactive aspect. Also, it will increase user engagement in terms of the visual aspect of the site. It is also another way to display multiple images on a single page which saves up space.
</p>

## Other Features:
<p align = "justify">In the main page, I added an additional interactive aspect by adding a greeting based on the local time and a textbox that asks the user’s name and displays it. After clicking ‘continue’, it goes to the next section ‘smoothly’.
</p>

<p align = "center">
<img src = "Main.PNG" 
alt = "Screenshot of feature in the Main Page">
</p>

## Process
### Struggles & Bugs
1. **HTML, CSS & JavaScript**

<p align = "justify">I have a limited knowledge in HTML and CSS and have never coded in JavaScript before so it was a bit of a struggle to code the website. But thankfully,  there are resources available online such as, "MDN Web Docs" which is a learning resource used by web developers and Moodle.
</p>

2. **Layout (secondPage)**

<p align = "justify">I struggled a bit with displaying an image and a text (which is the words I stored in an array) side by side but I solved it using 'margin-left'. After that, I found another bug which is that when you go to the next page and go back again, the text disappears. In the end, I decided to put the for each loop inside the class of the picture and then print each words in the array of words which solved the problem.
</p>

3. **Layout (Nav Bar & other elements)**

<p align = "justify">I was struggling to separate the navigation bar and the other elements like the header, so I used a lot of line breaks (br) to separate them but turns out, I can just use margin- top.
</p>

4. **Slideshow**

<p align = "justify">I wanted to incorporate this feature into my website at the start of the website development and at first, I had to use the W3Schools to learn how to do it, but unfortunately, that did not work and there were too much code that I mostly did not understand. In the end, I used the Svelte tutorials to learn how to make a slideshow. At first, I made an array of image files and a for each loop as I initially wanted it to display the images one by one, however, that did not work so I decided to make an if statement which checks if the length of images is not empty (greater than zero) and if condition is true, image will be displayed. I also put the next and previous buttons inside the if statement to make the previous button go to the left side and the next button go to the right side as I initially put the buttons outside the if statement, making the buttons to be displayed on the top of slideshow which I did not want.
</p>

5. **Display User’s Name**

<p align = "justify">In the first page of the website, the user’s name is displayed after inputting a name, however, when I go to the next page and then back to the first page, the user’s name disappears. It also accepts numbers and special characters which are invalid inputs.
</p>

## References:
https://www.awwwards.com/ (Website Inspirations)

https://unsplash.com/ (Pictures)

https://developer.mozilla.org/en-US/ (MDN Web Doc)

https://svelte.dev/ (Svelte)

https://svelte.dev/tutorial/basics (Svelte Tutorials)

### Research for Website Design

https://designmodo.com/rounded-corners/ (Rounded Corners in Images)

https://www.impactplus.com/blog/sans-serif-vs-serif-font-which-should-you-use-when (Font style)

https://www.bdadyslexia.org.uk/advice/employers/creating-a-dyslexia-friendly-workplace/dyslexia-friendly-style-guide#:~:text=Readable%20fonts,may%20request%20a%20larger%20font. (Dyslexia Friendly Fonts)

https://www.studiorubric.co/blog/insight/font-size-matters-why-you-should-design-with-a-larger-font (Font Size)

https://boldist.co/web-design/using-animations-in-web-design/ (Animation)

### Usability Heuristics

https://www.nngroup.com/articles/ten-usability-heuristics/

### Bug Solution

https://developer.mozilla.org/en-US/docs/Web/API/Window/localStorage (Web Storage)

### Other Features
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date/getHours (Greetings based on local time feature)
