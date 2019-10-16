TOPIC: Application Context
AUTHORS: Rolfe Dlugy-Hegwer; rolfedh@github.com; github:rolfedh
         Joe Medley; jmedley@chromium.org; github:jpmedley

# Application Context

An **application context** is a top-level browsing context that has a
manifest applied to it.

If an application context is created as a result of the user agent being asked to navigate
to a deep link, the user agent must immediately navigate to the deep link with replacement enabled.
Otherwise, when the application context is created, the user agent must immediately navigate to the
start URL with replacement enabled.

Please note that the start URL is not necessarily the value of the start_url member: the user or user
agent could have changed it when the application was added to home-screen or otherwise bookmarked.
