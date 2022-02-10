# Marketing Redirect

Do you have a marketing page and an app with two separate, but similar domains?
Something like `datadog.com` and `app.datadog.com`, or `digitalocean.com` and `cloud.digitalocean.com`?

Did you know that your users frequently go to the former when they intended to go to the latter?
Did you know this is frustrating UX,
especially when there isn't a clear way to find a link to the "app" page from the marketing page?

## What if your cusmers could go straight to the application they're paying for?

To give them the great UX they're paying for, simply:
1. Copy the code from `redirect-script.html` onto your marketing page. Replace the `YOUR_SITE_HERE` text with the url of your app.
2. Put a `<button>` element anywhere on the page with the id `marketing-redirect`. For example,
`<button id="marketing-redirect">Always go to app</button>` would be perfect.
3. Style your button using any classes you want.

Now, whenever your customer ends up on the marketing page, they can opt in to simply being redirected to the app. That's great UX?

## What if a customer wants to stop being redirected from the marketing page to the app?

Simply send the user to your marketing page with the value `disable-marketing-redirect` somewhere in the hash. If your marketing page is located at `coolcompany.com`, just put a link to the url `https://coolcompany.com/#disable-marketing-redirect` and the redirect will be turned off. You could put that link in the settings page of your app.

# Example

To see `marketing-redirect` in action, go to [the marketing page](https://elliotaplant.github.io/marketing-redirect), which is just the `index.html` file in this repo. Click the "Always go to app" button to always be redirected to the app page. Try going to the marketing page again, and see your browser get redirected to the app. When you're done, click "Disable marketing redirect" to disable the automatic redirect.

# Couldn't you just do this with a redirect on your server?

I expect that many companies don't have the same people in charge of the marketing page and a user level setting to control http codes.

# Future plans and monetization

In the future I would like to turn this into a cloud service that integrates with analytics providers to help marketing teams distinguish existing customers from genuine leads.
