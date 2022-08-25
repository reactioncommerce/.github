<h1 align="center">
  Mailchimp Open Commerce (formerly Reaction Commerce)
</h1>
<h4 align="center">
  <a href="https://mailchimp.com/developer/open-commerce/">Open Commerce Website</a> |
  <a href="https://mailchimp.com/developer/open-commerce/">Documentation</a> |
  <a href="https://discord.gg/Bwm63tBcQY">Discord</a>
</h4>


<h2>An open source, API-first, modular commerce stack made for technical, growth-minded retailers.</h2>


<table>
<tr>
<td><strong>Flexibility at scale</strong><br><br>
Use our essential commerce capabilities alongside or instead of your existing tech stack.
</td>

<td>
<strong>Build your ideal platform</strong><br><br>Implement only the services that fit your business and the future 
you’re building.
</td>

<td>
    <strong>Suit your needs without limits</strong><br><br>
    Customize any part of the platform with new technologies, channels, or business models—at your own pace.
</td>
</tr>
</table>


# Features

<table>
<tr><td><strong>Fast</strong></td><td>Returns data in split seconds, and faster queries mean faster web pages</td></tr>
<tr><td><strong>Proven</strong></td><td>Open Commerce fuels sites doing 10's of thousands of orders per day with 100's of thousands of products</td></tr>
<tr><td><strong>Composable</strong></td><td>A flexible plugin system allows you to pick and choose which integrations work best for you</td></tr>
<tr><td><strong>Multi-tenant</strong></td><td>Host multiple shops in the same installation</td></tr>
<tr><td><strong>Scalable</strong></td><td>Start out with a single server and scale up to hundreds</td></tr>
<tr><td><strong>Flexible Products</strong></td><td>Allows Products, with options and variants to fit a wide variety of needs</td></tr>
<tr><td><strong>Inventory</strong></td><td>Track inventory, allow or disallow backorders and more</td></tr>
<tr><td><strong>Shipping</strong></td><td>Integrate with a shipping rate provider or build your own custom table</td></tr>
<tr><td><strong>Taxes</strong></td><td>Integrate with a tax rate provider or build your own custom tax table</td></tr>
<tr><td><strong>Fulfillment</strong></td><td>Flexible fulfillment system allows you create your own fulfillment methods</td></tr>
<tr><td><strong>Order Tracking</strong></td><td>View and manage your orders in the included admin system</td></tr>
<tr><td><strong>Emails</strong></td><td>Customizable templates for Order confirmations and more</td></tr>
<tr><td><strong>Open</strong></td><td>Fully open source. Never be locked in again</td></tr>
</table>


# Getting started
## What you’ll need


- We recommend installing [nvm](https://github.com/nvm-sh/nvm)
- [14.18.1 ≤ Node version < 16](https://nodejs.org/ja/blog/release/v14.18.1/)
- [Git](https://git-scm.com/)
- [Yarn](https://yarnpkg.com/cli/install) (for the storefront)
- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

- Windows users: [WSL 2](https://docs.microsoft.com/en-us/windows/wsl/install-win10) and [Docker for WSL](https://docs.docker.com/docker-for-windows/wsl/)

In addition you need to have your system setup for [SSH authentication with GitHub](`https://docs.github.com/en/authentication/connecting-to-github-with-ssh`)

## Install the CLI

`npm install -g reaction-cli`

## Install the API Server

- Create a directory for your entire project using `mkdir myproject` and then `cd` into it
- Create an API server by running `reaction create-project api <myapiserver>`, _you can substitute any directory
  name for `<myapiserver>`_
- Change directory into your newly created server directory and run `npm install`
- Once this is complete run `reaction develop`. This will start the Open Commerce server in development mode.
- Congrats you have installed the Mailchimp Open Commerce API server. You can now proceed to install the Storefront
  and Admin applications. You can view the GraphQL playground locally `http://localhost:3000/graphql`

## Install the Storefront

- Open a new terminal window
- Change to the root of the project directory you created above
- Execute `reaction create-project storefront <mystorefront>` (like above you can name this directory whatever you like)
- Change directory into the newly created storefront by doing `cd <mystorefront>` (using whatever name you have it
  above)
- Now run `yarn install` to install the dependencies
- Then run `reaction develoop` to start the storefront in development mode
- Congratulations, you have installed the default storefront for Mailchimp Open Commerce. You can access the
  storefront from http://localhost:4000

## Install the Reaction Admin
- Open a new terminal window
- Change to the root of the project directory you created above
- Execute `reaction create-project admin <myadmin>` (like above you can name this directory whatever you like)
- Change into your newly created directory by doing `cd <myadmin>`
- Now run `npm install`
- Then run `reaction develop` which will start the Admin in development mode (Note: The admin can take a little
  while to start up the first time because it's in Meteor)
- Once the server has started you can access it by going to `http://localhost:4080`

## Access the dashboard, playground, and storefront

Now that you have the entire Mailchimp Open Commerce project running locally, you can create a shop manager account for your local instance.

First, visit the Admin interface at `localhost:4080`. On the top right, click the user profile image. Click **Create Account** and enter your email address and create a password, which will grant you admin privileges.

Enter a name for your shop and click the **Create Shop** button. You should now see the Open Commerce admin dashboard, from which you can [create products](/developer/open-commerce/docs/creating-organizing-products/), [add tags](/developer/open-commerce/docs/tags-navigation/), and [manage your orders](/developer/open-commerce/docs/fulfilling-orders/).

Once you've created a shop, you can visit the GraphQL playground at `localhost:3000/graphql`, where you can run test GraphQL queries and mutations. In the **Docs** tab of the playground, you can view the complete Open Commerce GraphQL API reference.

You can also view your Open Commerce storefront at `localhost:4000`.

## Next steps

Now that you’re up and running, you can start managing your store by creating products or building a custom storefront on top of the GraphQL API. The local instance also provides everything you need to code your own plugins for use with Open Commerce; for more information, see the [Build an API Plugin](/developer/open-commerce/guides/build-api-plugin/) guide.

Once you are done working with any of the servers you can stop then by either pressing Ctrl+C or by simply closing
the terminal window.



### License

Reaction is [GNU GPLv3 Licensed](./LICENSE.md)
