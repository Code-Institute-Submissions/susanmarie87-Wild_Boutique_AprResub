# [*Wild Boutique*](https://wild-indigos.herokuapp.com/)


![Wild Indigos](media/screens.png)

Wild Boutique is a s holistically minded brand and community.
We promote whole body health and wellness. Our mindful approach to healthy and connected living drives our community bond and we want this website to represent the beauty of that.


[Live Site](https://wild-indigos.herokuapp.com/)

## Milestone Project 4

# UX <a name="ux"></a>

## Strategy <a name="strategy"></a>

* I created this site as a way for my daughter to sell her bracelets online and for myself to begin the process of building a like-minded community through wellness. This site will be tailored to suit all of our customer's needs.

* This project was built to showcase my abilites in designing and developing a full-stack web application predominantly using  Django, Javascript, Python, Bootstrap.

* The website I have built is a full stack E-commerce web application for a company that my daughter and I created called Wild Boutique. I built a basic front-end website for Wild Boutique for my MS1 but with my skills advancing, I decided to remake the website and add all of the commerce features.

* The application I have designed is an intuitive E-commerce store for company that sells organic tinctures, bathbombs, aromatherapy bracelets, and apparel. This website is equipped with Stripe. The user can add and delete products, and update the cart to their preference. The user can also contact the site as well.

* The Site Owner has properly working CRUD functionality. The owner can successfully create a new product. 


* For the assessor, the admin login details have been included in the comments section when submitting the project.

* Please note that this website is solely for educational purposes so Please don't attempt to enter real credit card details when using the stripe functionality. use the below details for testing purposes.

    * stripe card number: 4242 4242 4242 4242
    * Any card end date you wish
    * Anyy CVV number you wish


# Table of contents

1. [UX](#ux)

    * [strategy](#strategy)
        * [user stories](#user-stories)
        * [site goals](#site-goals)
    
    * [scope](#scope)
        * [features](#features)
    
    * [structure](#structure)

    * [skeleton](#skeleton)
        * [wireframes](/media/MS4-wireframes.zip)
        * [Database](#database)
    
    * [surface](#surface)

2. [Technologies Used](#technologies-used)

3. [Testing](#testing)

4. [Deployment](#deployment)

5. [Credits](#credits)

### User Stories <a name="user-stories"></a>

* I want to be able to quickly view the products that the site is selling.

* I want to be able to easily navigate throughout the site.

* I want to be able to find out more information about the company and see if they have a social media presence.

* I want to be able to contact the company.

* I would like to be able to search for a specific item using the search bar.

* I want to be able to search the site based on the different categories.

* I want to be able to see all product details before I choose to buy the item

* I want to be able to sort the items based on their price.

* I want to be able to add items to my shopping bag

* I would like to be notified when I add items to bag or interact with the site functionality.

* I want to be able to edit my shopping bag.

* I want the checkout process to be quick and painless.

* I want to be able to see previous order details.

* I want my details to be saved to my account for faster purchases in future.


### Site Goals <a name="site-goals"></a>

* I want to be able to add, edit and delete products, blog posts and the ability to delete comments from blog posts easily.

* I want to be able to increase organic visitors to the site using SEO friendly blog posts.

* I want an admin section of the site and to make administration tasks simpler.

* I want customers to have a relaxed and trouble free time on the site.

* I want the site to be fully mobile responsive.

## Scope <a name="scope"></a>

## Design

### Scope and Structure

**Scope**

* Responsive Design 
* Informative Landing Page
* Mobile Nav Bar 
* Relational database to store all uploaded data/content
* CRUD functionality at varying levels for profiles and products
* Authentication functionality
* Profile page
* Search functionality
* Contact functionality
* List functionality
* E-Commerce functionality

**Skeleton Structure**

This application will be made up of multiple pages derived or based around 5 data models, product, cart, checkout, user profile, and contact form.

The landing page will consist of a large hero image with a text introduction of the site's offering or purpose.

Login, registration, add/edit products/profile and contact pages will all consist of forms with varying inputs dependant on the purpose of the form.

The profile page will display user information derived from the form and past orders .

The products page will display all products and can be sorted or filtered.

The product detail page will display the image and details with an option to purchase, favorite or update/delete for the admin user.

**Interaction Design**

The nav bar items will highlight on hover.

All forms will show a success or error messages through webhooks.

Delete features will trigger warning modals and require confirmation before the action runs.

Successful actions and unsuccessful actions will be flagged with Django messages to the user.

Authentication processes, placed orders and contact form submission will trigger emails sent to the users email address provided.

### Wireframes
A mock-up of how the site will be laid out is available here:

- [Landing Desktop](/media/LandingDesktop.png).

- [Landing Tablet](/media/LandingTablet.png).

- [Landing DMobile](/media/LandingMobile.png).

- [Products Mobile](/media/ProductsMobile.png).

- [Products Tablet](/media/Products/Tablet).

### Database Structure

#### Data Models

###### Product & Categories

- The product model creates objects containing individual product information, such as name, description, price, image and sku. 
- The unique ID is auto generated. 
- The product objects will be used for the order model and favorites model.
- The product model is lonked to the categories model which divides the products into subsections.

##### User Profile & User

- The User model is created by django All Auth on registration, it stores the name, email and password of a user.
- The User Profile model creates and instance of the user information in the database, similar to above as an object. 
- The User Profile is linked to the User model. 
- The user Profile stores shipping and contact information.

##### Order Model & Order Line Item

- The order model is connected to the user profile, feeding in the shipping and contact information. 
- The order model creates an instance of an order on the data base with billing information, date and time of placement and by whom. 
- The order model is linked to the Order Line Item model which holds the product information for the order placed.
- The Order Line Item model is linked to products.

##### Contact
- The contact model stores users queries in the backend for the admin user to view.

### Security

Sensitive data such as SECRET_KEYS were stored on heroku using config variables to prevent unwanted connections to the database.

Django allauth was used to set up user authentication and built in decorators allowed restricted access to certain features on the website.

### Color Scheme

This new theme has been chosen because it feels like a breath of fresh air. The white navbar and other white elements across the site give the site such a light a bright feel. 

The dark text colors are brand colors that have been adopted for their strong visual contrast in an attempt to make all content as easily consumable and suitable for visually impared users as possible.
* There are two main colors used throughout the project and they are listed below.
    * #FFFFFF - this is the color used in the header and footer as well as border colors fonts etc.
    * #ebdee6-  A shade of white that is used in the buttons and contact form
    * #f090b8 - A gentle red that is used in conjunction with white as a linear gradient to bring about an eye popping design that blends nicely with the flowers on the hero image. This ties the site together with the beautiful flowers in the hero image.
    

### Typography

[Google Fonts](https://fonts.google.com/poppins) 

Poppins A combination of both soft and bold versions of Poppins will be used across the site. Soft Poppins will be the main font for all content across links and buttons and all descriptiive messaging. Strong Poppins will be used on the landing page for the Animated element section and also the card heading, This font was chosen because of it's playful vibe and also the hero image is strong and an equally strong font needed to be applied in order to avoid straining the eyes.   

[Google Fonts](https://fonts.google.com/BioRhyme + Expanded) 

BioRhyme + Expanded is being used on the card section headings to stand out from the rest of the page.


### Imagery

The Hero image reflects this brand perfectly. A beautiful woman standing in a sea of pink flowers that while are beautiful, are all the same, and the woman in the hero image has somehow found a gorgeous red flower that she is smelling under angelic light. This imagery reflects the message the brand is trying to send. In a world full of pretty and proper flowers, be a Wild Indigo.

Other images were just basic product images that seem to match the boho theme associated with the Wild Indigos brand. These photos were obtained through Unsplash and Pexels. 

## Features

### Existing Features

1. Responsive to different screen sizes.
2. Supported by Chrome, Opera, and Firefox browsers.
3. Adapted for users with special accessibility requirements where possible.
4. There will be multiple pages: 
Landing page. Products page. Product detail page. Shopping bag. Checkout Form Page. Successfull Check out page. Profile Page. login page, sign up page, product page, bag page, checkout form page, contact form page, 404 error and 500 error page.


5. The home page will have:

        - A hero image.
        _ Animated content.
        - Informative text.
        - Card section displaying products with links.
        - A contact section
        - A footer

6. The login/register page will have:

        - A form requesting user information (name, username & password) and a submission button.
        - Links to signup with your Google or Facebook accounts.
        - Toast messages letting you know if the attempt was successful or not.

8. The profile page will have: 

        - An area displaying the users information.
        - An area displaying orders the user has purchased.
        - There will be an option to edit information.
        - Toast messages displaying successfull/unsuccessful update of information.

9. The all products page will have:

        - Existing products.
        - Each product will have an image, label and a link to review its details.
        - To an admin user there will be a link to edit/delete.

10. The product detail page will have:

        - An image of the product
        - Descriptive text
        - Price
        - favorite icon
        - Quantity selector
        - Add to cart button
        - Go back button
        - Edit/Delete link for the admin user only
        - Toast messages displaying successfull/unsuccessful addition of products to the shopping bag

11. The shopping bag page will have:

        - Images and descriptions of products
        - Option to edit quantity or remove products
        - Grand total calculation
        - Keep shopping button
        - Continue to checkout button
        - Toast messages displaying successfull/unsuccessful removal of products

12. The check out page will have:

        - A form requesting/prepopulating order details
        - An order summary
        - A stripe payment option
        - A check box to save info to a profile
        - A grand total
        - Messages to convey successful or unsuccessful check out



13. The contact form page will have a form with fields for:

        - Name
        - Email
        - Drop down menu for the subject title
        - Text box
        - Submission button
        - Toast messages to convey successful or unsuccessful submission of the form.

14. All users interactions will either be confirmed or notified of an error either via on screen messages, orders, contact forms and profile set up will be also confirmed via email.

15. All products page and the cart page will have a scroll to top button.

## Information Architecture

### Data Storage

#### User Table

|   Title           | Key In Database                  | Form Validation   | Data Type  |
| ----------------- | -------------------------------- | ----------------- | ---------- |
| Account id        | _id                              | No Validation     | Primary Key|
| First Name        | first_name                       | max length 20     | CharField  |
| Last Name         | last_name                        | hashed min length | CharField  |
| Email             | email                            | Must have @ &.com | Email      |
| Street Address    | default_street_adress_1          | max length 120    | CharField  |
| Street Address  2 | default_street_adress_1          | max length 120    | CharField  |
| City or Town      | default_city_town                | max length 120    | CharField  |
| County/State      | default_county_state             | max length 72     | CharField  |
| Postal Code       | default_postcode_zip             | max length 120    | CharField  |
| Postal Code       | default_postcode_zip             | max length 120    | CharField  |
| Contact           |                                  |Number max         |            |
| Number            | default_phone_number             |length 20          | CharField  |
| Country           | country                          |pycountry select   | Option     |


### Products Table

|   Title           | Key In Database                  | Form Validation      | Data Type   |
| ----------------- | -------------------------------- | ----------------- | ----------  |
| Product Id        | _id                              | No Validation        | Primary Key |
| Product Name      | name                             | max length 254       | CharField   |
| Price             | price                            | max digits  6        | DecimalField|
| description       |description                       | No validation        | CharField   |
| sale_type         |sale_type                         | max length 20        | DecimalField|
| image             |image                             | Null True Blank True | ImageField  |



### Orders Table

|   Title           | Key In Database                  | Form Validation   | Data Type   |
| ----------------- | -------------------------------- | ----------------- | ----------  |
| Order Number      | order_number                     | No Validation     | Primary Key | 
| User Profile      | user_profile                     |     text          | Foreign Key |
| First Name        | first_name                       | max length 100    | CharField   |
| Last Name         | last_name                        | max length 100    | CharField   |      |
| email             | email                            | max length 120    | CharField   |
| Phone number      | phone_number                     | max length 20     | CharField   |
| Street Address  1 | default_street_adress_1          | max length 120    | CharField   |
| Street Address  2 | default_street_adress_1          | max length 120    | CharField   |
| City or Town      | default_city_town                | max length 120    | CharField   |
| County/State      | default_county_state             | max length 72     | CharField   |
| Postal Code       | default_postcode_zip             | max length 120    | CharField   |
| Country           | country                          |pycountry select   | Option      |
| Contact           |                                  |Number max         |             |
| Number            | default_telephone_number         |length 20          | CharField   |
| Order Date        | order_date                       |datetime.date.today| DateField   |
| Total Order       | total_order                      |max digits 10      | DecimalField|
| Delivery Charge   | delivery_charge                  |max digits 5       | DecimalField|
| Grand Total       | grand_total                      |max digits 10      | DecimaField |


## Technology Used

### Languages

- HTML
- CSS
- Javascript
- [Python](https://www.python.org/)

### Frameworks

- [Django](https://www.djangoproject.com/)
- [Bootstrap](https://getbootstrap.com/)

### Libraries

- [Jquery](https://jquery.com/)
- [Sweet Alert](https://sweetalert2.github.io/)
- [Stripe Payments](https://stripe.com/)
- [PopperJS](https://popper.js.org/)

### Tools

- [AWS](https://aws.amazon.com/s3/)
- [Heroku](https://www.heroku.com)
- [Git](https://git-scm.com/)
- [Postgres](https://www.postgresql.org/)

##  Resubmission Notes

Some of the problems noted in the project assessment results were as follows:

1. Very poor UX design.

- I agreed. The last project UX design was awful. I tried my best to turn the poor UX design around by completely changing the entire theme and overall site. The landing pages has been completely refreshed. A better hero image was applies. The navbar was made light to fit a light and bright theme. A three card section was added to feature our products and give the users a better idea right upon landing on the site, what our purpose is. Content with a good description was added to the hero image and given an animation effect. The "login" after being logged in messaging has been corrected. The desktop checkout form has been corrected. Jumbotrons were added across the site to break up the sections a bit and bold headers were added.

2. Confirmation pages that were bare with no return links.

- The confirmation pages have minimal but effective designs with a button link not to take the user back the home pages.

3. Login displayed after a user has already logged in.
- Easy fix by changing the text on the navbar link. I also added Jinja templating to add the user's name for a personal touch.

4. Oversize checkout form on desktop screens.
- This was solved by adding a row and column to the bootstrap portion to properly size the form across desktop screens.

5. Add product button for Site Owner CRUD funtionality is missing.
- I was able to implement the 'add' button onto the site for the shop owner making their experience much easier.

6. The edit crud functionality creates a new product instead of updating the current one.
- This was fixed by changing 

- This issue was solved by removing:
if form.is_valid():
            product = form.save()
and updating the html tags to properly reflect correct function. Fixing these two issues now allows a product to be updated properly.

7. Stripe confirmation emails.
- Currently working on resolving this issue which is proving to be a challenge. Stripe will not allow me to send automatic confirmation receipts with a TEST API key. I can manually send the emails from the Stripe dashboard, but they will not automatically send.



## Bugs

Bug 1
 
Problem: Trying to render a basic hello function. 
returns this error:

Page not found (404)
Request Method:	GET
Request URL:	http://localhost:8000/
Using the URLconf defined in wild_indigos.urls, Django tried these URL patterns, in this order:

admin/
hello/ [name='hello']
The empty path didn’t match any of these.

Cause: This error was being returned because I did not have function mapped to the home url
in my root urls.py.

Solution: Django needs to define the url with an empty string. Once I removed hello from the string, the test function
properly rendered to the page.
___________________________

Bug 2

Problem: On the first test run to check my index.html, an error kept returning:

'module' object is not callable.

Cause: It turns out that I had improperly imported os in the wrong file. 

Solution: By removing the improperly imported os placement I was able to open my project.
___________________________

Bug 3

Problem: When wiring up my item-detail folder into urls.py, I was met whith an invalid syntax error. 

Cause: This error occurred because when I created the path, I forgot to add the commas at the end of both paths which led to the invalid syntax error.

Solution: This was solved by of course adding a ), to the end of the path.
_________________________

Bug 3

Problem: When setting up the view for product details. I had 
Context = {
‘product’: products,
}

This returned a templating error and would not render the individual product once clicked.

Cause: Invalid Syntax. 

Solution: This issue was solved by changing ‘products’ to ‘product’
______________________________

Bug 6

Problem: When trying to implement the logic for adding the quantity times the price total, I receive a TypeError for an integer and a string 
Total +=

Cause: Wrong model field reference in the Product models.py file.

Solution: The bug was fixed by changing the price string to a DecimalField and running migrations. After the models were properly migrated the cart was able to render the prices of the items. 
________________________

Bug 7

Problem: Scott helped me with this one. I am using Bootstrap 5 and because of this, when I went to add the
Toasts to my project, it was not working. 

Cause: This was because Bootstrap 5 stopped using JQuery and are
instead using Vanilla JS. The initialization step is different.
In Bootstrap 4 the JavaScript Initialization is:
<script type=”text/javascript”>
      $(.toast).toast(‘show’);
</script>
In Bootstrap 5 it is quite different:

var toastElList = [].slice.call(document.querySelectorAll('.toast'))
var toastList = toastElList.map(function (toastEl) {
  return new bootstrap.Toast(toastEl, option)
})

Solution: Scott was able to make a loop that cycled through the toasts:
For (let x = 0; x < toastList.length;  x++) {
                               toastList[x].show();
               }
This solved the issue and my website started returning the Toast messages successfully.

**NOTE** I ended up switching back to Bootstrap4 due to design complications.
______________________________

Bug 9

Problem: When trying to add CRUD into the project for the store owner, I was met with a disturbing error during the test phase. I added the new item, saw that it was processed properly and headed to the Django admin to delete the product. When I did this, an error came back with:

Page not found (404)
Request Method: GET
Request URL: http://localhost:8000/
Raised by: home.views.index
Using the URLconf defined in wild_boutique.urls, Django tried these URL patterns, in this order:
admin/
accounts/
[name='home']
The empty path matched the last one.
You’re seeing this error because you have DEBUG = True in your Django settings file. Change that to False, and Django will display a standard 404 page.

Cause: There was an issue with the session cookie and this was solved by taking the following steps:

Solution: Open up Dev Tools, go to the Application tab, select Storage from the sidebar, then click the "Clear Site Data" button, it will fix the issue for you by emptying your cart.
_______________________

Bug 10

Problem: When clicking the secure checkout button an error occurred with crispy forms. 

Cause: This was due to a gitpod corruption. 

Solution: I had to run a command of:

curl https://raw.githubusercontent.com/Code-Institute-Org/gitpod-full-template/main/.gitpod.dockerfile > .gitpod.dockerfile

Then I had to copy and paste the original requirements.txt contents into https://lechien73.github.io/reqfix/ 

Next, I copied the code returned from https://lechien73.github.io/reqfix/, into my requirements.txt file.

Commit everything.

Go to Github, click the green button and create a new workspace.

Run the command of  pip3 install -r requirements.txt, to reinstall all the dependencies.

I created a new instance of my project a new env.py and reinstalled all dependencies to it. As I had manually loaded my categories and products fixtures files into the Django admin, I was left to completely redo the products section. 
_________________

Bug 11

Problem: Requirements.txt file was corrupted a second time.

Cause: Unsure of how the file was corrupted a second time.

Solution: Followed the same exact steps as the first time.
____________

Bug 12

Problem: I was unable to make migrations after the new install 

Cause: A corrupted value inside the migration file which was spotted by Kevin on tutor support.

Solution: Kevin gave it a valid value and I was able to run the migrations.

___________
Bug 13

Problem: The Aws crisis. Images not displaying on Heroku.
Cause: A backslash, /, generated in the AWS IAM secret convig variable. The backslash that is automatically generated in some AWS keys cause major issues in Heroku and this happened to me. Because of the slash in the key, it
Solution: Scott and James had a student who had previously had these problems. I generated a new user key and added them to the Heroku config vars and the images displayed on Heroku.
_____________
BUG 14

Problem: Details about products like price and CSS not picking up.
Cause: Somehow the product details were not picked up in AWS.
Solution: Correcting the CSS files in AWS.

_____________
BUG 15

Problem: Product detail CSS not picking up. Out of nowhere they have just disappeared and my brain is shutting down. It cannot process anything else before the deadline what-so-ever.
Cause: The issue was that somehow someway, my details disappeared from AWS S3 Bucket.
Solution: This problem ws solved by manually adding the productndetails into S3 static folder's CSS file in the bucket. The details rendered across the deployed Heroku version after this.

## User Story Testing

- USER STORY: "I want to be able to quickly view the products sold on the site." In order to meet this user story, a button was placed directly on the landing page for an obvious link to the products. There is also a product link located on the navbar.

- TEST: The button style was adapted from Boutique Ado and so of course it functions perfectly and breaks down perfectly across all screen sizes across all browsers.

- Result: There is now a button on the landing page.

- Verdict: The button being the first thing a user notices immediately entices them to click the link and get to shopping right away.
_________________

- USER STORY: "I want to be able to easily navigate throughout the site."
- Test: Is less really more?
- Result: In keeping the site minimal without a lot of bells and whistles, users will easily be able to navigate the site.
- Verdict: The navigation helps users easily navigate the site.
________________

- USER STORY: "I would like to be able to search for a specific item using the search bar." "I want to be able to search the site based on the different categories."
- Test: A searchbar was added into the products section. 
- Result: This searchbar works across all browsers but the words have to be specific.
- Verdict: The searchbar function is a nice addition and provides a good user experience. User stories satisfied. 
_____________

- USER STORY: "I want to be able to see all product details before I choose to buy the item"
- Test: Product details were added in so the user could see better details before purchasing.
- Result: Originally, there were product details.  During the AWS crisis of my project my product details were there. The product details have now vanished into thin code air and I have no clue what has happened to them nor the time or brain power left to even attempt figuring that out before the deadline.
- Verdict: Products without details are worthless and will absolutely drive users away. Very poor user experience and mucy be addressed immediately. User stories were satisfied but not now when it counts.
___________________

- USER STORY: "I want to be able to add items to my shopping bag."
"I would like to be notified when I add items to bag or interact with the site functionality."
"I want to be able to edit my shopping bag."
- TEST: The add and edit bag functions in the bag app along with Bootstrap toast messages were implemented to satisfy these user stories.
- RESULT: The users can add and edit their bag flawlessly across all browsers. These features work properly and add a nice UX feature to the site
- VERDICT: The user stories were satisfied.
____________________

- USER STORY: "I want the checkout process to be quick and painless."
- TEST: Stripe was implemented into the project.
- RESULT: Stripe is only in test phase for this proejct but the it work perfectly throughout all browsers.
- VERDICT: The stripe addition satisfies this user story.
_____________________

 USER STORY: "I want to be able to see previous order details." "I want my details to be saved to my account for faster purchases in future."
- TEST: Create a profile to obtain and save order history and personal information. 
- RESULT: As far as my testing went, the order details and customer information was saved.
- VERDICT: These user stories were satisfied.
______________________

 USER STORY: "I want to be able to see previous order details." "I want my details to be saved to my account for faster purchases in future."
- TEST: Create a profile to obtain and save order history and personal information. 
- RESULT: As far as my testing went, the order details and customer information was saved.
- VERDICT: These user stories were satisfied.
______________________

## Special Note

On my computer, when going through tests, it seems as though the inspect tool has a lag time and must  be refreshed. Otherwise the site design gets completely skewed. This is likely just my computer but I wanted to note it just in case.

## HTML VALIDATION

The code has been passed through  [W3 Validator](https://validator.w3.org/). When the files are passed through individually, the code comes back with a multitude of errors. 
When the code is passed through by URI which is what I was instructed to do via tutor support, the code only has one warning which is:
Warning: The type attribute is unnecessary for JavaScript resources.

I finally learned about the HTML validator extension. After adding this extension I was able to run all HTML files easily through the validators. There are minor warnings but no errors.

## CSS VALIDATION

 Aside from a few invalid value and parse errors, the CSS passes validation.

## FUTURE IMPLEMENTATION

A blog section for customers to use to create SEO friendly blog posts, in hopes to increase organic traffic to the site. 

A comments section for users to add comments for interactivity with the store and leave comments on blog posts.

## Remaining Design Issues

 The desktop version of the navbar is awful but I could not figure out what was blocking me from being able to get the account and cart to sit on the right side. The mobile and nav version look akay.

 **Navbar update**- The problem with the navbar was that I had left a nav element in the base. When I tried to remove it, the navbar would disappear. This issue was FINALLY solved by adding the bg-dark class to the main-nav.html file and my navbar looks better now.

 The button on the products search bar broke on me a few days back and I have not been able to figure out what I did to break that.

## Remaining Flake8 errors

- Several errors in the Checkout app view.py file in regards to profiles and objects that I was unable to solve. All relating to the products having no objects or not existing even though it seems like they exist because they work. An attempt was made to remedy these errors but were ultimately left ignored.

- Warnings in signal.py contact file but when arguments are removed the website breaks


## HTML Validation Errors

The site has been thoroughly checked for validation errors and it has passed every page. There are minor warning in relation to google fonts.

## Deployment

Below is an example of how to deploy this site locally based on using *Gitpod IDE*, deploying to Heroku using *Amazon S3* for hosting of static and media files. This will allow the site to deploy automatically with commits to the master branch. The code can also be run locally.

### Deployment Requirements

- [Gitpod](https://www.gitpod.com/) IDE Local development tool
- [python](https://www.python.org/downloads/) Documentation is based on Python v3.8
- PIP package installer
- [Stripe](https://stripe.com/gb) Payment infrastructure

### Deploying Locally

1. Clone a copy of the repository by clicking code at the top of the page and selecting 'Download Zip' when this has downloaded, extract the files to your folder of choice.
   Alternatively if you have git installed on your client you can run the following command from the terminal.

 ```bash
   git clone https://github.com/susanmarie87/wild-boutique.git
   ```

   1. Open us your local IDE (For this example we will be using Gitpod as linked in the requirements) and open the working folder.

1. Ideally you will want to work within a virtual environment to allow all packages to be kept within the project, this can be installed using the following command (please note some IDE's require pip3 instead of pip, please check with the documentation for your chosen IDE)

```bash
pip3 install pipenv
```

1. In your root dir, create a new folder called .venv (ensure you have the .)

1. To activate the virtual environment navigate to the below dir and run activate.bat

```bash
[folderinstalled]\scripts\activate\activate.bat
```

If you're using Linux or Mac use the below command 

```bash
source .venv/bin/activate
```

1. Next we need to install all modules required by the project to run, use the follow

```bash
pip3 install -r requirements.txt
```

1. Create a new folder within the root dir called env.py. Within this file add the following lines to set up the environmental variables.

```bash
import os

os.environ["SECRET_KEY"] = "[Your Secret Key]"
os.environ["DEV"] = "1"
os.environ["HOSTNAME"] = "0.0.0.0"
os.environ["STRIPE_PUBLIC_KEY"] = "[Your Stripe Key]"
os.environ["STRIPE_SECRET_KEY"] = "[Your Stripe Secret Key]"
os.environ["DATABASE_URL"] = "[Your DB URL]"
```

### Database setup

1. To set up your database you will first need to run the following command

```bash
python3 manage.py migrate
```

1. To create a super user to allow you to access the admin panel run the following command in your terminal and complete the required information as prompted

```bash
python3 manage.py createsuperuser
```

1. From there you should now be able to run the server using the following command

```bash
python3 manage.py runserver
```

1. If everything has been correctly configure you should not get a message giving you a link to your locally hosted site usually at http://127.0.0.1:8000

1. Next close the server in your terminal using ctrl+c (cmd+c on mac) and run the following commands to populate the database

```bash
python3 manage.py loaddata store/fixtures/categories.json
python3 manage.py loaddata store/fixtures/products.json
python3 manage.py loaddata clients/fixtures/clients.json
```

### Deploying to Heroku

To run this application in an online environment you will need to deploy the code to *Heroku*.
Before moving on to this section please ensure you have followed the instructions for local deployment and this has been successful

1. Either create an account at [Heroku](https://www.heroku.com/) or log in to your account
1. Set up a new app under a unique name
1. In the resources section, in the addons field type the below command and select the free cost option

```bash
heroku Postgres
```

1. in the settings tab select Reveal Config Vars and copy the pre populated DATABASE_URL into your settings.py file in your project
1. in the Config Vars in Heroku you will need to populate with the following keys

|          Key          |     Value    |
|:---------------------:|:------------:|
| AWS_ACCESS_KEY_ID     | [your value] |
| AWS_SECRET_ACCESS_KEY | [your value] |
| SECRET_KEY            | [your value] |
| STRIPE_PUBLIC_KEY     | [your value] |
| STRIPE_SECRET_KEY     | [your value] |
| USE_AWS               | TRUE         |
| DATABASE_URL          | [Your Value] |

1. Now this has been configured you will now migrate the local database to the cloud database using the migrate command as below

```bash
python3 manage.py migrate
```

2. Next you will need to create a super user and populate the database as described in the database set up section
3. When the migrations and data has been loaded, in your *Heroku* dashboard select the Deploy tab
4. From here select the Github option and connect the repository from GitHub and select the branch (Master) to deploy from.
5. It is advised to select automatic deployment to ensure for each push to Github the hosted version is up to date.
6. When this has deployed select open app from the top bar of the *Heroku* App.

<a></a>

# Inspiration For this Site

<a></a>

The inspiration for this project and much of the code functions and styling came from Code Institute and their project.

[Boutique Ado](https://github.com/Code-Institute-Solutions/boutique_ado_v1)

[Landing Template Design](https://www.developerdrive.com/responsive-landing-page-bootstrap-4/)


### MEDIA


[Make today amazing](https://unsplash.com/photos/DXmhzif5izc?utm_source=unsplash&utm_medium=referral&utm_content=creditShareLink)


[3 bracelets image](https://unsplash.com/photos/md87xXz3le4?utm_source=unsplash&utm_medium=referral&utm_content=creditShareLink)


[Pain tincture](https://unsplash.com/photos/D6SQVDF7x_E?utm_source=unsplash&utm_medium=referral&utm_content=creditShareLink])

[Tincture Guy](https://unsplash.com/photos/D6SQVDF7x_E?utm_source=unsplash&utm_medium=referral&utm_content=creditShareLink)

[Contact section textured background](https://unsplash.com/@thomas2006)

[Landing page bracelet image Brooke Cagle](https://unsplash.com/photos/kElEigko7PU)

[Sweatshirt photo by Rangga Aditya Armien]( https://www.pexels.com/photo/more-faith-less-fear-white-sweater-189199/)

[Howlite](https://unsplash.com/photos/Gwhtv-14miU?utm_source=unsplash&utm_medium=referral&utm_content=creditShareLink)

[Pain Tincture](https://unsplash.com/photos/D6SQVDF7x_E)

[Good Vibes tincture](https://unsplash.com/photos/LAOVX-PFNvI)

[Supplement Landing Image Emma-Jane Hobden](https://unsplash.com/photos/UNs7kXHGIe0)

[Hero Image Erriko Boccia](https://unsplash.com/photos/TWB035qnbQs)

[Super Good vibes](https://unsplash.com/photos/k2DvXqBl_rQ?utm_source=unsplash&utm_medium=referral&utm_content=creditShareLink)

[Bathbomb Trio](https://unsplash.com/photos/yVAXSK6zFIM)

[Glowing text](https://www.w3docs.com/snippets/css/how-to-create-a-glowing-text.html)



## Acknowledgements

The <strong>[TUTORS](https://learn.codeinstitute.net/ci_support/diplomainsoftwaredevelopment/tutor)</strong>

All of them:

1. [@Scott_CI -U4NJFT2M6](https://code-institute-room.slack.com/)
2. [@sheryl_ci - U01PFKGS623](https://code-institute-room.slack.com/)
3. [@james_ci - U02HZ4NTSHG](https://code-institute-room.slack.com/)
4. [@sean_ci - U023BDTRM9C](https://code-institute-room.slack.com/)
5. [@ed_ci - Ed Bradley](https://code-institute-room.slack.com/)
6. [@john traas_ci - John Traas](https://code-institute-room.slack.com/)
7. [@rebecca_ci - U02NKD296N5](https://code-institute-room.slack.com/)
8. [@michael_ci - Michael Park](https://code-institute-room.slack.com/)
9. [@ger_ci-U030LJXSLQH](https://code-institute-room.slack.com/)

 The tutor support was invaluable for me. As someone who literally hadn't been on a computer since 2008 and has absolutely zero tech skills, I would have never been able to figure out the AWS key was breaking my images when deployed to Heroku. I would have never known that my requirements.txt file had been corrupted. The tutors practically dragged me through this course. They all had impeccable patience and manners. I know I would have wanted to get snarky with me after some of the things I have put them through. I am not a fan of social platforms and especially when I have never felt so just dumb in my life. The thought of putting that on full display for strangers to see was mortifying to me. For others, Slack is invaluable, but for me, it was terrifying. I am beyond thankful I had this resource and though it may not seem like it, I learned so much from my sessions. A note would probably be to increase the tutor support option and really promote it as that sets Code Institute apart from the rest.

<a></a>
The Mentors
[Simaen Daelin-U4MVA9YQP](https://code-institute-room.slack.com/)

<strong>[Code Institute](https://codeinstitute.net//)</strong>
