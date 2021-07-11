When it comes to the world of digital currencies, one of the challenges new users face is *transparency* and *ease-of-use*. Modern Blockchain technologies afford censorless, high-volume transactions but leveraging these powerful solutions requires technical expertise and detailed understanding.

**[Block Trac](https://blocktr.ac)**, the newest product from Dev Null Productions, allows you to easily derive value from the Blockchain, such that the activity you are interested in is delivered straight to your inbox!

![blocktrac landing page](@/assets/posts/blocktrac-tutorial/landing-page.png)

With Block Trac you have the ability to see transactions conducted on many Blockchain real-time. Automatically dive into the details of each and every transaction, and setup filters so that you receive notifications of exactly what you want and no more.

Notifications can be sent to your inbox, smart device, or API, facilitating plug-and-play integrations into any automated system. By using a comprehensive and strong *pattern matching system*, Block Trac allows the inclusion (and/or exclusion) of specific transactions of interest.

## Live Transactions

After arriving at the informational landing page click, **Begin today** to launch the main application. From there you will see live transactions propagating through the network in real time.

![live xrp transactions](@/assets/posts/blocktrac-tutorial/live-xrp-txs.png)

With Blockchains like XRP and XLM, where blocks close every few seconds, you will see a torrent of transactions representing all sorts of activity... thankfully we have Block Trac to access that in which we are interested!

For older technologies such as BTC and ETH, transactions transpire when blocks are closed, which may take up to 30 minutes, so updates the live transaction stream will be more infrequent.

Use the control in the upper left to change the Blockchain being monitored:

![select blockchain](@/assets/posts/blocktrac-tutorial/select-blockchain.png)

To create a new filter click "Create Personalized Filter":

![create new filter](@/assets/posts/blocktrac-tutorial/create-filter.png)

## Creating New Filters

There are two available options when it comes to adding a filter, "By Category" and "By Expression". We will explore both below. 

### By Category

Category based filters allow you to easily setup alerts based on pre-defined categories of activities. Many categories are available for you to use, from there simply set the parameters relevant to that category and you are good to go.

Depending on the blockchain, categories include:

- Transactions originating *from* a specific account
- Transactions being sent *to* a specific account
- Minimum fee that is paid
- Miner payout
- DeFI currency pair offer created
- and much more!

![create-xrp-filter](@/assets/posts/blocktrac-tutorial/create-xrp-filter.png)

Let's say we want to see XRP transactions which pay abnormally high fees. The typical fee is 20 Drops (millionths of an XRP), so will will setup an alert for 30+ drops.

- Select 'XRP' blockchain
- Select 'Minimum Fee'
- Set the fee to '30' drops
- Set the filter name
- Click 'Ok'

You will then be prompted to login or register. See below for instructions on that process.

### By expression

Block Trac implements a powerful pattern matching system, called expressions, which allow you to perform a **deep inspection** on every since blockchain transaction, executing the expression against each. The expression returns true, indicates the filter matches, and a notification should be sent.

![create-expression-filter](@/assets/posts/blocktrac-tutorial/create-expression-filter.png)

To create a new expression based filter.

- Click 'By expression'
- Select the Blockchain to monitor
- Enter the expression to use as the basis of the filter (see below)
- Set the filter name
- Click 'OK'

Again you will be prompted to login or register (see below).

## JSONPath Expressions

Blockchain transactions are transmitted in JSON, a structured data format is used to represent the transaction details as they propagate the network. Block Trac implements a JSON-querying specification, dubbed JSONPath, that lets you hone in on the exact content of the JSON transactions you want to match.

To analyze just XRP transactions that create offers, for example, use the following expression:

<pre>$..[?(@.TransactionType == 'OfferCreate')]</pre>

To specify Payments which transfer more than 500 XRP (500 million drops), you can use: 

<pre>$..[?(@.TransactionType == 'Payment' && parseInt(@.Amount) > 500000000)]</pre>

Or to only inspect transactions that create new accounts:

<pre>$.meta.AffectedNodes[?(@.CreatedNode.LedgerEntryType == 'AccountRoot')]</pre>

To read more on these expressions click on the <img src="@/assets/posts/blocktrac-tutorial/question.svg" style="display: inline"/> icon above the transactions stream:

![jsonpath-help1](@/assets/posts/blocktrac-tutorial/jsonpath-help1.png)

Click on *JSONPath tutorial* for even more help.

![jsonpath-help2](@/assets/posts/blocktrac-tutorial/jsonpath-help2.png)

## Registration

To persist your filter you will need to login or create a new account. The do the later:

- Click on "Register" in the upper right

![register1](@/assets/posts/blocktrac-tutorial/register1.png)

- Enter a valid email address and password.

![register2](@/assets/posts/blocktrac-tutorial/register2.png)

- Click on **Register**
- Open your email and click the link contained within. If you did not receive the email, check your spam folder.

![register-email](@/assets/posts/blocktrac-tutorial/register-email.png)

Now you are good to go!

## Logging in

Once your register, or if you already have an account, login to create and manage your filters.

- Click on 'Login' in the upper right

![login1](@/assets/posts/blocktrac-tutorial/login1.png)

- Enter your email and password

![login2](@/assets/posts/blocktrac-tutorial/login2.png)

- Click on **Login**

If you forgot your password:

- Click on *Forgot Password?* on the login form
- You will be prompted to enter your email

![reset-password](@/assets/posts/blocktrac-tutorial/reset-password.png)

- Click on *Reset*
- Check your email and click on the provided link. If you did not receive the email, check your spam folder.
- Finally enter your new password
- Click *Reset* and you are good to go!

## Viewing and editing filters

Once you logged in, you can view your filters via the left hand navigation:

![my-filters](@/assets/posts/blocktrac-tutorial/my-filters.png)

Click on a specific filter to edit, duplicate, and delete.

![filter-matches](@/assets/posts/blocktrac-tutorial/filter-matches.png)

Here you will be presented with the last 100 transactions which your filter matched as well as the ability to test your filter against a library of pre-captured transactions. Simply click **Test Filter** to see the results!

![test-filter](@/assets/posts/blocktrac-tutorial/test-filter.png)

## Programmatic Integration

You may choose to get notifications through email or text message via Block Trac. Advanced users can specify API endpoints which will automatically be invoked when matching transactions occurs. Block Trac is a great way to integrate Blockchain activity into any programming environment, such as trading bots, auditing/forensics platforms, and much more!

![edit-filter](@/assets/posts/blocktrac-tutorial/edit-filter.png)

## Settings

Notification times and batch sizes may be set via the 'Settings' form:

- Click **Settings** in the left hand navigation

![settings1](@/assets/posts/blocktrac-tutorial/settings1.png)

- Modify settings accordingly, for quicker notifications, smaller batch sizes, and access to more notification endpoints, upgrade your account (see below).

![settings2](@/assets/posts/blocktrac-tutorial/settings2.png)

## Upgrade Account

To unlock the full power of Block Trac, upgrade your account.

- Click **Get a pro account** on the top of the screen. 

![upgrade1](@/assets/posts/blocktrac-tutorial/upgrade1.png)

- Select the plan which you are interested in.

![upgrade2](@/assets/posts/blocktrac-tutorial/upgrade2.png)

- Customize your plan, you may add additional filters and notification endpoints (sinks) beyond which your plan allows for an additional charge

![upgrade3](@/assets/posts/blocktrac-tutorial/upgrade3.png)

- Enter payment details and you are done!

![upgrade4](@/assets/posts/blocktrac-tutorial/upgrade4.png)

## Conclusion

We hope this article helped guide you through your journey into Block Trac. Be sure to subscribe to the Dev Null Productions' blog for more updates: support for more Blockchains, more notification endpoints, and many more exciting features are coming soon!
