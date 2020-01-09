# Ecommerce App
A basic online marketplace. Make sure you go through UX suggestions below before starting.

## Task
You have to write a web app on which vendors can register themselves and add items they want to sell, and users can add money
and order these items (the users have to register too!).

There are multiple phases to this project.


### Phase 1: Basic functionality
1. Implement authentication. Use Django's [in-built authentication system](https://docs.djangoproject.com/en/3.0/topics/auth/).
It's handy and easy to use. You must keep in mind that there are two kinds of users on your web app - the vendors and the customers.
They are different because they are allowed to do different things. For example, a vendor is not allowed to order items, while a 
customer is not allowed to sell items. Your application should have one page on which vendors can register, and one on which users
can register.
2. Create a well defined database structure and implement it in the models. When writing the models, keep the following in mind - 
    * A customer can order from only one vendor at a time.
    * A customer can order only one item (but he can order multiple number of units of it) at a time. For example, if a vendor
    is selling footballs and basketballs, I can order 3 footballs *or* 2 basketballs, but not 3 footballs *and* 2 basketballs.
    * A vendor can add multiple items that he wants to sell, and he has to specify how many units of those items he 
    has available.
    * An item must have an image, a title, a price and a description.
3. Allow vendors to add or delete items to sell.
4. Allow customers to add money (don't implement a payment gateway, just add whatever amount they want directly)
6. Allow customers to view orders that they have made previously.
6. Allow vendors to view all orders that were placed for items that they're selling.
7. Implement a '**home page**' where all items are listed. Items that have the highest sales should appear first.
8. Create a page for each vendor where his items are listed, sort of like 'vendor profile'.
9. Make sure that a customer cannot place an order if there isn't sufficient money in his account or if the item is out of
stock. Perform more checks if needed. Show appropriate error messages.
10. Allow customers to change their address information.


### Phase 2: More features
1. Add Oauth - allow users to sign up with google. You can do this easily with a library called [Django Allauth](https://wsvincent.com/django-allauth-tutorial/).
But for more experienced developers, I recommend you use [google's API client library](https://www.datadependence.com/2016/03/google-python-library-oauth2/)
as things are a bit more flexible that way.
2. Notify the vendor with an email whenever someone buys from him. You can do this with [Sendgrid](https://sendgrid.com).
Sign up for sendgrid and get your API key. [This code sample](https://sendgrid.com/docs/for-developers/sending-email/v3-python-code-example/)
might give you an idea of how to do it.
3. You've been using the weak SQLite database which is not fit for production. Time for an upgrade. Change your project
settings to use MySQL for the database. [This tutorial](https://www.digitalocean.com/community/tutorials/how-to-create-a-django-app-and-connect-it-to-a-database#step-3-%E2%80%94-install-mysql-database-connector)
might help.
4. Allow the vendor to generate a CSV/Excel report of all his sales till now.
5. Remember how the customer could order only one type of an item at a time? Not anymore. Allow the customer to order multiple
types of items at a time. So if a vendor is selling basketballs and footballs, I should be able to order two basketballs 
and three footballs at the same time. This might need some refactoring of your models, and you'll need to implement a 
*shopping cart* model for this.
5. Allow customers to add items to their wishlists.
6. Remember the *previous orders* list? If the user clicks on an order in this list he should be redirected to a new page where
all details of this order are shown (for example, the time when the order was placed).


### Phase 3: Deploy!
Your code is of no use unless it makes it to a production server!
1. Sign up on DigitalOcean using [this referral link](https://m.do.co/c/258499a2d433) to get $100 credit for two months. (Do 
not use your BITS ID for signing up).
2. Create a droplet (a droplet is just a fancy word for a virtual private server by DigitalOcean). You can ssh into this server.
3. Deploy your django application on the internet using nginx, gunicorn and supervisor. [This tutorial](https://rakibul.net/django-gunicorn-supervisor-nginx)
might really help.
4. You're live! Go to the IP address of your droplet to see your application live on the internet!

---

### Additional features -
You can implement some more features to really polish your web app and give it more functionality. The assignment is
considered complete even if you don't implement the following. 
* Allow customers to directly move an item from wishlist to cart.
* Allow vendors to change prices and other details of items.
* Allow vendors to show discounts on items.
* Allow customers to order **multiple items** from **multiple vendors** at a time, just like you can order different things
from different sellers at the same time on Amazon.


### UX suggestions -
If you want, you can make your app your way. But if you want to save yourself the time it'll take to come up with a proper
'design' for your app, you can do it this way - 
* Have a vendor dashboard. When the vendor logs in, he should be redirected to this dashboard. On his dashboard should be all
the vendor related functionality. For example, there could be a link which redirects him to a page that shows him all the orders
he has recieved.
* On the vendor dashboard, add a link to a page on which the vendor can see all the items he is selling. He should be able
to add and delete items from this page. If you implemented the *edit item details* (additional) feature, clicking on an item 
should redirect to a form to edit the item's details.
* When the customer logs in, directly redirect him to the home page. On the home page, add links to pages that show the customer
his previous orders, his wishlist, his shopping cart, etc.


### Time alloted -
  - Phase 1 - 5 days
  - Phase 2 - 4 days
  - Phase 3 - 1 days
  

### Submission Rules
***Securely*** share the source code on GitHub under your own account.  

What Securely means:
  1. Don't share the Django secret key.
  2. Don't share any test databases.
  3. Don't share any database passwords/names or anything of the kind.
  4. Don't share any API keys.
  5. **Do** use common sense.

Basically, don't share any data that must be kept secret.  
**Hint**: Make a python file where you store all of these values as variables (sort of like C/C++ macros in a header file), then add this file to your gitignore. Generally, we prefer to call that file the keyconfig.
