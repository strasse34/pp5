# Ride Review

Developer: Reza Mirzaie

![Mockup image](docs/responsive.png)

[View live website](https://ride-review-63e228ade7d7.herokuapp.com/)

## Table of Contents

- [About](#about)
- [Project Goals](#project-goals)
  - [User Goals](#user-goals)
- [User Experience](#user-experience)
  - [Target Audience](#target-audience)
  - [User Stories](#user-stories)
    - [Profile Page](#profile-page)
    - [Navigation and Authentication](#navigation-and-authentication)
    - [Adding and Liking Posts](#adding-and-liking-posts)
    - [Post Page](#post-page)
    - [The Posts Page](#the-posts-page)
- [Wireframes](#wireframes)
- [Technologies Used](#technologies-used)
  - [Languages](#languages)
  - [Libraries, frameworks and dependencies](#libraries-frameworks-and-dependencies)
  - [Tools & Programs](#tools--programs)
- [Agile design](#agile-design)
  - [About](#about-1)
  - [User Story Template](#user-story-template)
  - [Kanban Board](#kanban-board)
  - [Moscow Prioritisation](#moscow-prioritisation)
  - [Milestones](#milestones)
- [Design](#design)
  - [Colours](#colours)
  - [Fonts](#fonts)
- [Project Structure](#project-structure)
  - [Front-End](#front-end)
    - [React](#react)
  - [Back-End API](#back-end-api)
    - [Django REST Framework](#django-rest-framework)
- [Features](#features)
  - [Implemented Features](#implemented-features)
    - [Navigation(Navbar)](#navigationnavbar)
    - [Sign Up Page](#sign-up-page)
    - [Sign In Page](#sign-in-page)
    - [HomePage](#homepage)
      - [Popular Profiles](#popular-profiles)
      - [Posts Page](#posts-page)
      - [Search-bar](#search-bar)
    - [Feed Page](#feed-page)
    - [Liked Page](#liked-page)
    - [post Detail Page](#post-detail-page)
    - [post Create Page](#post-create-page)
    - [post Edit Page](#post-edit-page)
    - [Profile Page](#profile-page-1)
    - [Profile Edit Page](#profile-edit-page)
    - [Change Username Page](#change-username-page)
    - [Change Password Page](#change-password-page)
    - [Page Not Found](#page-not-found)
  - [Features to be Implemented](#features-to-be-implemented)
- [Validation](#validation)
  - [CSS](#css)
  - [Html](#html)
  - [Lighthouse](#lighthouse)
- [Testing](#testing)
- [Deployment](#deployment)
  - [Deploying the website in Heroko](#deploying-the-website-in-heroko)
    - [Login or create an account at Heroku](#login-or-create-an-account-at-heroku)
    - [Creating an app](#creating-an-app)
    - [Open Deploy Tab](#open-deploy-tab)
      - [Choose deployment method](#choose-deployment-method)
      - [Connect to Github](#connect-to-github)
      - [Automatic and Manual deploy](#automatic-and-manual-deploy)
      - [Deployment](#deployment-1)
    - [Forking the GitHub Repository](#forking-the-github-repository)
    - [Cloning the repository in GitHub](#cloning-the-repository-in-github)
- [Credits](#credits)
  - [Images](#images)
  - [Code](#code)
- [Thank You](#thank-you)

## About

The Ride Review project aims to provide users with a platform to share their experiences and reviews of various rides with cars. Leveraging modern web technologies and React components, Ride Review offers an intuitive interface for users to create, browse, and interact with ride reviews. Whether it's sharing insights on a recent road trip or rating the comfort of a new car model, Ride Review empowers users to contribute to a community-driven database of car reviews. With its user-friendly design and robust features, Ride Review brings together enthusiasts, commuters, and travelers alike to exchange valuable information and make informed decisions about their rides.

## Project Goals

The key functionality aspects:

- simple and intuitive navigation across all pages
- user authentication
- user interaction via posts, comments, likes, followers
- user profiles with their description and images
- CRUD functionality for posts, comments, likes and profile information
- posts filtering by brand, model, production year, other details
- posts filtering by liked posts and followed users posts

### User Goals

- Ability to post a post
- Be able to comment on a post
- Ability to amend and update content
- Ability to rate along with commenting a post
- Able to like a post
- Able to follow a user

## User Experience

### Target Audience

- Everybody who want to share riding experience of a car
- Everybody who want to buy a car and need to know about different brands of cars

### User stories

#### Profile Page

1. **Profile Page**: As a user, I can view other users' profiles so that I can see their posts and learn more about them.
2. **Most Followed Profiles**: As a user, I can see a list of the most followed profiles so that I can see which profiles are popular.
3. **User Profile - User Stats**: As a user, I can view statistics about a specific user: bio, favorite car, number of posts, follows and users followed so that I can learn more about them.
4. **Follow/Unfollow a User**: As a logged-in user, I can follow and unfollow other users so that I can see and remove posts by specific users in my posts feed.
5. **View All Posts by a Specific User**: As a user, I can view all the posts by a specific user so that I can catch up on their latest posts, or decide I want to follow them.
6. **Edit Profile**: As a logged-in user, I can edit my profile so that I can change my profile picture, bio, username, and password.
7. **Update Username and Password**: As a logged-in user, I can update my username and password so that I can change my display name and keep my profile secure.

#### Navigation and Authentication

1. **View Navbar**: As a user, I can view a navbar from every page so that I can navigate easily between pages.
2. **Create Account**: As a user, I can create a new account so that I can access all the features for signed-up users.
3. **Sign In**: As a user, I can sign in to the app so that I can access functionality for logged-in users.
4. **Sign Up**: As a user, I can create a new account so that I can access all the features for signed-up users.
5. **Logged-in Status**: As a user, I can tell if I am logged in or not so that I can log in if I need to.
6. **Refreshing Access Tokens**: As a user, I can maintain my logged-in status until I choose to log out so that my user experience is not compromised.
7. **Conditional Rendering**: As a logged-out user, I can see sign-in and sign-up options so that I can sign in/sign up.
8. **Avatar**: As a user, I can view user's avatars so that I can easily identify users of the application.

#### Adding and Liking Posts

1. **Create Posts**: As a logged-in user, I can create posts so that I can share my experience with the world.
2. **View a Post**: As a user, I can view the details of a single post so that I can learn more about it.
3. **Like a Post**: As a logged-in user, I like a post so that I can show my support for the posts that interest me.

#### Post Page

1. **Post Page**: As a user, I can view the post page so that I can read the comments about the post.
2. **Edit a post**: As a post owner, I can edit my post content so that I can make corrections or update my post after it was created.
3. **Delete a post**: As a post owner, I can delete my post so that I can remove my post after it was created.
4. **Create a comment**: As a logged in user, I can add comments to a post so that I can share my thoughts about the post.
5. **Comment date**: As a user, I can see how long ago a comment was made so that I know how old a comment is.
6. **View comments**: As a user, I can read comments on posts so that I can read what other users think about the posts.
7. **Delete comments**: As an owner of a comment, I can delete my comment so that I can control removal of my comment from the application.
8. **Edit a comment**: As an owner of a comment, I can edit my comment so that I can fix or update my existing comment.

#### The Posts Page

1. **View Most Recent Posts**: As a user, I can view all the most recent posts, ordered by the most recently created first so that I am up to date with the newest content.
2. **Search for Posts**: As a user, I can search for posts with keywords so that I can find the posts and user profiles I am most interested in.
3. **View Liked Posts**: As a logged-in user, I can view the posts I liked so that I can find the posts I enjoy the most.
4. **View Posts of Followed Users**: As a logged-in user, I can view content filtered by users I follow so that I can keep up to date with what they are posting about.
5. **Infinite Scroll**: As a user, I can keep scrolling through the images on the site, that are loaded for me automatically so that I don't have to click on "next page" etc.

## Wireframes

- A low-fi wireframe was built before developing the website.
- This was done in Balsamiq Wireframes.
- Most of the pages has same design so a basic wireframe was created for the following pages:
- Home page also used for feed and liked page
- Add/edit page also used for add posts, edit posts and edit profile

<details><summary>Home Page logged out</summary>
<img src="docs/wireframes/home-notloggedin.png" >

</details>

<details><summary>Home Page logged in</summary>
<img src="docs/wireframes/home-loggedin.png" >

</details>

<details><summary>Signin Page</summary>
<img src="docs/wireframes/signin.png" >

</details>

<details><summary>Signup Page</summary>
<img src="docs/wireframes/signup.png" >

</details>

<details><summary>Profile Page</summary>
<img src="docs/wireframes/home-profilepage.png" >

</details>

<details><summary>Profile Edit Page</summary>
<img src="docs/wireframes/edit-profile.png" >

</details>

<details><summary>Post detail Page</summary>
<img src="docs/wireframes/home-commentcreate.png" >

</details>

<details><summary>Add/edit form page</summary>
<img src="docs/wireframes/home-postcreate.png" >

</details>

<details><summary>Change username Page</summary>
<img src="docs/wireframes/change-username.png" >

</details>

<details><summary>Change password Page</summary>
<img src="docs/wireframes/change-password.png" >

</details>

## Technologies Used

### Languages

- HTML
- CSS
- Javascript
  - React (17.0.2)

### Libraries, frameworks and dependencies

- [Axios](https://axios-http.com/docs/intro) - axios were used for promise-based HTTP. Justification: I used axios to send API requests from the React project to the API and avoid any CORS errors when sending cookies.
- [ClassNames](https://www.npmjs.com/package/classnames/) - JavaScript utility for conditionally joining classNames together, used in the FeedbackMsg component. This is used to apply the styles dynamically based on the type of style and apply more than one style to elements in FeedbackMsg component
- [JWT](https://jwt.io/) - library to decode out JSON Web token. Justification: I used JWT to prevent unauthenticated user from making extra network requests to refresh their access token. Also used to remove the timestamp from the browser when the user refreshes token expires or the user logs out.
- [Popper](https://popper.js.org/) - a 3rd party library used by React-Bootstrap. Justification: I used Popper to make sure the dropdown menus position is fixed on all browsers.
- [React 17](https://17.reactjs.org/) - JavaScript library for building user interfaces
- [React-Bootstrap 4.6](https://react-bootstrap-v4.netlify.app/) - Justification: I used Bootstrap React library for UI components, styling and responsiveness.
- [React Infinite Scroll](https://www.npmjs.com/package/react-infinite-scroll-component) - Justification: I used this component to load content (posts/comments) automatically as the user scrolls towards the bottom of the page without having to jump to next/previous page.
- [React Router](https://v5.reactrouter.com/web/guides/quick-start) - used for dynamic routing. Justification: I used this library to enable the navigation among views of various components and control what the user sees depending on the URL they have accessed in the browser.
- [Prettier](https://prettier.io/): This extension was used to format code for all files

### Tools & Programs

- [Am I Responsive](http://ami.responsivedesign.is/) was used to create the multi-device mock-up at the top of this README.md file
- [Balsamiq](https://balsamiq.com/) to create the projects wireframes
- [Chrome dev tools](https://developers.google.com/web/tools/chrome-devtools/) was used for debugging of the code and checking site for responsiveness
- [Cloudinary](https://cloudinary.com/) to store static files
- [Coolors](https://coolors.co/?home) was used to create the color scheme palette
- [Favicon.io](https://favicon.io) for making the site favicon
- [Font Awesome](https://fontawesome.com/) - Icons from Font Awesome were used throughout the site
- [Google Fonts](https://fonts.google.com/) - import of font for the website
- [Gitpod](https://gitpod.io/) was IDE used for writing code and to push the code to GitHub
- [GitHub](https://github.com/) was used as a remote repository to store project code
- Validation:
  - [WC3 Validator](https://validator.w3.org/) was used to validate the html
  - [Jigsaw W3 Validator](https://jigsaw.w3.org/css-validator/) was used to validate the css
  - [Lighthouse](https://developers.google.com/web/tools/lighthouse/) used to validate performance, accessibility, best practice and SEO of the app

##### Back to [top](#table-of-contents)

## Agile design

### About

- Agile development is the most effective way to development of any website
- This was able to do basic development of website using user story template

### User Story Template

- Using Github issues first I created the template for a user story that was later used to create user stories. I created three labels: must have, could have, should have.

<details><summary>See User story template</summary>
<img src="docs/agile/issue-template.png">
</details>

### Kanban Board

- As a visual representation of the project's status, showing what tasks are to be done, in progress and completed.Each task is represented as a card on the board, and the cards can be moved from one column to another to show progress.

<details><summary>See Kanban board</summary>
<img src="docs/agile/kanban.png">
</details>

### Moscow Prioritisation

- The Moscow prioritization technique is used to prioritize project requirements based on their importance.

<details><summary>See Image</summary>
<img src="docs/agile/moscow.png">
</details>

### Milestones

- Milestones are created with a aim of finishing a task on a certain date. I have created 6 milestones for this project and linked them with issues related.

<details><summary>See Image</summary>
<img src="docs/agile/mileston.png">
</details>

## Design

### Colours

- I have tried to keep the color of the website simple, light and in matching with the logo.
- I tried to find the similar palette using [Coolors](https://coolors.co/?home)

<details><summary>See General Color Palette</summary>
<img src="docs/palette/general.png">
</details>
<details><summary>See Sign in/up Color Palette</summary>
<img src="docs/palette/signinup.png">
</details>

### Fonts

- Google fonts "DM Sans", sans-serif; font were used for this project as it offers clean and legible design, which makes it easy to read on screens of different sizes and resolutions. It has a neutral appearance and doesn't have any distracting features that can make it difficult to read.

<details><summary>See DM Sans</summary>
<img src="docs/palette/md-sans-font.png">
</details>

## Project Structure

### Front-End

#### React

React is a declarative, efficient, and flexible JavaScript library for building user interfaces. Its primary goal is to make it easy to reason about an interface and its state at any point in time, by dividing the UI into a collection of independent and reusable components ([source](https://www.freecodecamp.org/news/the-react-handbook-b71c27b0a795/)).

There were various components created and reused across this application.

- `<Asset />` - multi purpose component, used to display a range of items due to being passed props.

  - Those include a loading spinner from React Bootstrap, image with source and alt attribute or a message consisting of a paragraph.

- `<Avatar />` - reusable component, used to display the relevant user profile picture.

  - This component uses props which can specify the source of the image and also its size
  - This components was used in profile avatar, post owner, comment create form and comments posted

- `<DropDowns />` - reusable component, used to display the three dots option button based on the required rights of the user.

  - This was used for user who are authorised to make changes. For example, for user to edit and delete their own comments and user to edit their profile, change their username and password.

- `<EditStars />` - used to display editable stars while editing comments.

  - This component uses props which can get the stars value for further process.
  - This component was used in when user edit their ratings while editing comment successfully.

- `<BrandChoices />` - reusable component, used to display choices while creating a new post or editing an old post in the brand input field.

  - This component was used when user selects a year in production field in post create form commponent.

- `<ProductionYearChoices />` - reusable component, used to display choices while creating a new post or editing an old post in production input field.

  - This component was used when user selects a car brand name in brand field in post create form component.

- `<RatingsAverageStar />` - used to reperesent rating average by the stars in post component.

  - This component was used when a post is displayed.

- `<ShowStarsInCommentList />` - used to display the rate of each user by stars in comment list component.

  - This component was used when comment list is created.

- `<StarRating />` - used to able user to rate a post by selecting stars while commenting.

  - This component was used when user rates a post.

- `<NavBar />` - reusable component, used for easy navigation of the site.

  - This component is reusable as it will display different icons based on a users logged in status.
  - If no user is logged in a log in, sign up and contact icon will be available however if a user is currently logged in, the full range of icons will be available apart from log in.

- `<PageNotFound />` - specific component, used to display a 404 page made up of an image file and return home button for when the page does not exist.

There were various pages created and used in this application

- auth - The auth page group consisted of the following files:

  - SignInForm.js - This file handles the Login form
  - SignUpForm.js - This file handles the Sign up form

- comments - The comments page group consisted of the following files:

  - Comment.js - This file returns the comments
  - CommentEditForm.js - This file handles the comment edit form
  - CommentCreateForm.js - This file handles the create comment form

- posts - The posts page group consisted of the following files:

  - post.js - This file returns the post and all its related info
  - postCreateForm.js - This file handles the post create form
  - postEditForm.js - This file handles the post edit form
  - postPage.js - This file handles the post detail
  - postsPage.js - This file returns the list of posts

- profiles - The profiles page group consisted of the following files:

  - Profile.js - This file returns the profile section
  - ProfilePage.js - This file returns the entire Profile page
  - PopularProfiles.js - This file returns the users of the site as per the posts count they posted

  - ProfileEditForm.js - This file handles the profile edit form
  - UsernameForm.js - This file handles the username change form
  - UserPasswordForm.js - This file handles the password change form

### Back-End API

#### Django REST Framework

The API for this Front-End application was built with the Django REST Framework. The repository with a README file for the DRF Back-End can be found [here](https://github.com/strasse34/pp5-drf-api).

## Features

### Implemented Features

#### Navigation(Navbar)

- Navbar consists of Logo image and is displayed in all pages for easy navigation of website
- Navbar consists of name of website which is displayed in larger device
- Logo and website name both are links for home page
- Navbar consists of a links to a signin page and signup page for logged out users
- Authenticated/Signed in user can see additional icons as follows:
  - Add Review: It opens the post create form page
  - Feed: It shows the posts created of all users whom the logged in user has followed
  - Liked: It shows the posts user has liked
  - Logout: This is used for user to logout
  - Profile: This shows the user avatar and opens the user's profile page
- Feature is fully responsive and on smaller screen sizes it converts into a 'Hamburger menu'

<details><summary>See Nav-bar logged out</summary>

![Navbar logged out](docs/features/navbar-loggedout.png)

</details>

<details><summary>See Nav-bar logged in</summary>

![Navbar logged in](docs/features/navbar-loggedin.png)

</details>

#### Sign Up Page

- This page consists of sign up form for user to create new account
- New users can access this page by clicked on SignUp link on Navbar
- User Story covered: 2

<details><summary>See Sign Up Page</summary>

![Signup Page](docs/features/signup.png)

</details>

#### Sign In Page

- This page consists of sign in form for existing user to signin using their credentials
- Users can access this page by clicking on SignIn link on Navbar
- User Stories covered: 3

<details><summary>See Sign In Page</summary>

![Signin Page](docs/features/signin.png)

</details>

#### HomePage

- This page consists of four components as follows
  - Popular Profiles
  - Review Posts
  - Search form and filters

<details><summary>See HomePage logged out</summary>

![HomePage logged out](docs/features/home-loggedout.png)

</details>
<details><summary>See HomePage logged in</summary>

![HomePage logged in](docs/features/home-loggedin.png)

</details>

##### Popular Profiles

- This component is displayed on right side of the page in large screen and at the top in small screen
- This component uses filter to order all the site users by followers count
- Logged in users can follow and unfollow users from here as well
- User can click on these profiles avatar and see profile page of them

<details><summary>See Popular Profile logged in and out</summary>

![Popular Profile](docs/features/popular-profiles.png)

</details>

##### Posts Page

- All posts created by users are displayed here.
- This component has infinite scroll functionality for user to scroll to view posts created and do not have to click for going to next page
- The post created is in form of a card and displays following:
  - post owner avatar
  - Image of post
  - Car brand, model, other details, production year and post owner experience
  - likes, comments and rating average
  - Logged in user and not post owner can like a post

<details><summary>See posts page</summary>

![posts page](docs/features/posts-page.png)

</details>

#### Feed Page

- The feed page looks identical to the homepage, only the posts component changes.
- In this page all the posts displayed by filtering the posts created by the users logged in user is following
- It is the same as posts page but Feed icon is active

#### Liked Page

- The liked page looks identical to the homepage, only the posts component changes
- In this page all the posts that already liked by logged in user are displayed
- It is the same as posts page but Liked icon is active

##### Search-bar

- This component is provided for user to search all posts easily by their brand, model, other details and production year
- User can also type other user's name and see all posts posted by them

<details><summary>See Search form and filters Section</summary>

![Search form and filters](docs/features/searchbar.png)

</details>

#### post Detail Page

- This page consist a detail view of post created by users
- Users can click on post image in post card to open this page
- Logged in users can post comments on this page on posts and interact with other users
- post owner can edit and delete the post
- User can read full content about what the post is about

<details><summary>See Post Detail Page Logged out</summary>

![Post Detail Page- Loggedout](docs/features/postpage-loggedout.png)

</details>
<details><summary>See Post Detail Page Logged in with comment place</summary>

![Post Detail Page- Loggedin](docs/features/pastpage.png)

</details>

#### Post Create Page

- This page consists of post create form where user can create an post
- Logged in user can open this page by clicking on 'add review' link on Navbar

<details><summary>See post Create Page</summary>

![post Create Page](docs/features/addpost.png)

</details>

#### Post Edit Page

- This page consists of post form where post owner can edit the data of the post
- post owner can access this page by clicking on edit icon in post detail page
- After successful update user is displayed successful message

<details><summary>See post Edit Page</summary>

![post Edit Page](docs/features/post-edit.png)

</details>

#### Profile Page

- This page consists the detail of user including their bio, following and followers counts and posts posted by that user
- User can access other's profile by clicking on avatar of other users
- Logged in user can access this page by clicking on their avatar image in Navbar

<details><summary>See Profile Page Logged out</summary>

![Profile Page logged out](docs/features/profilepage-loggedout.png)

</details>

<details><summary>See Profile Page Logged in</summary>

![Profile Page logged in](docs/features/profilepage-loggedin.png)

</details>

#### Profile Edit Page

- This page consists of profile form where loggedin user can update their profile data
- Profile owner can access this page by clicking on edit profile in their profile page
- After successful update user is displayed successful message

<details><summary>See Profile Edit Page</summary>

![Profile Edit Page](docs/features/profile-edit.png)

</details>

#### Change Username Page

- This page consists of username change form where loggedin user can update their username
- Profile owner can access this page by clicking on change username in their profile page
- After successful update user is displayed successful message

<details><summary>See Change Username Page</summary>

![Change username Page](docs/features/profile-username.png)

</details>

#### Change Password Page

- This page consists of username change form where loggedin user can update their password
- Profile owner can access this page by clicking on change password in their profile page
- After successful update user is displayed successful message

<details><summary>See Change Password Page</summary>

![Change Password Page](docs/features/profile-password.png)

</details>

#### Page Not Found

- This page occurs when there is an 404 error
- This consists of an image and a button with a link to go back to home page
- After successful update user is displayed successful message
- User Stories covered: 31

<details><summary>PageNotFound Page</summary>

![PageNotFound Page](docs/features/page-not-found.png)

</details>

### Features to be Implemented

- Reply feature to the comment lists to provide chances to the users to reply a comment.
- Filter option feature to order posts/cars according their ratings.

## Validation

### CSS

- [Jigsaw W3 Validator](https://jigsaw.w3.org/css-validator/)was used to validate the css in the project.
- I got 2 errors after validation as url input and fixed them

<details><summary>See Errors</summary>
<img src="docs/validation/css.png">
</details>

<details><summary>Jigsaw validation using url</summary>
<img src="docs/validation/css-noerror.png">
</details>

### Html

- [WC3 Validator](https://validator.w3.org/) was used to validate the html in the project
- The deployed app was passed as url input for validation
- No errors were found
- Note : info were provided regarding standard Meta code

<details><summary>HTML validation screenshot</summary>
<img src="docs/validation/html-validation.png"  >
</details>

### Lighthouse

- [Lighthouse](https://developers.google.com/web/tools/lighthouse/) for performance, accessibility, progressive web apps, SEO analysis of the project code here are the results:

- While conducting lighthouse validation of profile edit page, commenting, username and password change page lighthouse was refreshing and testing the home page so I have not included the test results

- Note: Lighthouse results from testing the project may exhibit inconsistencies due to the functionality involving user-uploaded images. Hosting the project on Heroku could affect the results, impacting server response time, caching, and network latency. Additionally, the inclusion of additional external libraries may reduce the website's responsiveness. A significant number of cookies were received from Cloudinary, resulting in a lower rating in the 'Best Practices' criterion. Despite efforts, the persistent low rating in 'Performance' on mobile screens remains unresolved. Improvements will be pursued in future projects to enhance performance.

<details><summary>Home Desktop-screen</summary>
<img src="docs/validation/home-loggedout-desk.png" >

</details>
<details><summary>Home Mobile-screen</summary>
<img src="docs/validation/home-loggedout-mobile.png" >
</details>

<details><summary>SignIn page Desktop-screen</summary>
<img src="docs/validation/signin-desk.png" >
</details>

<details><summary>SignIn page Mobile-screen</summary>
<img src="docs/validation/signin-mobile.png" >
</details>

<details><summary>Sign up page Desktop-screen</summary>
<img src="docs/validation/signup-desk.png" >
</details>

<details><summary>Sign up page Mobile-screen</summary>
<img src="docs/validation/signup-mobile.png" >
</details>

<details><summary>Feed Desktop-screen</summary>
<img src="docs/validation/feed-desk.png" >
</details>

<details><summary>Feed Mobile-screen</summary>
<img src="docs/validation/feed-mobile.png" >
</details>

<details><summary>Liked Desktop-screen</summary>
<img src="docs/validation/liked-desk.png" >
</details>

<details><summary>Liked Mobile-screen</summary>
<img src="docs/validation/liked-mobile.png" >
</details>

<details><summary>Profile page Desktop-screen</summary>
<img src="docs/validation/profile-loggedout-desk.png" >
</details>

<details><summary>Profile page Mobile-screen</summary>
<img src="docs/validation/profile-loggedout-mobile.png" >
</details>

<details><summary>Post Detail Desktop-screen</summary>
<img src="docs/validation/postdetail-loggedout-desk.png" >
</details>

<details><summary>Post Detail Mobile-screen</summary>
<img src="docs/validation/postdetail-loggedout-mobile.png" >
</details>

<details><summary>Create Post Desktop-screen</summary>
<img src="docs/validation/create-post-desk.png" >
</details>

<details><summary>Create Post Mobile-screen</summary>
<img src="docs/validation/create-post-mobile.png" >
</details>

<details><summary>Edit Post Desktop-screen</summary>
<img src="docs/validation/edit-post-desk.png" >
</details>

<details><summary>Edit Post Mobile-screen</summary>
<img src="docs/validation/edit-post-mobile.png" >
</details>

## Testing

- Testing of the website can be [seen here](https://github.com/strasse34/pp5/blob/main/TESTING.md)

## Deployment

### Deploying the website in Heroko

- Before deploying in Heroku following files were created:
  1. env.py : stores confidential data eg. API keys, passwords etc.

2. Procfile : Very important for deployment and must be added with capital P

3. Requirements.txt: This must be updated for deployment in Heroku. It stores data of libraries used for project

- The website was deployed to Heroko using following steps:

#### Login or create an account at Heroku

- Make an account in Heroko and login

#### Creating an app

- Create new app in the top right of the screen and add an app name.
- Select region
- Then click "create app".

#### Open Deploy Tab

##### Choose deployment method

- Connect GITHUB
- Login if prompted

##### Connect to Github

- Choose repositories you want to connect
- Click "Connect"

##### Automatic and Manual deploy

- Choose a method to deploy
- After Deploy is clicked it will install various file

##### Deployment

- Project was deployed in Heroku

### Forking the GitHub Repository

1. Go to the GitHub repository
2. Click on Fork button in top right corner
3. You will then have a copy of the repository in your own GitHub account.
4. [GitHub Repository](https://github.com/strasse34/pp5)

### Cloning the repository in GitHub

1. Visit the GitHub page of the website's repository
2. Click the “Clone” button on top of the page
3. Click on “HTTPS”
4. Click on the copy button next to the link to copy it
5. Open your IDE
6. Type `git clone <copied URL>` into the terminal

## Credits

### Images

- The image for no results and upload were taken from Code Institute walkthrough project [Moments](https://github.com/Code-Institute-Solutions/moments)
- The car images for posts were taken from different free picture services like [Pinterest](https://www.pinterest.de/) and [Pixby](https://pixabay.com/)

### Code

- The code was written with the help of Code Institute walkthrough project [Moments](https://github.com/Code-Institute-Solutions/moments)

- For making rating stars I used different online free resources like [this](https://www.youtube.com/watch?v=J-gURMj3M6A) YouTube channel and [MUI](https://mui.com/material-ui/react-rating/) webpage.

## Thank You

- to Code Institute, tutur team and Slack community for helping me when I was getting stuck with some challenges.
- Special thanks to my wife and lovely daughter for their support during the past month in completing my PP5 project.
